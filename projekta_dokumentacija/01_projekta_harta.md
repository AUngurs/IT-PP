# PROJEKTA HARTA (PROJECT CHARTER)

| Projekta nosaukums: | BackOffice sistēmas izstrāde – 1. Daļa OCPP |
|:---|:---|
| **Iepirkuma identifikators:** | VMKC_Iep-12 |
| **Pētniecības projekta Nr.:** | 2.2.1.3.i.0/1/24/A/CFLA/004 |
| **Pasūtītājs (Sponsors):** | SIA "PC Consulting" (Valdes loceklis Ģirts Aleksāns) |
| **Sadarbības partneris:** | SIA "VTKC" (Viedo materiālu kompetences centrs) |
| **Izpildītājs:** | Izstrādātājs (Galvenā IT izstrādes speciālistu grupa) |
| **Projekta vadītājs:** | Izstrādātāja Projekta Vadītājs (e-pasts: pm@izstradatajs.lv) |
| **Apstiprināšanas datums:** | 2025. gada 5. maijs |
| **Plānotais ilgums:** | 2025. gada 5. maijs – 2025. gada 30. septembris |
| **Budžeta bāzlīnija:** | 89 450.00 EUR (bez PVN) / 108 234.50 EUR (ar PVN 21%) |
| **Dokumenta statuss:** | Bāzlīnija (1. Nodevums — 50%) |

---

## 1. Pamatinformācija

### 1.1. Biznesa pamatojums un projekta nolūks
Projekts tiek īstenots CFLA un Eiropas Atveseļošanas fonda pētniecības aktivitātes **“Videi draudzīgas elektroauto uzlādes ekosistēmas prototipa izstrāde, integrējot atjaunojamos energoresursus un elektrotīkla balansēšanu”** ietvaros. 

Mūsdienīgai e-mobilitātes infrastruktūrai nepieciešama vadības sistēma (*BackOffice* / CSMS), kas spēj uzturēt pastāvīgus sakarus ar uzlādes stacijām. Pašreizējie risinājumi balstās uz vecākiem protokoliem (OCPP 1.6), kuriem trūkst mūsdienīgu drošības mehānismu un dinamiskas enerģijas vadības. Šī projekta nolūks ir izstrādāt jaunas paaudzes servera programmnodrošinājumu, kas ievieš **OCPP 2.1** standartu un nodrošina gatavību elektrotīkla balansēšanai un viedajai uzlādei.

### 1.2. Mērāmi mērķi un veiksmes kritēriji (SMART)
1. **Funkcionālā gatavība**: Izstrādāt aizmugursistēmu, kas nodrošina pilnu OCPP 2.1 bāzes ziņojumu apmaiņu (*BootNotification, StatusNotification, TransactionEvent, Heartbeat* u.c.) un uztur atpakaļsavietojamību ar OCPP 1.6 un 2.0.1 stacijām.
2. **Veiktspēja un mērogojamība**: Nodrošināt stabilu darbību vismaz 500 vienlaicīgām staciju sesijām ar vidējo ziņojuma atbildes laiku zem 200 ms.
3. **Drošība un atbilstība**: Ieviest šifrētu datu pārraidi, digitālo sertifikātu pārbaudi un piekļuves lomu pārvaldību atbilstoši GDPR prasībām.
4. **Termiņa un izmaksu izpilde**: Pabeigt visus līguma darbus 11 cilvēkmēnešu (~1760 stundu) apjomā un nodot gala rezultātu līdz **2025. gada 30. septembrim**.

---

## 2. Saturiskā daļa

### 2.1. Produkta un pakalpojuma raksturojums (Produkta tvērums)
Sistēma ir centrālais sakaru un vadības mezgls starp elektroauto uzlādes stacijām un operatora ārējām sistēmām:
* **Sakaru serveris**: Uztur reāllaika šifrētus savienojumus ar uzlādes stacijām.
* **Darījumu un tarifu modulis**: Uzskaita uzlādes sesijas, patērētās kilovatstundas un aprēķina maksu pēc dinamiskajiem tarifiem.
* **Datu bāze**: Glabā informāciju par stacijām, pieslēgvietām, RFID lietotājiem un notikumu žurnāliem.
* **Integrācijas saskarnes (API)**: Nodrošina standartizētus REST galapunktus datu apmaiņai ar ERP, CRM un viesabonēšanas (e-roaming) platformām.

