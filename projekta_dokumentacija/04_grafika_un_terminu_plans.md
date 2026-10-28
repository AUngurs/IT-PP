# GRAFIKA UN TERMIŅU PĀRVALDĪBAS PLĀNS

**Projekts:** BackOffice sistēmas izstrāde – 1. Daļa OCPP (VMKC_Iep-12)  
**Dokuments:** Grafika un laika pārvaldības plāns  
**Versija:** 1.0 (1. Nodevums — 50%)

---

## 1. Grafika vadības pamatprincipi

Grafika pārvaldības mērķis ir nodrošināt, ka visas aktivitātes un nodevumi tiek izpildīti nolikuma noteiktajā termiņā — no 2025. gada maija sākuma līdz **2025. gada 30. septembrim**.

Projekta laika plānošanā tiek nodalīti divi jēdzieni:
* **Darbietilpība**: Ieguldītais darba apjoms, kas noteikts **11 cilvēkmēneši** (~1760 cilvēkstundas).
* **Ilgums**: Kalendārais laiks darbu veikšanai — **5 mēneši** (aptuveni 21 kalendārā nedēļa).

Grafika uzticamība atbilst nozares pārbaudes formulai ($\text{Ilgums mēnešos} \approx \sqrt{\text{Darbietilpība cilvēkmēnešos}} = \sqrt{11} \approx 3.3\text{ mēneši}$), kas apliecina, ka 4 speciālistu komandai 5 mēnešu kalendārais ietvars ir reāls un izpildāms.

---

## 2. Projekta šķirtnes (Milestones)

Šķirtne ir nozīmīgs notikums projektā, kura **ilgums ir 0**. Šķirtnes atbilst līguma galvenajiem atskaites punktiem un SMART kritērijiem:

| Šķirtnes ID | Nosaukums un saturs | Plānotais datums | Saistītais līguma nodevums |
|:---:|:---|:---:|:---|
| **Š-1** | **Sistēmas arhitektūra un koncepcija** | **31.05.2025.** | Augsta līmeņa arhitektūra, datu plūsmas un prasību specifikācija (M1). |
| **Š-2** | **Tehniskais dizains un drošība** | **30.06.2025.** | Datubāzes shēma, drošības prasību apraksts un testēšanas vides plāns (M2). |
| **Š-3** | **Bāzes prototipa gatavība** | **31.08.2025.** | Darbspējīgs OCPP 2.1 prototips, datubāzes saglabāšana un testu atskaites (M3). |
| **Š-4** | **Gala sistēmas pieņemšana** | **30.09.2025.** | Pilna sistēma, tarifi, API, slodzes testi, UAT akcepts un fiziska koda nodošana (M4). |

---

## 3. Aktivitāšu secība un izstrādes posmi

Aktivitātes ir savstarpēji loģiski saistītas secīgās darba fāzēs:

1. **1. Fāze: Prasību analīze un sistēmas arhitektūra (Maijs 2025)**:
   * Prasību precizēšana kopā ar Pasūtītāju (200 h).
   * Sistēmas konceptuālās arhitektūras un datu plūsmu izstrāde.
   * *Noslēgums:* Šķirtne Š-1 (31.05.2025.).
2. **2. Fāze: Tehniskais dizains un datubāzes shēma (Jūnijs 2025)**:
   * PostgreSQL relāciju tabulu un Redis kešatmiņas projektēšana (200 h).
   * Drošības arhitektūras un digitālo sertifikātu pārbaudes mehānisma apraksts.
   * *Noslēgums:* Šķirtne Š-2 (30.06.2025.).
3. **3. Fāze: Bāzes prototipa izstrāde (Jūlijs – Augusts 2025)**:
   * Reāllaika sakaru servera programmēšana (OCPP 2.1 bāzes ziņojumi) (450 h).
   * Atpakaļsavietojamības adapteri OCPP 1.6 stacijām.
   * Vienību un integrācijas testēšana.
   * *Noslēgums:* Šķirtne Š-3 (31.08.2025.).
4. **4. Fāze: Paplašinātā funkcionalitāte, tarifi un API (Augusts – Septembris 2025)**:
   * Dinamisko tarifu aprēķinu modulis (500 h).
   * REST API saskarnes ERP un CRM integrācijām.
