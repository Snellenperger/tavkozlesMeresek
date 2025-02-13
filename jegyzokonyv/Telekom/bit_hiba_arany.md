# MÉRÉSI JEGYZŐKÖNYV   
## Optikai hálózat      

**A mérést végző neve:** Snellenperger Sándor   
**A mérés tárgya:**  Bit hibaarány mérése optikai hálózaton  
**A mérés száma:** 01. mérés    
**A mérés dátuma:** 2025. 02. 13.    
**A mérést vezette:** Hajdú Péter    

**Évfolyam:** 13. E  
**Helyszín:** Telekom Duális helyszín

## Feladat leírása
Több SFP tesztelése egy optikai hálózaton állítható csillapítóval és a bit hibaarányok figyelése.

### Méréshez használt eszközök:
  - 2 cisco Catalyst 3560 series switch (S/N: CAT1027ZGQ1)
  - ETS-1000L Ethernet Loopback (S/N: MTKL006)
  - Exfo FTB-200 Packet analyzer (S/N: 553698) 
  - Acterna OLP-6 Optical Power Meter
  - JDSU OLA-55 (programozható csillapító) (S/N: MUSZ4222)
  - 2db SFP-GE-LX CC1310nm (S/N:SCB7630094)
  - 2db SFP-GE-ZX CC1550nm (S/N: SE9C780017)
  - 10dB csillapító
  - SFP-GE-MBU-31D CC TX1310,RX1490 (S/N: BU10YE75520005)
  - SFP-GE-MBU-31D CC TX1490,RX1310 (S/N: BU10YE75520006)
  - 2 optikai vezeték

### Hálózati kapcsolat létrehozása
Első lépésként mind a 2 switchen a GigabitEthernet 0/3 portot access portként kezeltük és az előre létrehozott Vlan 10-be helyeztük a GigabitEthernet 0/1-es porttal együtt. Előbbi azaz a Gi0/3-on csatlakozott a 2 switch egymáshoz ide fogjuk az SFP-ket is behelyezni. A Gi0/1-en csatlakoztattuk az Ethernet Loopbacket illetve az Ethernet Analizátort.  
  
![jooooo](https://github.com/user-attachments/assets/44ef42ff-270b-488e-93ec-b28568dba26e)



### Az SFP-GE-LX CC 1310nm tesztelése

A switch semmi erősítés vagy csillapítás nélkül -6,8dBm adott és a riasztási értékei a következőek vételnél:
  - High Alarm Threshold: -3dBm
  - High Warning Threshold: -4dBm
  - Low Alarm Threshold: -23dBm
  - Low Warning Threshold: -24dBm
  
![limitek](https://github.com/user-attachments/assets/2dd2f39c-8e4c-4115-bd48-6b91c6531662)  

Az áramkört teszteltük szándékosan küldött bit hibával is. Ezt a Exfo FTB-200 Packet analyzerel nagyon szépen lehetett szemlélteni. A képen tökéletesen látszik, hogy korábban hiba nélküli hálózatot mutat de a hiba küldése után már számolta és jelezte is.

![hibakere](https://github.com/user-attachments/assets/f9b3580f-c2f6-468d-a435-95c68d0b0f40)  



Következő lépésként bekötöttük az állítható csillapítót. 1310nm re van állítva.  10dB állítva
így zsombinál már csak -16dB volt mérhető. Ez az én adásom korábban -5,6 körül volt.17,45 nél zsombinál már -24 dB volt a küldésem, ekkor már riasztott is nála hoszen alapértékként már 23 nál alarm 22 warning üzenetet küld.
Ennél a pintál már hibázott is, a műszer jól mutatta.
24,6 dB csillapításnál szét is dobta a hálózatot, ekkor zsombinál -31.5 mért. 23,5 csillapításnál állt helyre újra a kapcsolat, ekkor zsombinál -31 dB van.

24,2 nél még nem hibázik de 24,4 nál már hibáztak a bitek.
-31,5dB


A kvetkező sfpnél már egy 10dB csillapítót tettünk bele.

-2 és -26 között kell lennie ezért tettünk bele csillapítást.

-31,5 csillapításnál még jó volt a jelfolyam, és olyan 32,4 körül már dobálta a biteket.






Riasztása -2,-23 



-22,7 nél még jó a jelünk itt a jleszintünk  a vételi jelünk most -30dB  ,  -23,45 már érezhető a bithiba


