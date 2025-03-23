# Stiilijuhend GitHubis arendatavate õppematerjalide ühtlustamiseks

Juhendi eesmärk on ühtlustada visuaalset ja tehnilist esitlusstiili, et materjalid oleksid loetavad, järjepidevad ja kergesti kasutatavad nii õppijatele kui ka kaasautoritele.

---

## Sisukord

- [1. Failistruktuur ja nimekonventsioonid](#1-failistruktuur-ja-nimekonventsioonid)
- [2. Pealkirjade kasutus](#2-pealkirjade-kasutus)
- [3. Teksti vormindamine](#3-teksti-vormindamine)
- [4. Pildid ja joonised](#4-pildid-ja-joonised)
- [5. Siselingid ja navigeerimine](#5-siselingid-ja-navigeerimine)
- [6. Märkused, hoiatused ja täiendused](#6-märkused-hoiatused-ja-täiendused)
- [7. LaTeX ja matemaatilised avaldised](#7-latex-ja-matemaatilised-avaldised)
- [8. Tabeli koostamine](#8-tabeli-koostamine)
- [9. Esitlusstiil](#9-esitlusstiil)
- [10. Hea praktika ja tüüpilised vead](#10-hea-praktika-ja-tüüpilised-vead)
- [11. Soovituslikud töövahendid](#11-soovituslikud-töövahendid)

## 1. Failistruktuur ja nimekonventsioonid

Soovitsulikku failistruktuuri kirjeldab [õppevara mall](https://github.com/nullyks/oppevara-mall), mida on mõistlik võtta uue materjali aluseks.

Kõik sisumaterjalid paiknevad kaustas `materjalid/`. See loob arusaadava struktuuri ja eraldab need muudest failidest nagu `README.md` ja `LICENSE`.
Mediafailid asuvad kausta `materjalid/` alamkastas `meedia/`.

Iga teema või alateema esitatakse eraldi MarkDowni (`.md`) failina, mis võimaldab teemade kaupa navigeerimist ja jagamist.

Failinimed peaksid olema kirjeldavad ja masinloetavad: väldi täpitähti ja tühikuid, kasuta sidekriipse.

**Soovituslik vorming:** `X_teema-nimi.md`, kus `X` on järjekorranumber.

**Näide:**
```
materjalid/
├── 1_Sissejuhatus-Arduinosse.md
├── 2_LED-i-uhendamine.md
├── 3_Takisti-toole.md
```

---

## 2. Pealkirjade kasutus

Kasutatakse MarkDowni pealkirjatasemeid vastavalt sisuloogikale:

- `#` – üldpealkiri 
- `##` – teema või faili põhisisu pealkiri
- `###` – jaotised alateema sees (nt komponendid, ühendamine, kood)
- `####` – täiendavad alamjaotused, kui vajalik

**Näide:**
```markdown
## LED-i ühendamine

### Vajalikud komponendid
- LED
- Takisti (220 Ω)

### Ühendusskeem
(joonis või kirjeldus)
```

Ära kasuta mitut `#` järjest lihtsalt esteetika pärast. Iga tase olgu tähendusega ja loogiliselt üles ehitatud.

---

## 3. Teksti vormindamine

**Rõhutamine:**
- `**paks kiri**` – oluline termin; ei tohiks kasutada liiga palju.
- *`*kursiiv*`* - terminid inglise keeles ja allikad. Ka sellega tuleb olla ettevaatlik, sest kursiiv ei ole sageli väga hästi loetav.

**Kood:**
- \``tekstisisene kood`\` – kui viitad funktsioonidele või muutujatele teksti sees: `digitalWrite()`
- Pikema koodinäite puhul eraldi koodiblokk:

```markdown
~~~cpp
void setup() {
  pinMode(13, OUTPUT);
  digitalWrite(13, HIGH);
}
~~~
```
Näeb välja nii:
~~~cpp
void setup() {
  pinMode(13, OUTPUT);
  digitalWrite(13, HIGH);
}
~~~

**NB!** *backtick* sümbol " \` "  on eesti asetusega klaviatuuril raskesti leitav. Tekstisisese koodibloki puhul pole see asendatav kuid eraldi koodibloki puhul on mugavam kasutada kolmekordse *backtick* sümboli asemel kolmekordset *tilde* sümbolit. 

**Loetelud:**
- Numbriline loetelu juhiste jaoks:
  1. Ühenda LED takistiga.
  2. Ühenda takisti GND-ga.
- Täppidega loetelu komponentide või omaduste jaoks:
  - LED
  - Takisti

Markdownis tähistavad nii * (tärn) kui - (kriips) punktloetelu algust – funktsionaalselt on need täiesti võrdsed. Mõlemad tekitavad täppidega loetelu ja renderdus on identne.

---

## 4. Pildid ja joonised

Pildid paigutatakse alamsisestesse kaustadesse nagu `materjalid/meedia/`. Kasuta **suhtelisi linke**, et tagada pildi kuvamine ka GitHubis:

```markdown
![LED skeem](meedia/led-uhendus.png)
```

Soovitav on kasutada **väiksemaid ja optimeeritud PNG** või **SVG-faile**, et tagada kiire laadimine ja hea kvaliteet.

---

## 5. Siselingid ja navigeerimine

**Failide vahelised lingid:**

```markdown
[Loe edasi takisti kohta](3_Takisti-toole.md)
```

**Pealkirjadele hüppamine samas failis:** (pealkirjad teisendatakse GitHubis automaatselt ankruteks)

```markdown
[Vaata komponentide nimekirja](#vajalikud-komponendid)
```

---

## 6. Märkused, hoiatused ja täiendused

Kasuta `>` blockquote vormingut, et esile tõsta lisainfot või ohte:

```markdown
> **NIPP:** LED-l on polaarsus – pikem jalg on anood.

> **HOIATUS:** Vale ühendus võib rikkuda LED-i või pordi.
```

---

## 7. LaTeX ja matemaatilised avaldised

GitHub toetab LaTeX-i laadseid süntakse mitte otse, vaid ainult piiratud kujul läbi MathJaxi teegi.

**Plokiaavaldis (kogu valem eraldi reale):**
```markdown
$$
R = \frac{U}{I}
$$
```

Näeb välja nii:
$$
R = \frac{U}{I}
$$

**Tekstisisene avaldis:**
```markdown
Takisti väärtus arvutatakse valemiga $R = \frac{U}{I}$.
```
Näeb välja nii:

Takisti väärtus arvutatakse valemiga $R = \frac{U}{I}$.



**NB!** Kui kasutad GitHubi failivaadet, siis valemid ei renderdu.

[Kasulikke näiteid](https://jojozhuang.github.io/tutorial/mathjax-cheat-sheet-for-mathematical-notation/)

---

## 8. Tabeli koostamine
Markdownis tabeli koostamine käib vertikaaljoonte (|) ja sidekriipsude (-) abil. 
- Esimene rida – veeru pealkirjad
- Teine rida – veeru eraldaja, vähemalt 3 sidekriipsu (---)
- Lahtrid eraldatakse vertikaaljoontega |
- Veergude joondust saab kontrollida koolonite abil:

Joonduse süntaks:
- Vasakult	:---
- Paremalt	---:
- Keskelt	:---:

Näiteks:

~~~markdown

| Komponent      | Kirjeldus                 | Märkused               |
|:---------------|:-------------------------:|------------------------:|
| LED            | Valgusdiood               | Kontrolli polaarsust   |
| Takisti        | Piirab voolu LED-is       | Nt 220 Ω või 330 Ω     |
| Arduino UNO    | Mikrokontrollerplaat      | Toidetakse USB kaudu   |
~~~~

Näeb välja nii:

| Komponent      | Kirjeldus                 | Märkused               |
|:---------------|:-------------------------:|------------------------:|
| LED            | Valgusdiood               | Kontrolli polaarsust   |
| Takisti        | Piirab voolu LED-is       | Nt 220 Ω või 330 Ω     |
| Arduino UNO    | Mikrokontrollerplaat      | Toidetakse USB kaudu   |

## 9. Esitlusstiil

Kirjastiil olgu **konkreetne, juhendav ja õppijasõbralik**. Väldi pikki lohisevaid seletusi enne praktilisi samme.

Kasuta **käskivat kõneviisi**:
- "Ühenda LED takistiga..."
- "LED tuleks ühendada takistiga..." (vältida)

Uued mõisted tuleks lühidalt selgitada esmakordsel kasutamisel:
> PWM (impulsslaiusmodulatsioon) võimaldab reguleerida LEDi eredust.

Kasuta küsimusi või tegevuspõhiseid üleskutseid: "Mõtle, kuidas vool liigub skeemis..."

---

## 10. Hea praktika ja tüüpilised vead

| Viga                                  | Parandus                                       |
|--------------------------------------|------------------------------------------------|
| Kasutatakse ainult `#` kõikjal       | Kasuta `##`, `###` sisulise struktuuri jaoks   |
| Kood esitatakse tavalise teksti sees | Kasuta ```cpp ... ``` koodiplokki               |
| Puuduvad pildid või katkised lingid  | Kontrolli, et failitee oleks suhteline ja korrektne |
| Ebajärjekindlad failinimed           | Kasuta "X_teema-nimi.md" formaati               |

---

## 11. Soovituslikud töövahendid


| Kategooria              | Vahend                                                                 | Kirjeldus ja soovitus                                                                 |
|-------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Tekstiredaktorid**    | [Visual Studio Code](https://code.visualstudio.com/)                  | Laiendatav töövahend MarkDowni, Git-i ja GitHubi haldusega. Sobib nii õpetajatele kui arendajatele. |
|                         | [Typora](https://typora.io/) *(tasuline)*                              | Visuaalne WYSIWYG MarkDown-redaktor, väga lihtne kasutada. Sobib mittetehnilistele kasutajatele.         |
|                         | [MarkText](https://marktext.app/)                                     | Avatud lähtekoodiga visuaalne MarkDowni redaktor. Hea alternatiiv Typorale.                                |
|                         | [Obsidian](https://obsidian.md/)                                      | Märkmepõhine MarkDowni töövahend, sobib õppematerjalide sisuloomeks ja isiklikeks märkmeteks.             |
|                         | Tavaline tekstiredaktor (nt Notepad++, Kate)                          | Võimalik kasutada, kui eelistad lihtsust.                                            |
| **Git/GitHub tööriistad** | [GitHub Desktop](https://desktop.github.com/)                        | Lihtsustatud graafiline liides GitHubi haldamiseks – sobib algajatele.                                    |
|                         | [GitKraken](https://www.gitkraken.com/)                               | Visuaalne Git-kliendi rakendus, sobib keerukamate projektide haldamiseks.                                 |
|                         | [Git](https://git-scm.com/) käsurealt                                 | Võimas ja paindlik, vajalik edasijõudnud kasutajale või töövoo automatiseerimiseks.                              |
| **Markdown eelvaade ja testimine** | VS Code laiendus „Markdown Preview Enhanced“             | Reaalajas eelvaade koos LaTeX toe ja diagrammide toega.                                                    |
|                         | [Dillinger](https://dillinger.io/)                                    | Veebipõhine MarkDown-redaktor eelvaatega, sobib kiireks katsetamiseks.                                     |
| **LaTeX ja valemid**    | [MathJax](https://www.mathjax.org/)                                   | LaTeX-i renderdamise mootor.                          |
|                         | [KaTeX](https://katex.org/)                                           | Kiirem ja kergem alternatiiv MathJaxile.                                 |
| **Diagrammid ja joonised** | [draw.io / diagrams.net](https://app.diagrams.net/)               | Intuitiivne skeemide joonistamine. Salvestab pilte otse `.png` kujul.                                      |
|                         | [Mermaid.js](https://mermaid.js.org/)                                 | MarkDowni sees kirjutatavad skeemid (nt järjestus-, voog-, olekudiagrammid). Toetatud GitHubis ja VS Code’is.   |
| **Koodijupid ja testimine** | [Arduino IDE](https://www.arduino.cc/en/software)                | Vajalik Arduino näidete testimiseks ja käivitamiseks.                                                      |
|                         | [Tinkercad Circuits](https://www.tinkercad.com/circuits)              | Visuaalne Arduino simulaator ja skeemide joonistaja. Hea õppematerjalide illustreerimiseks.               |
|                         | [Falstad Circuit Simulator](https://falstad.com/circuit/circuitjs.html) | Veebipõhine interaktiivne vooluringide simulaator. Sobib elektroonikaalaste põhimõistete õpetamiseks ja katsetamiseks. |
