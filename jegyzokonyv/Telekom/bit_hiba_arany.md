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



### Méréshez használt eszközök:
  - 2 cisco Catalyst 3560 series switch S/N: CAT1027ZGQ1
  - ETS-1000L Ethernet Loopback S/N: MTKL006
  - Exfo FTB-200 Packet analyzer S/N: 553698 
  - 2 optikai vezeték
  - Acterna OLP-6 Optical Power Meter
  - JDSU OLA-55 (programozható csillapító) S/N: MUSZ4222
  - 2db SFP-GE-LX CC1310nm S/N:SCB7630094
  - 2db SFP-GE-ZX CC1550nm S/N: SE9C780017
  - 10dB csillapító
  - SFP-GE-MBU-31D CC TX1310,RX1490 S/N: BU10YE75520005
  - SFP-GE-MBU-31D CC TX1490,RX1310 S/N: BU10YE75520006














Sanyi adása -10,7dBm a mért érték műszer szerint





                              High Alarm  High Warn  Low Warn   Low Alarm
          Temperature         Threshold   Threshold  Threshold  Threshold
Port       (Celsius)          (Celsius)   (Celsius)  (Celsius)  (Celsius)
--------- ------------------  ----------  ---------  ---------  ---------
Gi0/3       53.7               110.0        95.0       -42.0      -45.0

                              High Alarm  High Warn  Low Warn   Low Alarm
           Voltage            Threshold   Threshold  Threshold  Threshold
Port       (Volts)            (Volts)     (Volts)    (Volts)    (Volts)
---------  ---------------    ----------  ---------  ---------  ---------
Gi0/3      3.14                  3.60        3.50        3.05       3.00

           Optical            High Alarm  High Warn  Low Warn   Low Alarm
           Transmit Power     Threshold   Threshold  Threshold  Threshold
Port       (dBm)              (dBm)       (dBm)      (dBm)      (dBm)
---------  -----------------  ----------  ---------  ---------  ---------
Gi0/3       -6.8                -1.0        -2.0       -10.0      -11.0

           Optical            High Alarm  High Warn  Low Warn   Low Alarm
           Receive Power      Threshold   Threshold  Threshold  Threshold
Port       (dBm)              (dBm)       (dBm)      (dBm)      (dBm)
-------    -----------------  ----------  ---------  ---------  ---------
Gi0/3       -5.2                -3.0        -4.0       -23.0      -24.0


Áramkör tesztelése egy szándékosan küldött bit hibával.


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


