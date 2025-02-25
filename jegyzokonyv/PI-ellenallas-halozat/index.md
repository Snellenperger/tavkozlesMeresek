## &#928; Csillapító Áramkör Mérési Jegyzőkönyv

**Mérés helye**: Miskolci SZC Kandó Kálmán Informatikai Technikum   
**A mérést vezette**: Sándor Péter  
**Cél**: A pi csillapító áramkör elemzése.

---

### 1. **A mérés célja**

Egy olyan négypólusú Π csillapító áramkör építése aminek a bemenetére egy 600 Ω belső ellenállású jelgenerátort kötünk, és a cél, az hogy 6 dB csillapítást érjünk el a kimeneten amit egy oszcilloszkóppal fogunk mérni.

### 2. **A mérés menete**

Egy Π csillapító áramkör kalkulátort kerestem, ahova az előre meghatározott értékeket megadtam: kért csillapítás 6dB, impedancia 600 Ω. Így a kalkulátor megadta, a legoptimálisabb ellenállás értékeket.

![image](https://github.com/user-attachments/assets/c2e08f2c-e3f4-4301-910e-3c919be68bc7)

Következő lépésként egy blokk vázlatot készítettem a falstadban, amiben található egy 600 Ω értékű terhelés, kettő feszültségmérő (ellenőrzés miatt), egy olyan DC generátor aminek 600 Ω a belső ellenállása és a Π csillapító tag, ami 3 ellenállásból áll. Az R1 és az R3 megegyezik. Az R2=448.2 Ω az R1=R3=1805 Ω-al. Itt egy ellenőrzést is végeztem, hogy a 6dB csillapítás biztosan elérhető lesz ezekkel az értékekkel.

![image](https://github.com/user-attachments/assets/78c0a220-05a1-4784-89fe-eeb7e051c8b3)

Pontos ellenállás értékeket nem találtam így ezekkel az értékekkel számoltam ellenben a blokk vázlatton feltüntett adatokkal szemben: R1=R3=1690 Ω, R2=680 Ω, és a terhelő ellenállás értéke is 680 Ω lett. Így a számítások is ezek szerint alakultak.

![image](https://github.com/user-attachments/assets/2931091f-d6bf-48d6-842d-20ac4ce0a896)

Sikeresen összekötöttem egy breadbordon, amire a jelgenerátort sikeresen rákötöttem és egy 1kHz-es, 5V jelet generáltam, és az osszcilloszkópon sikeresen mértem a 2Vpp-t jelet ami a névleges ellenállások mellett, még elfogadható tartományban volt.

![image](https://github.com/user-attachments/assets/20160b80-d60f-4b13-b57e-5f9d2a6c57be)


### 3. **Következtetések**
A pontos értékek meghatározása talán legfontosabb lépés, hiszen ez fogja adni az egésznek az alapot. Nagy segítséget jelenthet, ha az áramkört egy program seítségével először szimulálod, így ellenőrizni, ezáltal kiszűrni az esetleges hibákat.


