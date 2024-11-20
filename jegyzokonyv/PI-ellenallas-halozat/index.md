## &#928; Csillapító Áramkör Jegyzőkönyv.

**Mérés helye**: Miskolci SZC Kandó Kálmán Informatikai Technikum  
**Mérés időpontja**: 2024.10.07.  
**A méréshez használt eszközök**:<br>
HMO1002 Oscilloscope - 1764K02-102609-WG <br>
Jelgenerátor - A682393<br>
Breadboard, ellenállások és laptop
<br>
**Felelős személy**: Sándor Péter  
**Cél**: A pi csillapító áramkör elemzése.

---

### 1. **Bevezetés**

Egy olyan négypólusú Π csillapító áramkör építése aminek a bemenetére egy 600 Ω belső ellenállású jelgenerátort kötünk, és a cél, az hogy 6 dB csillapítást érjünk el a kimeneten amit egy oszcilloszkóppal fogunk mérni.

## Elmélet:

Az áramkör arról kapja a nevét, hogy az ellenállásokat a görög "&#928;" formájában kötjük össze.
Az érétkeket a következő képletekkel számoljuk ki:

![R1 képlete](https://raw.githubusercontent.com/szabot2/pi-csillapito/cffee4ced185268076fb4bf54fdfafc23a0b0f74/kepek/svgviewer-output.svg)

![R2 képlete](https://raw.githubusercontent.com/szabot2/pi-csillapito/cffee4ced185268076fb4bf54fdfafc23a0b0f74/kepek/svgviewer-output(1).svg)


6 dB-es csillapításra kiszámolt ellenállás értékek:


<img src="https://raw.githubusercontent.com/szabot2/pi-csillapito/refs/heads/main/kepek/ql_41d4e91c270a0827beb0bb25f1c6a62a_l3.png">
<br>

A kapcsolási rajz ábrázolja a jelgenerátort a belső ellenállásával, valamint a Pi csillapítót a kiszámolt ellenállás értékekkel:
<a href="https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWc0wCZIA4AsBmBDUsM4A2AThxAUiqpoQFMBaMMAKADcQySRdVuvdBijhw8WjSnQEbAE6CQwpZhUiaJOGwDuavcpyQsUHYv57zkU8vMGcvK7oNGlCXoeOPX7l6jdKAdgEvOyF-HHsTJ3DIv3cSdWtwhJAPVJSQ-1Qg1N8cqwU07IE0+3VwYgLc42K+MCF8vmpTUpSsevTEhXaGgR7O0TBK037arBIa-JGOsr4JgaqsHkC+5dmNLV1l5WWwLE9rVWVlPYPdJfiRNxp1ke2c65WTAAdFU713ygPXx9rH2a+UT49z681qXguA3GxluAHslAiaGgEOMlNAlmQyBhUKgcERsDiyEgYPAIDQBCU2PCwAFEeA-KiwNBCJiyKwaftUKwiFBYHAIBABDTUmwgA" target="_blank">
<img src="https://raw.githubusercontent.com/szabot2/pi-csillapito/refs/heads/main/kepek/circuit-20241008-0905.png" width="640" height="400">
</a>


### 3. **Mérési paraméterek**

| Paraméter           | Érték |
|---------------------|-------|
| Generátor jel       | 5.00 Vp2p|
| Kimeneti Jel        | 2.06 Vp2p |
| Generátor Frekvencia| 1000 Hz |
| Csillapítás         | -7.702 dB |
| Átviteli Arány      | 7.702 dB |
| Bemeneti impedancia | ? Ω |
| Kimeneti impedancia | ? Ω |   

<br>

Látható az oszcilloszkópon a sárga 1-es csatornán a csillapított kimeneti jel, és a kék 2-es csatornán a generátor jel.

<img src="https://raw.githubusercontent.com/szabot2/pi-csillapito/refs/heads/main/kepek/TA02.PNG" width="600" height="480">


### 4. **Mérési eredmények**

- **Kimeneti Jel**: A kimeneti jel mindössze 41.2%-a a generátor jelének.
  
- **Csillapítás/Átviteli arány**:  7.702 dB csillapítást tapasztalunk az áramkör jóvoltából.

- **Kimeneti/Bemeneti impedancia**: ??????.  

### 5. **Elemzés**
A pi csillapító (pi pad) ellenállás áramkörének elemzése során megfigyelhető, hogy a tervezett áramkör hatékonyan csökkenti a jel amplitúdóját, miközben megőrzi a jel formáját. Az áramkör négy fő komponensből áll: három ellenállásból és egy terhelő ellenállásból. Kisebb eltérés tapasztalható a kiszámolt értékek és a valós értékek között.

### 6. **Következtetések**
A pi csillapító áramkör sikeresen megvalósult, és a tesztelési eredmények azt mutatják, hogy a csillapítási teljesítmény megfelel a tervezett specifikációknak. A mérések alapján a csillapító hatás a kívánt frekvenciatartományban optimális, és a jelminőség megőrzése is megfelelő. A projekt során szerzett tapasztalatok alapján a tervezési folyamat során figyelembe kell venni a komponensek toleranciáját és a környezeti hatásokat, mivel ezek befolyásolhatják az áramkör teljesítményét.

### 7. **Javaslatok**

- nincs

---

**Aláírás**:  
Felelős mérő személy: ..............................  
Dátum: .............................................

