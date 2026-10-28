# TVĒRUMA PĀRVALDĪBA UN DARBU SADALĪJUMA STRUKTŪRA (DSS)

**Projekts:** BackOffice sistēmas izstrāde – 1. Daļa OCPP (VMKC_Iep-12)  
**Dokuments:** Tvēruma pārvaldības plāns, tvēruma definīcija un DSS  
**Versija:** 1.0 (1. Nodevums — 50%)

---

## 1. Ievads un tvēruma pārvaldības pieeja

Tvēruma pārvaldības mērķis ir skaidri definēt visas sistēmas prasības, nodalīt produkta īpašības no veicamā darba un izveidot strukturētu darbu sadalījumu, lai nodrošinātu sekmīgu līguma izpildi un novērstu nekontrolētu tvēruma izslīdēšanu (*scope creep*).

Tvēruma plānošanas rezultātā tiek noteikta **tvēruma bāzlīnija** (apstiprināta tvēruma definīcija, darbu sadalījuma struktūra un tās vārdnīca). Jebkuras izmaiņas tvēruma bāzlīnijā ir iespējamas tikai caur formālu izmaiņu pārvaldības procesu.

---

## 2. Prasību noskaidrošana un analīze

Saskaņā ar iepirkuma tehnisko specifikāciju prasības ir iedalītas funkcionālajās, nefunkcionālajās un piegādes prasībās:

### 2.1. Funkcionālās prasības
* **PR-F1 (OCPP 2.1 sakari)**: Serverim jānodrošina pastāvīga, šifrēta reāllaika saziņa ar uzlādes stacijām, atbalstot visus bāzes ziņojumu tipus (*BootNotification, Heartbeat, StatusNotification, TransactionEvent* u.c.).
* **PR-F2 (Atpakaļsavietojamība)**: Jānodrošina hibrīda sakaru atbalsts, kas ļauj vienlaicīgi pieslēgt arī vecāku protokolu versiju stacijas (OCPP 1.6J un OCPP 2.0.1).
* **PR-F3 (Attālinātā vadība)**: Iespēja no servera nosūtīt komandas uzlādes procesa sākšanai/apturēšanai, pieslēgvietas atbloķēšanai, stacijas pārstartēšanai un konfigurācijas maiņai.
* **PR-F4 (Dinamiskie tarifi)**: Dinamiskas cenu politikas administrēšana (laika zonu tarifi, cenas atkarībā no pieprasījuma) un precīza patērētās enerģijas (kWh) maksas aprēķināšana.
* **PR-F5 (Ārējās saskarnes / API)**: Standartizēti REST API galapunkti datu apmaiņai ar ERP, CRM un viesabonēšanas (e-roaming, OCPI) platformām.

### 2.2. Nefunkcionālās un drošības prasības
* **PR-NF1 (Veiktspēja)**: Sistēmai jāspēj vienlaicīgi apkalpot vismaz 500 pieslēgtu staciju sesijas ar vidējo ziņojuma apstrādes laiku zem 200 ms.
* **PR-NF2 (Drošība)**: Datu šifrēšana sakaru kanālā, digitālo sertifikātu pārbaude un piekļuves lomu pārvaldība (administrators, operators, finanšu darbinieks).
* **PR-NF3 (GDPR atbilstība)**: Personas datu (lietotāju kontu un RFID identifikatoru) aizsardzība un iespēja dzēst vai anonimizēt datus pēc pieprasījuma.

### 2.3. Piegādes prasības
* **PR-P1 (Fiziskie datu nesēji)**: Koda un dokumentācijas nodošana notiek uz fiziska ārējā cietā diska vai USB zibatmiņas; sūtīšana mākoņpakalpojumos bez saskaņošanas ir aizliegta.

---

## 3. Tvēruma definīcija

### 3.1. Produkta tvērums pret Projekta tvērumu
* **Produkta tvērums (Ko mēs radām)**: Funkcionējoša *BackOffice* aizmugursistēma ar OCPP 2.1 sakaru moduli, PostgreSQL datubāzes shēmu, dinamisko tarifu dzinēju un integrāciju REST API.
* **Projekta tvērums (Kāds darbs jāveic)**: Visi nepieciešamie izstrādes, analīzes, arhitektūras projektēšanas, testēšanas, kļūdu labošanas un dokumentēšanas darbi 11 cilvēkmēnešu ietvaros, lai šo produktu piegādātu Pasūtītājam.

### 3.2. Tvērumā neietilpstošais (Out-of-Scope)
Lai novērstu nepareizas gaidas, tvērumā **neietilpst**:
* Gala patērētāju mobilās lietotnes vai publiskie tīmekļa portāli (tiek sagatavots tikai API to pieslēgšanai nākotnē).
* Uzlādes staciju aparatūras ražošana, uzstādīšana vai elektrisko tīklu būvdarbi.
* Banku karšu termināļu tieša fiziska uzstādīšana.