5. **5. Fāze: Kvalitātes pārbaude, slodzes testi un UAT (Septembris 2025)**:
   * Veiktspējas testi (500+ staciju vienlaicīga slodze) un drošības audits (250 h).
   * Lietotāju akcepttests (UAT) ar Pasūtītāju un dokumentācijas sagatavošana (160 h).
   * *Noslēgums:* Šķirtne Š-4 (30.09.2025.).

---

## 4. Izstrādes iterācijas (Sprintu ritms)

Komandas ikdienas darbs norit **desmit 2 nedēļu sprintos**:

| Iterācija | Laika periods | Galvenais uzdevums | Saikne ar šķirtnēm |
|:---:|:---:|:---|:---:|
| **1. sprints** | 05.05. – 16.05.2025. | Prasību analīze, lietotāju stāsti, izstrādes vide | Sagatavo Š-1 |
| **2. sprints** | 19.05. – 30.05.2025. | Arhitektūras shēma un datu plūsmu saskaņošana | **Šķirtne Š-1 (31.05.)** |
| **3. sprints** | 02.06. – 13.06.2025. | Datubāzes relāciju shēma un entītiju struktūra | Sagatavo Š-2 |
| **4. sprints** | 16.06. – 27.06.2025. | Drošības specifikācija un testa vides plāns | **Šķirtne Š-2 (30.06.)** |
| **5. sprints** | 30.06. – 11.07.2025. | Servera sakaru kodols un sesiju uzturēšana | Izstrāde Š-3 |
| **6. sprints** | 14.07. – 25.07.2025. | Bāzes OCPP 2.1 ziņojumi (*Boot, Heartbeat, Status*) | Izstrāde Š-3 |
| **7. sprints** | 28.07. – 08.08.2025. | Transakciju uzskaite un OCPP 1.6 savietojamība | Izstrāde Š-3 |
| **8. sprints** | 11.08. – 22.08.2025. | Prototipa integrācijas testi un demonstrācija | **Šķirtne Š-3 (31.08.)** |
| **9. sprints** | 25.08. – 05.09.2025. | Dinamiskie tarifi un REST API integrācijām | Izstrāde Š-4 |
| **10. sprints**| 08.09. – 19.09.2025. | Slodzes testēšana (500+ stacijas) un drošības audits | Sagatavo Š-4 |
| **Pabeigšana**| 22.09. – 30.09.2025. | UAT akcepttests, koda ieraksts USB/HDD un nodošana | **Šķirtne Š-4 (30.09.)** |

---

## 5. Kritiskā ceļa metode (CPM) un rezerves laiks

### 5.1. Kritiskais ceļš
Kritiskais ceļš ir savstarpēji atkarīgo aktivitāšu virkne, kas nosaka visīsāko iespējamo projekta izpildes laiku:
$$\text{Arhitektūra (M1)} \longrightarrow \text{Datubāze un drošība (M2)} \longrightarrow \text{Servera kodols (M3)} \longrightarrow \text{Tarifi un API} \longrightarrow \text{Slodzes testi un UAT (M4)}$$
Jebkurš kavējums šajā ķēdē tieši apdraud 2025. gada 30. septembra termiņu.

### 5.2. Rezerves laiks (Buferis)
Lai mazinātu Parkinsona likuma ietekmi (*"darbs aizņem visu tam atvēlēto laiku"*):
* Drošības buferi netiek mākslīgi pievienoti katrai mazai aktivitātei.
* Tiek izveidots **kopējais projekta laika buferis (aptuveni 1 nedēļa septembra beigās)** neparedzētiem kļūdu labojumiem un UAT saskaņošanai pirms oficiālā līguma termiņa.

---

## 6. Grafika uzraudzība un saīsināšanas paņēmieni

* **Kontrole pret grafika bāzlīniju**: Progresa mērīšana notiek katru ceturtdienu.
* **10–15% noviržu slieksnis**: Ja izpilde kavējas par vairāk nekā 10%, tiek aktivizēti grafika saīsināšanas paņēmieni:
  * **Saspiešana (*Crashing*)**: Papildu iekšējo resursu piesaiste kritiskā ceļa uzdevumiem.
  * **Paralelizēšana (*Fast Tracking*)**: Atsevišķu aktivitāšu (piemēram, tarifu moduļa izstrādes un API dokumentēšanas) izpilde paralēli.
