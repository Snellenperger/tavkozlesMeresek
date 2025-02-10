# MÉRÉSI JEGYZŐKÖNYV   
     
**A mérést végző neve:** Snellenperger Sándor   
**A mérés tárgya:**  Amplitúdómoduláció vizsgálata a GRF-1300A trénerrel  
**A mérés száma:** 01. mérés    
**A mérés dátuma:** 2025. 02. 10.    
**A mérést vezette:** Sándor Péter    

**Évfolyam:** 13. E  
**Csoport:** GYAK 1  
**Helyszín:** V3 Labor 

## Feladat Leírása   
A vizsgázó feladata egy földfelszíni digitális TV vételi rendszer kiépítése, a megfelelő adótorony (Miskolc, Avasi adótorony) kiválasztása, a jel mérésének és elosztásának elvégzése, valamint az IPTV rendszer konfigurálása.

A fogható multiplexek jelerősségének ellenőrzése, és a DVB-T jel LEMCO SCL-824CT fejállomásba történő bevezetése. A fejállomásból a digitális tartalom IPTV streamként kerül kiadásra.

A Multicast IP tartomány megválasztása és az IPTV Set-top-box konfigurálása a megfelelő vételhez.

## Használt Eszközök:  
  - Beltéri vagy kültéri antenna    
  - Fejállomás: LEMCO SCL-824CT 8 × DVB-S/S2/T/T2/C to 4 × DVB-T/C & IP (FTA)  
  - Set-top box: MAG IPTV
  - Hálózati eszköz: IGMP protokollt támogató és DHCP képes router internet kapcsolattal (ASUS)
  - Mérőműszer: METEK HDD digitális TV jelmérő
  - Jelosztó a fejállomás bemeneteire érkező jelek kialakításához (RF16)  
  
Első lépésként a router (ASUS) konfigurációjával kezdtünk.  
                                                          -wifi SSID: furti  
                                                          -Jelszó: furti12345
                                                          - Router IP: 192.168.50.1 
                                                          Bejelentkezés:  
                                                          -User: admin  
                                                          -Jelszó: admin12345  
                                                           
                                                          
              

Az antennát behangoltuk a legjobb vételhez a METEK HDD segítségével. (DNY 240°)  
### Itt ilyen értékeket mértünk:  
Jelszint: 51dB  
MER(Modulation Error Ratio): 25dB  
Kódolása: QPSK/8K/1/32  
### Kültéri időjárási viszonyok:  
Páratartalom: 74%  
Szél: 5km/h  
Nyomás: 1033,8mB  
Hőmérséklet: 3°C  

![image](https://github.com/user-attachments/assets/08f85285-c379-4e01-b706-6fc20fa6d507)  
![image](https://github.com/user-attachments/assets/97289298-d209-4128-9f02-45fed1d5cbd2)  



Következő lépésként a LEMCO fejegységre kötöttük az antennát ami egy 4 es osztórol (RF16) került bekötésre.    
A fejegység IP címe a 192.168.1.200 amit parancsorból az arp -a paranccsal tudtuk meg. Ezután statikusa a 192.168.50.1 címról kezdtük a konfigurációt.  
Hogy egy hálózatba kerüljünk ahhoz a router ip címein kellett változtatnunk így az 192.168.1-es hálózatba hoztuk. 192.168.1.1 lett az ASUS címe és 192.168.1.2-254 osztja a címeket.  
A fejegységen a bementeket a megfelelő csatornára hangoltuk az ingyenesen fogható csatornák miatt, amik különböző multiplexeléssel érkeztek.  
Itt 36-51 % jelerősséget fogtunk de az összes kimeneten 100% minőséget vettünk.  

Ezek a következőek:   
                    - Multiplex A  
                    - Multiplex B  
                    - Multiplex E  
                    - Miskolc Városi TV     

![asd](https://github.com/user-attachments/assets/afc9b856-80b1-4df4-90c3-a380cde61fda)  
![asdsa123](https://github.com/user-attachments/assets/99e5f498-029e-40c9-b4a1-265710762776)


                    
Az átrendezett csatornákat a 239.1.1.1 -es Multicast IP címmel továbbítjuk ahol a csatornákat 1234-es porttól kezdve számoztuk UPD protokollal.

Sikeresen zártuk a feladatot hiszen a routerünk sikeresen osztja az általunk beállított TV csatornákat és internet kapcsolatunk is elérhető.
A Set Top Box-ra a LEMCO fejegységről a kész konfigot egy M3U fájlként mentettünk, amit egy pendrive segítségével Set Top Boxra sikeresen felmásoltunk.
A TV-n 22.2 Mbps adatátviteli sebességet mértünk.

A következő értékeket mértük az IP TV-vel kapcsolatban:
WireSharkon a mérésünk, amely az összes fogott csatornát mutatja.
![Képernyőkép 2025-02-05 125808](https://github.com/user-attachments/assets/e5fd0794-a745-41fa-9206-662626aab89a)  

A VLC mérésünk amelyen a 4 képkocka kiesés az teljesen normális hiszen ez egy optimális kiesés a stream betöltésekor.
![Képernyőkép 2025-02-05 131512](https://github.com/user-attachments/assets/be7fb1d5-7e59-4b58-aa28-0bbdbb1dcf60)



## Értékelés  
Sajnos a csatornákat nem sikerült szépen sorba rendezni de ez módosítható akár a set top boxon is. A DIKH TV pedig sajnos lemaradt, lehet másik multiplexbe került. Vigyázni kell, hogy az ASUS routerünket ne állítsuk se AP módba. 

                                
