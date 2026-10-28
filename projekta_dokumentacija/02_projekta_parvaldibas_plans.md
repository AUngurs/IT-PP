# PROJEKTA PĀRVALDĪBAS PLĀNS

**Projekts:** BackOffice sistēmas izstrāde – 1. Daļa OCPP (VMKC_Iep-12)  
**Dokuments:** Programmatūras projekta pārvaldības plāns  
**Struktūras pamats:** LVS 67:1996 (ANSI/IEEE Std 1058.1) vadlīnijas  
**Versija:** 1.0 (1. Nodevums — 50%)

---

## 1. Ievads

### 1.1. Projekta pārskats
Projekta pārvaldības plāns nosaka, kā projekts tiks izpildīts, uzraudzīts, kontrolēts un noslēgts. Projekta mērķis ir izstrādāt centrālo aizmugursistēmu (*BackOffice* / CSMS) elektroauto uzlādes staciju uzraudzībai un vadībai, izmantojot starptautisko OCPP 2.1 protokolu. Darbs tiek veikts CFLA pētniecības projekta Nr. `2.2.1.3.i.0/1/24/A/CFLA/004` ietvaros.

### 1.2. Galvenie nodevumi
Projekta gaitā Pasūtītājam tiek piegādāti četri oficiāli starpposmu nodevumi:
* **Nodevums 1 (M1)**: Sistēmas augsta līmeņa arhitektūra, datu plūsmu apraksts un prasību specifikācija.
* **Nodevums 2 (M2)**: Detalizēta datubāzes shēma, drošības prasību apraksts un testēšanas vides plāns.
* **Nodevums 3 (M3)**: Darbspējīgs bāzes prototips ar reāllaika OCPP 2.1 ziņojumu apmaiņu un testu atskaitēm.
* **Nodevums 4 (M4)**: Pilna sistēma ar dinamiskajiem tarifiem, integrāciju API, veiktspējas testiem, lietotāju akcepttestu (UAT) un tehnisko dokumentāciju.

### 1.3. Saistība ar citiem dokumentiem
Šis plāns integrē un saskaņo pārējos vadības dokumentus:
* **Projekta harta** (`01_projekta_harta.md`) — augstākais pilnvarojuma dokuments.
* **Tvēruma pārvaldības plāns un DSS** (`03_tveruma_parvaldiba_dss.md`) — prasības un darbu struktūra.
* **Grafika un termiņu plāns** (`04_grafika_un_terminu_plans.md`) — aktivitātes un laika bāzlīnija.
* **Finanšu un izmaksu plāns** (`05_finansu_un_izmaksu_plans.md`) — darbietilpība un izmaksu bāzlīnija.

---

## 2. Projekta organizācija

### 2.1. Procesa modelis (Hibrīda pieeja)
Projektā tiek apvienotas divas pieejas:
1. **Plānveida pieeja (līguma līmenī)**: Līguma izpildes kontrole balstās uz četriem fiksētiem atskaites punktiem (šķirtnēm) un formāliem pieņemšanas-nodošanas aktiem.
2. **Adaptīvā pieeja (izstrādes komandas līmenī)**: Koda programmēšana un testēšana notiek **2 nedēļu sprintos**. Tas ļauj ātri atklāt nepilnības, demonstrēt starprezultātus un elastīgi pielāgot darbus sprintu iekšienē.

### 2.2. Organizatoriskā struktūra un personāls
Projektu īsteno 4 speciālistu komanda ar kopējo kapacitāti 11 cilvēkmēneši (~1760 stundas):
* **Projekta vadītājs / Sistēmu arhitekts (350 h)**: Atbild par projekta pārvaldību, integrēto plānošanu, arhitektūras lēmumiem un komunikāciju ar Pasūtītāju.
* **Vadošais izstrādātājs (650 h)**: Atbild par servera kodola programmēšanu, OCPP 2.1 ziņojumu loģiku, datubāzi un API saskarnēm.
* **Drošības un tīklu inženieris (380 h)**: Atbild par sakaru šifrēšanu, digitālo sertifikātu pārbaudi un piekļuves lomu kontroli.
* **Testēšanas (QA) inženieris (380 h)**: Atbild par testu automatizāciju, staciju emulatoriem, slodzes mērījumiem un UAT sagatavošanu.

