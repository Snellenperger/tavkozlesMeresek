# MÉRÉSI JEGYZŐKÖNYV   
## Hálózat építés      

**A mérést végző neve:** Snellenperger Sándor   
**A mérés tárgya:** Komplex hálózat telepítése, konfigurálása  
**A mérés száma:** 01. mérés    
**A mérés dátuma:** 2025. 02. 13.    
**A mérést vezette:** Major András    

**Évfolyam:** 13. E  
**Helyszín:** Telekom Duális helyszín

## Feladat Leírása   


## Használt Eszközök:  
  - 5db Cisco Catalyst 3560 series Layer 3 Switch
  - Cisco 800 Series SOHO Router (S/N: CISCO0871V03)

### Konfigurálás, kalibráció:  
Miután megfelelően összekötöttünk mindent az iPASOLINK webes felületén (alapértelmezett elérése: http://172.17.254.253) a következőket állítottunk be a rádiós összeköttetés érdekében:  
  - Channel Spacing: 28MHz
  - Reference Modulation: QPSK
  - TX Frekvencia: 24800Hz
  - TX Power Controll: MTPC(Manual Transmission Power Control)
  - AMR modulációk: QPSK,16QAM,32QAM,64QAM,128QAM,256QAM
  - TX Power: 0dBm(1mW)  

Az átalakító tag bekötése után 3-3 dB veszteséget mértünk az eszközökön.  

![image](https://github.com/user-attachments/assets/3400b0b6-ef54-4043-91dd-3db44f538a80)

### Mérés, adatgyűjtés:  
Következő lépésként beiktattuk az állítható csillapító tagot és ezzel modelleztünk több időjárási körülményt. Ezt a webes felületen követtük végig.
![csillapú](https://github.com/user-attachments/assets/9f7c05de-7bce-4158-80ce-1bd9675799ca)  
  

![onlineeee](https://github.com/user-attachments/assets/1c50c0a1-8c3b-457d-b883-3e9f10190bf1)  

A szakaszcsillapítást 10dB-es lépésekkel növeltük, egészen 20-90dB-ig. Ez a folyamat alatt figyeltük a bejövő szintet, a mért feszültésget, illetve a leolvasott RX és TX modulációkat.  

![exc](https://github.com/user-attachments/assets/e91dea8c-6976-4f23-9a23-704d06bbe213)  
A következőket tapasztaltuk:
  - -60dB-nél már visszább lépett a modulációkban, a stabilabb adatátvitel érdekében  
  - -70dB-ig a jelünk elfogadható, nem esik szét teljesen  
  - A mért feszültség szinte egyenesen arányosan változik a bejövő szinthez képest

Ezeket az adatokat egy grafikon segítségével ábrázoltuk majd összevetettük a gyári (ideális) értékekkel és nagyon minimális eltérést tapasztatunk.
![meresek](https://github.com/user-attachments/assets/112bf978-7d54-437c-b6c3-ab3170b6e5e4)

### Áramfelvétel:  
Megmértük, hogy mennyi áramot vesznek fel az iPASOLINK eszközök, és hogy milyen feszültség van rajtuk. Azt lehetett tapasztalni, hogy amíg a Bootolás folyt addig 1,2A-t stabilan, miután elkezdődött a kommunikáció az eszközök között ez az érték felmászott egészen 1,66A is ami mellett 48,1V van rajta.  

![aram](https://github.com/user-attachments/assets/effc37ca-d797-45fd-a2ce-84dbf8cb3955)

## Értékelés:
A feladat során nagyon érdekes és látványos volt modellezni hogy nagyjából hogyan változtathatják az időjárási viszonyok az adatátvitelt rádiós eszközökön. Azt tapasztaltuk, hogy -90dB-nél már teljesen megszűnik a rádiós összeköttetés, az adatátvitellel együtt. Sokat segített az online és ezáltal könnyen menedzselhető felületete a iPASOLINK-nek. A mérés során sikeresen modelleztük a rádiós adatátvitel csillapításból adódó változásait és az eredmények minimális eltérést mutattak az ideális gyári értékekhez képest.

