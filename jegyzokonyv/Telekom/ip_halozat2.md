### Router

```cisco
Current configuration : 2290 bytes
!
version 12.4
no service pad
service timestamps debug datetime msec
service timestamps log datetime msec
service password-encryption
!
hostname Router_internet
!
boot-start-marker
boot-end-marker
!
enable secret 5 $1$/9JW$1A6THpdaIKGauZxD2E1/q0
!
aaa new-model
!
!
aaa authentication login default group radius local
aaa authorization console
aaa authorization exec default group radius local
!
!
aaa session-id common
clock timezone CET 1
clock summer-time CEST recurring last Sun Mar 2:00 last Sun Oct 3:00
!
!
!
!
ip cef
!
!
!
!
ip domain name Telekom.intra
!
multilink bundle-name authenticated
!
!
vtp mode transparent
username admin secret 5 $1$qfD6$HP07TjTsJKYl0SSIp7r4M/
archive
 log config
  hidekeys
!
!
vlan 20
 name Access1
!
vlan 30
 name Access2
!
ip ssh version 2
!
!
!
interface Loopback0
 ip address 10.0.0.254 255.255.255.255
 ip ospf 1 area 0
!
interface FastEthernet0
 shutdown
!
interface FastEthernet1
 switchport access vlan 20
!
interface FastEthernet2
 switchport access vlan 30
!
interface FastEthernet3
 shutdown
!
interface FastEthernet4
 ip address dhcp
 ip nat outside
 ip virtual-reassembly
 duplex auto
 speed auto
!
interface Vlan1
 no ip address
!
interface Vlan20
 ip address 192.168.254.10 255.255.255.252
 ip nat inside
 ip virtual-reassembly
 ip ospf network point-to-point
 ip ospf 1 area 0
!
interface Vlan30
 ip address 192.168.254.6 255.255.255.252
 ip nat inside
 ip virtual-reassembly
 ip ospf network point-to-point
 ip ospf 1 area 0
!
router ospf 1
 log-adjacency-changes
 passive-interface Loopback0
 default-information originate
!
ip route 0.0.0.0 0.0.0.0 dhcp
!
!
no ip http server
no ip http secure-server
ip nat inside source list 1 interface FastEthernet4 overload
!
ip access-list standard REMOTE_CLI
 permit 10.0.1.2
 deny   any
!
ip radius source-interface Loopback0
access-list 1 permit 10.0.1.0 0.0.0.3
access-list 1 permit 172.16.0.0 0.0.0.63
access-list 1 permit 172.16.0.64 0.0.0.63
access-list 1 permit 172.16.0.128 0.0.0.63
!
!
!
radius-server host 10.0.1.2 auth-port 1812 acct-port 1813 key 7 151A0E0008257A767B
!
control-plane
!
!
line con 0
 no modem enable
line aux 0
line vty 0 4
 transport input ssh
!
scheduler max-task-time 5000
ntp clock-period 17179861
ntp source Loopback0
ntp server 10.0.1.2

!
webvpn cef
end
```