### 2.3. Lēmumu pieņemšanas kārtība un eskalācija
* **Ikdienas operatīvie lēmumi**: Tehniskos un izstrādes jautājumus sprintu ietvaros patstāvīgi pieņem Izstrādātāja komanda un projekta vadītājs.
* **Līguma līmeņa lēmumi**: Jautājumi, kas skar termiņu izmaiņas, budžeta pārdali vai atkāpes no tehniskās specifikācijas, tiek nekavējoties eskalēti Pasūtītāja valdes loceklim Ģirtam Aleksānam kopīga lēmuma pieņemšanai.

---

## 3. Pārvaldības process

### 3.1. Pārvaldības mērķi un prioritātes
Galvenā prioritāte ir nodrošināt kvalitatīvu un stabilu aizmugursistēmu, iekļaujoties nolikuma noteiktajā termiņā (līdz 2025. gada 30. septembrim) un budžetā, saglabājot 100% izsekojamību atbilstoši CFLA pētniecības projekta prasībām.

### 3.2. Pārraudzības un kontroles mehānismi
* **Iknedēļas statusa sanāksmes**: Katru ceturtdienu plkst. 15:00 notiek darba sanāksme starp Izstrādātāja projekta vadītāju un Pasūtītāja pārstāvi par sprinta progresu un aktuālajiem jautājumiem.
* **Uzdevumu un kļūdu reģistrācija**: Izmantots vienots rīks (JIRA), kur katrs uzdevums ir piesaistīts darbu sadalījuma struktūras (DSS) kodam.
* **10–15% noviržu slieksnis**: Ja faktiskais darba stundu patēriņš vai grafiks novirzās vairāk nekā par 10%, projekta vadītājs sagatavo rakstisku korektīvo pasākumu plānu.

### 3.3. Izmaiņu pārvaldības kārtība
Jebkura izmaiņa projekta tvērumā vai prasībās tiek apstrādāta formālā kārtībā:
1. **Pieteikums**: Ierosinātājs sagatavo izmaiņu pieprasījumu ar pamatojumu.
2. **Novērtējums**: Izstrādātājs 3 darba dienu laikā novērtē ietekmi uz grafiku, darbietilpību un izmaksām.
3. **Saskaņošana**: Ja izmaiņa prasa līguma grozījumus, tā stājas spēkā tikai pēc abu pušu rakstiskas vienošanās parakstīšanas.

---

## 4. Tehniskais process

### 4.1. Izstrādes metodes un rīki
* **Tehnoloģiju bāze**: Servera kodols veidots, izmantojot *Node.js (TypeScript)* ar reāllaika asinhronu ziņojumu apstrādi.
* **Datu glabāšana**: Relāciju datubāze *PostgreSQL* transakcijām un staciju konfigurācijām, papildināta ar *Redis* reāllaika sesiju stāvokļiem.
* **Konteinerizācija**: *Docker* un *Docker Compose* vienkāršotai sistēmas palaišanai un uzturēšanai.

### 4.2. Vides un koda pārvaldība
Tiek uzturētas trīs izolētas vides:
* **Izstrādes vide (Dev)**: Komandas ikdienas darbam un vienību testiem.
* **Testēšanas vide (Test / Staging)**: Integrācijas testiem ar staciju emulatoriem un slodzes pārbaudēm.
* **Gala vide (Demo / Prod)**: UAT pieņemšanas testiem kopā ar Pasūtītāju.

Koda versiju kontrole tiek veikta Git vidē. Gatavie nodevumi un kods tiek eksportēti un nodoti Pasūtītājam fiziskos datu nesējos (ārējais cietais disks vai USB zibatmiņa).

---

## 5. Bāzlīniju integrācija

Projekta pārvaldības plāns apvieno un fiksē trīs galvenās bāzlīnijas:
1. **Tvēruma bāzlīnija**: Apstiprināta tvēruma definīcija un Darbu sadalījuma struktūra (DSS) ar vārdnīcu.
2. **Grafika bāzlīnija**: Apstiprināts kalendārais plāns ar 4 oficiālajām šķirtnēm un 10 sprintu grafiku.
3. **Izmaksu bāzlīnija**: Apstiprināts budžeta sadalījums pa laika periodiem (mēnešiem) un lomām.

Izmaiņas šajās bāzlīnijās ir pieļaujamas tikai caur formālu izmaiņu pārvaldības procesu.
