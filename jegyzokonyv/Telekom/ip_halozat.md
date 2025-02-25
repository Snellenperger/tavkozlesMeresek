
### Disztribúciós Switch
```cisco
Current configuration : 2471 bytes  
!  
! Last configuration change at 14:05:08 CET Thu Feb 20 2025 by sanyi  
! NVRAM config last updated at 13:44:29 CET Thu Feb 20 2025 by sanyi  
!  
version 15.0  
no service pad  
service timestamps debug datetime msec  
service timestamps log datetime msec  
service password-encryption  
!  
hostname Distribution1  
!  
boot-start-marker  
boot-end-marker  
!  
!  
enable secret 5 $1$zBYg$gHV7HfuIrY5dwbj54sQRw0  
!  
username admin secret 5 $1$grcv$yISMKSr3qizEAbAbWmaYH/  
aaa new-model  
!  
!  
aaa authentication login default group radius local  
aaa authorization console  
aaa authorization exec default group radius local  
!  
!  
!  
!  
!  
!  
aaa session-id common  
clock timezone CET 1 0  
clock summer-time CEST recurring last Sun Mar 2:00 last Sun Oct 3:00  
system mtu routing 1500  
vtp mode transparent  
ip routing  
ip domain-name Telekom.intra  
!  
!  
!  
!  
!  
!  
!  
!  
!  
!  
!  
!  
spanning-tree mode rapid-pvst  
spanning-tree extend system-id  
!  
vlan internal allocation policy ascending  
!  
ip ssh version 2  
!  
!   
!  
!
!
!
!
!
!
!
!
!
!
!
interface Loopback0
 ip address 10.0.0.193 255.255.255.255
 ip ospf 1 area 0
!
interface FastEthernet0/1
 no switchport
 ip address 192.168.254.2 255.255.255.252
 ip ospf network point-to-point
 ip ospf 1 area 0
!
interface FastEthernet0/2
 no switchport
 ip address 192.168.254.9 255.255.255.252
 ip ospf network point-to-point
 ip ospf 1 area 0
!
interface FastEthernet0/3
 no switchport
 ip address 192.168.254.70 255.255.255.252
 ip ospf network point-to-point
 ip ospf 1 area 0
!
interface FastEthernet0/4
 no switchport
 ip address 192.168.254.78 255.255.255.252
 ip ospf network point-to-point
 ip ospf 1 area 0
!
interface FastEthernet0/5
 no switchport
 ip address 192.168.254.86 255.255.255.252
 ip ospf network point-to-point
 ip ospf 1 area 0
!
interface FastEthernet0/6
 shutdown
!
interface FastEthernet0/7
 shutdown
!
interface FastEthernet0/8
 shutdown
!
interface GigabitEthernet0/1
!
interface Vlan1
 no ip address
 shutdown
!
router ospf 1
 passive-interface Loopback0
!
no ip http server
no ip http secure-server
!
!
!
ip access-list standard REMOTE_CLI
 permit 10.0.1.2
!
ip radius source-interface Loopback0
logging source-interface Loopback0
logging host 10.0.1.2
!
!
!
radius server radius
 address ipv4 10.0.1.2 auth-port 1812 acct-port 1813
 key 7 09444B05150A464058
!
!
!
vstack
!
line con 0
line vty 0 4
 access-class remote_cli in
 transport input ssh
line vty 5 15
 access-class remote_cli in

 transport input ssh
!
ntp source Loopback0
ntp server 10.0.1.2
end
```

