# MÉRÉSI JEGYZŐKÖNYV   
## Szakaszcsillapítás      

**A mérést végző neve:** Snellenperger Sándor   
**A mérés tárgya:**  Szakaszcsillapítás modellezése különböző vételi szinteknél  
**A mérés száma:** 01. mérés    
**A mérést vezette:** Balázs Géza    
 
**Helyszín:** Telekom Duális helyszín

## Feladat Leírása   
A mérés célja, hogy modellezzük és megmérjük egy mikró szakasz rádiós paramétereit különböző csillapításoknál. Majd az eredményt összehasonlítani az ideális adatokkal.

## Használt Eszközök:  
  - NEC iPASOLINK VR4 beltéri (S/N: 4402)
  - ODU VR4 iPASOLINK TRP-26G-1D kültéri (alsó oldalsáv) (S/N: 19838)
  - 48V Tápegység HP-P200 DC 48V 4,2A (S/N: 52044274)
  - Digitális multiméter METEX (S/N: MUSZ4075)
  - 20 dB fix csillapító
  - Állítható csillapító You Hewlett Packard 0-70dB, 10dB léptékkel (Működési tartomány DC: 26,5GHz)

### Konfigurálás, kalibráció:  
Miután megfelelően összekötöttem mindent az iPASOLINK webes felületén (alapértelmezett elérése: http://172.17.254.253) a következőket állítottam be a rádiós összeköttetés érdekében:  
  - Channel Spacing: 28MHz
  - Reference Modulation: QPSK
  - TX Frekvencia: 24800Hz
  - TX Power Controll: MTPC(Manual Transmission Power Control)
  - AMR modulációk: QPSK,16QAM,32QAM,64QAM,128QAM,256QAM
  - TX Power: 0dBm(1mW)  

Az átalakító tag bekötése után 3-3 dB veszteséget mértem az eszközökön.  

![image](https://github.com/user-attachments/assets/3400b0b6-ef54-4043-91dd-3db44f538a80)

### Mérés, adatgyűjtés:  
Következő lépésként beiktattam az állítható csillapító tagot és ezzel modelleztem több időjárási körülményt. Ezt a webes felületen követtem végig.
![csillapú](https://github.com/user-attachments/assets/9f7c05de-7bce-4158-80ce-1bd9675799ca)  
  

![onlineeee](https://github.com/user-attachments/assets/1c50c0a1-8c3b-457d-b883-3e9f10190bf1)  

A szakaszcsillapítást 10dB-es lépésekkel növeltem, egészen 20-90dB-ig. Ez a folyamat alatt figyeltem a bejövő szintet, a mért feszültésget, illetve a leolvasott RX és TX modulációkat.  

![exc](https://github.com/user-attachments/assets/e91dea8c-6976-4f23-9a23-704d06bbe213)  
A következőket tapasztaltam:
  - -60dB-nél már visszább lépett a modulációkban, a stabilabb adatátvitel érdekében  
  - -70dB-ig a jelünk elfogadható, nem esik szét teljesen  
  - A mért feszültség szinte egyenesen arányosan változik a bejövő szinthez képest

Ezeket az adatokat egy grafikon segítségével ábrázoltam majd összevetettem a gyári (ideális) értékekkel és nagyon minimális eltérést tapasztatunk.
![meresek](https://github.com/user-attachments/assets/112bf978-7d54-437c-b6c3-ab3170b6e5e4)

### Áramfelvétel:  
Megmértem, hogy mennyi áramot vesznek fel az iPASOLINK eszközök, és hogy milyen feszültség van rajtuk. Azt lehetett tapasztalni, hogy amíg a Bootolás folyt addig 1,2A-t stabilan, miután elkezdődött a kommunikáció az eszközök között ez az érték felmászott egészen 1,66A is ami mellett 48,1V van rajta.  

![aram](https://github.com/user-attachments/assets/effc37ca-d797-45fd-a2ce-84dbf8cb3955)

## Értékelés:
A feladat során nagyon érdekes és látványos volt modellezni hogy nagyjából hogyan változtathatják az időjárási viszonyok az adatátvitelt rádiós eszközökön. Azt tapasztaltuk, hogy -90dB-nél már teljesen megszűnik a rádiós összeköttetés, az adatátvitellel együtt. Sokat segített az online és ezáltal könnyen menedzselhető felületete a iPASOLINK-nek. A mérés során sikeresen modelleztük a rádiós adatátvitel csillapításból adódó változásait és az eredmények minimális eltérést mutattak az ideális gyári értékekhez képest.
