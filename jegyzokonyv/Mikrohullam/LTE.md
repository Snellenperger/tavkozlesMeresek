# Snellenperger Sándor 
## Távközlési hálózatok Jegyzőkönyv
---
Felhasznált eszközök:
- Mikrotik LHG18 LTE antenna
- Mikrotik nRay 60GHz mikrohullámú antenna szett
- ASUS SOHO router
- Laptop

Használt szoftverek:
- winbox
- speedtest.net

---
Első lépésként a hálózati eszközök gyári beállításainak visszaállításával kezdtem.  
Az LTE antenna beállításával folytattam, amelynek a 192.168.88.1 IP címet állítottam illetve DHCP szerverként is üzemeltettem ahol a címeket 192.168.88.100-192.168.88.250 osztja. Később a dátum is frissítésre került.
Itt 1-2 tesztet is készítettem, erről a képeket alább láthatja.
![teszt1-3](https://github.com/user-attachments/assets/aa5d7660-2c61-4789-be04-b10fb78dc82d)
![meres2](https://github.com/user-attachments/assets/e134eda3-d649-4a13-ace9-250357166908)

Ezután következett a Mikrotik nRay 60GHz antennák beállítása.
Itt az egyik egy Slave a másik pedig Master módban lett konfigurálva. Megkapták a 192.168.88.2 és a 192.168.88.3 címeket. A dátum és az idő illete a jelszó az előzőhöz hasonlóan itt is frissítésre került.

Következő lépésként az online felületén AP módba konfiguráltuk az ASUS routerünket. A megfelelő címekkel illetve felhasználói beállításokkal.
Ez a pont után pedig már  meg is kaptuk a címünket és kezdhettük a teszteléseket. 
Parancssorban meg is pingeltem az összes beállított címet.

<details>
  <summary>Ping tesztelés</summary>
C:\Users\Admin>ping 192.168.88.1

Pinging 192.168.88.1 with 32 bytes of data:
Reply from 192.168.88.1: bytes=32 time<1ms TTL=64
Reply from 192.168.88.1: bytes=32 time<1ms TTL=64
Reply from 192.168.88.1: bytes=32 time<1ms TTL=64

Ping statistics for 192.168.88.1:
    Packets: Sent = 3, Received = 3, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 0ms, Maximum = 0ms, Average = 0ms
Control-C
^C
C:\Users\Admin>ping 192.168.88.2

Pinging 192.168.88.2 with 32 bytes of data:
Reply from 192.168.88.2: bytes=32 time<1ms TTL=64
Reply from 192.168.88.2: bytes=32 time<1ms TTL=64
Reply from 192.168.88.2: bytes=32 time<1ms TTL=64

Ping statistics for 192.168.88.2:
    Packets: Sent = 3, Received = 3, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 0ms, Maximum = 0ms, Average = 0ms
Control-C
^C
C:\Users\Admin>ping 192.168.88.3

Pinging 192.168.88.3 with 32 bytes of data:
Reply from 192.168.88.3: bytes=32 time=1ms TTL=64
Reply from 192.168.88.3: bytes=32 time=1ms TTL=64
Reply from 192.168.88.3: bytes=32 time=1ms TTL=64
Reply from 192.168.88.3: bytes=32 time=1ms TTL=64

Ping statistics for 192.168.88.3:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 1ms, Maximum = 1ms, Average = 1ms

C:\Users\Admin>

C:\Users\Admin>ping 192.168.88.4

Pinging 192.168.88.4 with 32 bytes of data:
Reply from 192.168.88.4: bytes=32 time<1ms TTL=64
Reply from 192.168.88.4: bytes=32 time<1ms TTL=64
Reply from 192.168.88.4: bytes=32 time<1ms TTL=64
Reply from 192.168.88.4: bytes=32 time<1ms TTL=64

Ping statistics for 192.168.88.4:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 0ms, Maximum = 0ms, Average = 0ms
</details>

Majd teszteltük a Mikrotik nRay 60GHz antennapárunk között kapcsolatot.
Ehhez az iperf parancsot használtuk parancssorban.

![iperf](https://github.com/user-attachments/assets/a3e4b82b-4e2b-4b5a-8c1a-595a9cf38628)
![teszt utols2](https://github.com/user-attachments/assets/9951816f-384a-4cab-8b73-1865da7e26fe)  
 A Laptopról is csináltam a speedtestet ezt pedig itt láthatja.
 ![speed](https://github.com/user-attachments/assets/7616060a-0c94-478e-a3be-7e247b1187e8)

 Majd amikor mindennel készen lettem akkor megszerkesztettem Draw.io alkalmazásban a topológiai ábráját.
 ![drawio](https://github.com/user-attachments/assets/2bdc2c88-f844-41f2-989c-7fff1da27aad)

### Következtetéseim:  
A feladat során a Mikrotik mikrohullámú antenna szett, pontos beállítása lényeges, hiszen minimális eltérés is jelentős veszteséget eredményezhet.  
A konfiguráció sikeres volt, és a hálózat minden eszköze megfelelően működött. A helyi hálózat gyors és stabil, az eszközök közötti kommunikáció akadálymentesen zajlott.  




  
  
  
  



  