### 3.3. Produkta pieņemšanas kritēriji
Produkts tiek uzskatīts par pieņemtu, ja:
1. Ir sekmīgi izpildīti visi saskaņotie UAT testu scenāriji.
2. Sistēma demonstrē stabilu ziņojumu apmaiņu ar staciju emulatoriem.
3. Kods un dokumentācija ir ierakstīta fiziskā datu nesējā un nodota Pasūtītājam kopā ar pieņemšanas-nodošanas aktu.

---

## 4. Darbu Sadalījuma Struktūra (DSS / WBS)

Darbu sadalījuma struktūra (DSS) ir uz nodevumiem orientēta hierarhiska darbu dekompozīcija, kas balstās uz **100% likumu** (DSS ietver visu projekta darbu un tikai to darbu):

```text
1.0 Projekta pārvaldība un organizācija
    1.1 Projekta uzsākšana un Hartas izstrāde
    1.2 Projekta pārvaldības plāna integrācija
    1.3 Iknedēļas progresa uzraudzība un sanāksmes
    1.4 Izmaiņu un risku pārvaldība
    1.5 Nodevumu pieņemšanas aktu koordinācija

2.0 Sistēmas analīze un tehniskais dizains (Nodevumi M1 un M2)
    2.1 Prasību specifikācijas precizēšana
    2.2 Sistēmas augsta līmeņa arhitektūra un datu plūsmas
    2.3 Datubāzes konceptuālā un relāciju ER shēma
    2.4 Drošības mehānismu un sertifikātu pārbaudes specifikācija
    2.5 Izstrādes un testēšanas vides plāns

3.0 Sistēmas programmēšana un implementācija (Nodevumi M3 un M4)
    3.1 Reāllaika sakaru servera kodols (OCPP 2.1 bāzes ziņojumi)
    3.2 Atpakaļsavietojamības modulis (OCPP 1.6 un 2.0.1 adapteri)
    3.3 Transakciju un uzlādes sesiju uzskaites loģika
    3.4 Dinamisko tarifu un cenu aprēķinu modulis
    3.5 REST API galapunkti ārējām integrācijām (ERP / CRM / e-roaming)
    3.6 Drošības kontroles un lomu piekļuves (RBAC) ieviešana

4.0 Kvalitātes nodrošināšana, testēšana un nodošana (Nodevums M4)
    4.1 Vienību un integrācijas testēšana
    4.2 Veiktspējas un slodzes pārbaudes (500+ staciju jauda)
    4.3 Drošības un ievainojamību audits
    4.4 Lietotāju akcepttests (UAT) kopā ar Pasūtītāju
    4.5 Tehniskā dokumentācija, API apraksti un lietotāja instrukcija
    4.6 Koda un materiālu fiziska nodošana USB/HDD datu nesējā
```

---

## 5. Darba pakotņu skaidrojums (DSS Vārdnīca)

* **DP 2.2 Sistēmas augsta līmeņa arhitektūra (Nodevums M1)**:  
  Apraksta sistēmas galvenās komponentes, to savstarpējo mijiedarbību un datu plūsmu no uzlādes stacijas līdz datubāzei un ārējām sistēmām.
* **DP 2.3 Datubāzes shēma (Nodevums M2)**:  
  Definē tabulu struktūru staciju konfigurāciju, pieslēgvietu, transakciju, lietotāju un audita žurnālu glabāšanai PostgreSQL vidē.
* **DP 3.1 Reāllaika sakaru serveris (Nodevums M3)**:  
  Programmatūras modulis, kas uztur šifrētas reāllaika sesijas ar stacijām, saņem statusus un apstrādā pamata komandas.
* **DP 3.4 Dinamisko tarifu modulis (Nodevums M4)**:  
  Sistēmas loģika, kas ļauj operatoram definēt laika un jaudas tarifus un automātiski aprēķina maksu par patērētajām kilovatstundām.
* **DP 4.4 Lietotāju akcepttests (UAT)**:  
  Kopīga sistēmas verifikācija ar Pasūtītāju pēc iepriekš definētiem scenārijiem pirms galīgā pieņemšanas akta parakstīšanas.
* **DP 4.6 Fiziskā nodošana**:  
  Pirmkoda un dokumentācijas sagatavošana, kontrolsummu (SHA-256) pārbaude un fiziska nodošana USB/HDD nesējā.

---

## 6. Tvēruma bāzlīnija un izslīdēšanas (Scope Creep) kontrole

* **Tvēruma pamatlīmenis**: Veido šī dokumenta prasību saraksts un DSS struktūra.
* **Tvēruma izslīdēšanas novēršana**: Nekontrolētas izmaiņas netiek pieļautas. Ja Pasūtītājs vai izstrādes komanda ierosina papildu funkcijas, tās tiek virzītas caur Izmaiņu pārvaldības kārtību, izvērtējot ietekmi uz 11 cilvēkmēnešu resursiem un gala termiņu (2025. gada 30. septembris).
