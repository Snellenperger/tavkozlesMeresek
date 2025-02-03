# MÉRÉSI JEGYZŐKÖNYV   
# Méréstechnikai Feladat: Hálózat tervezés      

**A mérést végző neve:** Snellenperger Sándor   
**A mérés tárgya:**  DVB-T jel fejállomásba küldése és IPTV rendszeren való kiadása  
**A mérés száma:** 01. mérés    
**A mérés dátuma:** 2025. 02. 3.    
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
  - Hálózati eszköz: IGMP protokollt támogató és DHCP képes router internet kapcsolattal (TPlink)
  - Mérőműszer: METEK HDD digitális TV jelmérő
  - Jelosztó a fejállomás bemeneteire érkező jelek kialakításához (RF16)

Az antennát behangoltuk a legjobb vételhez a METEK HDD segítségével. (DNY 234°)  
### Itt ilyen értékeket mértünk:  
Jelszint: 51dB  
MER(Modulation Error Ratio): 25dB  
Kódolása: QPSK/8K/1/32  

### Kültéri időjárási viszonyok:  
Páratartalom: 72%  
Szél: 6km/h  
Nyomás: 1027,8mB  
Hőmérséklet: 3°  

Következő lépésként a LEMCO fejegységre kötöttük az antennát ami egy 4 es osztórol (RF16) került bekötésre.  
A fejegység IP címe a 192.168.1.200 amit parancsorból az arp -a paranccsal tudtuk meg. Ezután statikusa a 192.168.1.1 címról kezdtük a konfigurációt.  
A fejegységen a bementeket a megfelelő csatornára hangoltuk az ingyenesen fogható csatornák miatt, amik különböző multiplexeléssel érkeztek.
Itt 35-44 % jelerősséget fogtunk de az összes kimeneten 100% minőséget vettünk.

Ezek a következőek:   
                    - Multiplex A  
                    - Multiplex B  
                    - Multiplex E  
                    - Miskolc Városi TV    
                    
Az átrendezett csatornákat a 224.0.0.1 -es Multicast IP címmel továbbítjuk ahol a csatornákat 1001-es porttól kezdve számoztuk.

A TPlink konfigurációjával folytattuk a 192.168.0.1-es címen:       
                                                              - IP cím: 192.168.1.1  
                                                              - DHCP pool: 192.168.1.100-192.168.1.249  
                                                              - SSID: IPTV    
                                                              - Jelszó: 12345678    
                                                              - Dynamic IP    
                                                              - IGMP Snooping : On    
                                                              - A router portjait is a felhasználás szerint konfigoltuk    

Sikeresen zártuk a feladatot hiszen a routerünk sikeresen osztja az általunk beállított TV csatornákat és internet kapcsolatunk is elérhető.
A Set Top Box-ra a LEMCO fejegységről a kész konfigot egy M3U fájlként mentettünk, amit egy pendrive segítségével Set Top Boxra sikeresen felmásoltunk.
A TV-n 22.2 Mbps adatátviteli sebességet mértünk.

A következő értékeket mértük az IP TV-vel kapcsolatban:

## Értékelés  
Sajnos a csatornákat nem sikerült szépen sorba rendezni de ez módosítható akár a set top boxon is. A DIKH TV pedig sajnos lemaradt, lehet másik multiplexbe került. Vigyázni kell, hogy a TPlink routerünket ne állítsuk se AP módba. 

                                