### 2.2. Projekta tvēruma robežas
* **Ietilpst projekta tvērumā**: Servera koda izstrāde, datubāzes shēma, dinamiskie tarifi, drošības kontrole, API integrācijas, testēšana un tehniskā dokumentācija.
* **Neietilpst projekta tvērumā**: Gala lietotāju mobilās lietotnes, publiski tīmekļa portāli, staciju fiziskā ražošana, uzstādīšana dabā un elektrības pieslēgumu būvniecība.

### 2.3. Projekta īstenošanas pieeja
Tiek izmantota **hibrīda pieeja**:
* Pārvaldības un līguma līmenī tiek piemērots plānveida modelis ar 4 stingri fiksētām šķirtnēm un pieņemšanas aktiem.
* Izstrādes komandas iekšienē tiek izmantota adaptīva pieeja ar 2 nedēļu sprintiem un regulāru starprezultātu demonstrēšanu.

### 2.4. Nozīmīgākās projekta šķirtnes (Milestones)

Šķirtnes ir projekta nozīmīgākie atskaites punkti ar ilgumu 0, kas piesaistīti konkrētiem līguma nodevumiem:

| Šķirtne | Plānotais datums | Saistītais nodevums un saturs |
|:---|:---:|:---|
| **Š-1: Arhitektūra un koncepcija** | **31.05.2025.** | Augsta līmeņa arhitektūras shēma, datu plūsmas apraksts un prasību specifikācija. |
| **Š-2: Tehniskais dizains un drošība** | **30.06.2025.** | Detalizēta datubāzes shēma, drošības prasību apraksts un testēšanas vides plāns. |
| **Š-3: Bāzes prototips** | **31.08.2025.** | Darbspējīgs OCPP 2.1 prototips, datubāzes integrācija un vienību testu atskaites. |
| **Š-4: Gala sistēmas pieņemšana** | **30.09.2025.** | Pilns OCPP 2.1 un tarifu modulis, API, slodzes testi, UAT akcepts un gala nodošana USB/HDD. |

### 2.5. Būtiskākie pieņēmumi un ierobežojumi
1. **Pieņēmums par pārbaudes laiku**: Pasūtītājs veic nodevumu izvērtēšanu 20 darba dienu laikā no iesniegšanas brīža.
2. **Fiziska materiālu nodošana**: Saskaņā ar iepirkuma nolikumu, koda un dokumentācijas nodošana notiek fiziskos datu nesējos (ārējais HDD vai USB zibatmiņa). Datu izvietošana publiskos mākoņos bez saskaņošanas ir aizliegta.
3. **Sankciju atbilstība**: Projektā iesaistītie speciālisti atbilst ES Regulai Nr. 833/2014 un LR normatīvajiem aktiem par sankciju ievērošanu.
4. **Intelektuālais īpašums**: Viss jaunradītais pirmkods un dokumentācija pēc gala norēķina pāriet Pasūtītāja īpašumā.

### 2.6. Nozīmīgākie riski (Augsta līmeņa)
* Dažādu staciju ražotāju atšķirīga OCPP 2.1 interpretācija (risinājums: konfigurējams protokola validācijas slānis).
* Laika grafika saspringtība (11 cilvēkmēneši jārealizē 5 kalendārajos mēnešos; risinājums: 4 speciālistu paralēls darbs un stingra sprintu disciplīna).
* Līgumsoda risks par kavējumu (0,2% par katru nokavēto dienu; risinājums: 1–2 nedēļu laika rezerves pirms oficiālajām šķirtnēm).

---

## 3. Lomas, atbildība un pilnvarojums

* **Projekta sponsors (Pasūtītājs)**: Nodrošina finansējumu, apstiprina projekta hartu, pieņem starpposmu un gala nodevumus, lemj par līguma izmaiņām.
* **Projekta vadītājs (Izstrādātājs)**: Pilnvarots operatīvi vadīt 4 speciālistu komandu, rīkoties ar piešķirto darba laika budžetu, organizēt ikdienas izstrādi un pārstāvēt komandu iknedēļas sanāksmēs ar Pasūtītāju.

---

## 4. Apstiprinājums

Ar šo parakstu puses apliecina vienošanos par projekta mērķiem, tvērumu, šķirtnēm un budžeta ietvaru:

| Pasūtītāja (Sponsora) vārdā: | Izpildītāja (Projekta vadītāja) vārdā: |
|:---|:---|
| **SIA "PC Consulting"** | **Izstrādātāja komanda** |
| Valdes loceklis Ģirts Aleksāns | Projekta vadītājs |
| Paraksts: _________________________ | Paraksts: _________________________ |
| Datums: 2025. gada 5. maijā | Datums: 2025. gada 5. maijā |
