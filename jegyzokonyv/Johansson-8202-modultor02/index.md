# MÉRÉSI JEGYZŐKÖNYV

**A mérést végző neve:** Snellenperger Sándor, Csépke Péter  
**A mérés tárgya:** Bitsebesség vs jelminőség mérési feladat  
**A mérés dátuma:** 2024.11.27.  
**A mérést vezette:** Sándor Péter  
**Évfolyam:** 13. E  
**Csoport:** GYAK 2  
**Helyszín:** V3
## 1. Mérés célja

A Johansson 8202 DVB-T modulátoron többcsatornás jelszint generálására. A gyakorlat során két különböző programot konfigurálunk, és mérjük a jel minőségét különböző bitráták alkalmazásával. Összehasonlítani a 2 eszközön generált jel viszonyát.

## 2. Alkalmazott mérőeszközök és készülékek  

| Műszer neve | Típus          | Gyártási szám |
| ---------------- | ---------------- | -------------- | 
| Johansson 8202      | HDMI Modulator     | 2341010237801         | 
|       Johansson 8202            | HDMI Modulator   | 2341010237504     |
|           METEK HDD       | Spektrum analizátor | 211112002390         | 
| Laptop    | HP      | 3.        | 
 
### 3. **Mérés menete**
Egymásba fűztük a modulátorokat, majd a kör végén található modulátor RF kimenetét a Spektrumanalizátorra kötöttük.
![image](https://github.com/user-attachments/assets/8945e40e-ec60-4b3a-8e85-c6fb18bc9d60)  
Két külön testre szabott RF frekvenciát választottunk a modulátorokon.(594 MHz,602 MHz), majd elneveztük Tv1 illetve Tv2 néven a csatornákat.
![image](https://github.com/user-attachments/assets/35e2eecc-25c1-4a9d-a55f-de10413d1094)  
A TV1 15Mbps-el küld, a TV2 pedig 10Mbps-el, a megadott adatok alapján.
Utána megnéztük, hogy a 2 jel hogyan viszonyul egymáshoz illetve megmértük jelszinteket, a MER-t (Modulation error), valamint a bitsebességet. Utolsó feladatként pedig a TV2 bitsebességét maxra vettük és így is megcsináltunk az előző méréseket.

## 4. Mérések eredménye, különböző bitsebességen

| RF Frekvencia (MHz) | Program neve         | Bitsebesség (Mbps) | Jelszint (dBm) | MER érték (dB) |
| ---------------- | ---------------- | -------------- | -------- | ------------------ |
| 594    | TV1      | 15         | -35.1     |  40        |
|            602      | TV2     | 10          | -29.4     | 35.4        |
|           602       | TV2 | 21.5(max)          | -29.4     | 35.4          |

---

## 5. Mérési eredmények elemzése
Az adatok alapján az alábbi következtetéseket lehet levonni:
A táblázat adatai alapján az látszik, hogy a TV1 ami a TV2-be csatlakozik majd a spektrum analizátorba veszteséges a másikhoz képest ami valószínüleg az RF kábel lehet. Illetve a TV2 10 illetve 21.5(max) bitsebessége között nincs nagy eltérés azonban a beérkező bitrátában látszott a változás.

## 6. Konklúzió
Összességében, a mérések alapján a Johansson 8202 DVB-T modulátor képes stabilan kezelni a különböző bitsebességeket, de a jelminőség és a jelszint optimalizálásához figyelembe kell venni a kábelezést. A modulátor többcsatornás működése során a bitsebesség növelése nem eredményezett drámai csökkenést a jelminőségben.
## 7. Javaslatok
A modulátorokon a feladat kezdetén mindenképpen csináljatok egy factory resetet hogy ne ütközzetek más beállításokba. Ha a spektrum analizátoron hasonló jelszintet szeretnétek mérni. Akkor a TV1-en erősíteni kell a kimeneten számolva a kábelen történő veszteséggel.

**8. Képek a mérésről**  
TV1 jele:  
![image](https://github.com/user-attachments/assets/bcca0a51-9f16-4738-a9c7-fa5851dc1297)  
![image](https://github.com/user-attachments/assets/d5af8eec-9495-4f17-a03b-5d7f99ba76fe)   
TV2 10Mbps-en:     
![image](https://github.com/user-attachments/assets/4ff9ad0f-41ee-469f-992e-fda4e0377a86)    
![image](https://github.com/user-attachments/assets/a4155048-b485-44a3-8399-da595b9d2781)      
TV2 21,5Mbps-en:  
![image](https://github.com/user-attachments/assets/713588b4-c593-43b8-931a-6f4cc7ebe845)    
![image](https://github.com/user-attachments/assets/352e420f-2312-45db-a657-82ee9c5f6940)    






</details>


<br>

**Aláírás:** Snellenperger Sándor

**Dátum:** 2024.11.27.
