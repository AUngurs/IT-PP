# FINANŠU UN IZMAKSU PĀRVALDĪBAS PLĀNS

**Projekts:** BackOffice sistēmas izstrāde – 1. Daļa OCPP (VMKC_Iep-12)  
**Dokuments:** Finanšu un izmaksu pārvaldības plāns  
**Versija:** 1.0 (1. Nodevums — 50%)

---

## 1. Finanšu pārvaldības pamatprincipi

Finanšu plāna uzdevums ir nodrošināt caurspīdīgu projekta cilvēkresursu un izmaksu uzskaiti atbilstoši iepirkuma nolikumam un CFLA pētniecības projekta Nr. `2.2.1.3.i.0/1/24/A/CFLA/004` prasībām.

Projekta kopējais darba apjoms ir noteikts **11 cilvēkmēneši** (~1760 cilvēkstundas), ko 5 mēnešu laikā (maijs – septembris 2025) realizē 4 vadošo IT speciālistu komanda.

### Novērtējuma precizitātes robežas
Atbilstoši projekta fāzei tiek piemērotas nozares standarta precizitātes robežas:
* **Budžeta plānošanas posmā**: no $-10\%$ līdz $+25\%$ (pašreizējais 1. nodevuma stāvoklis).
* **Īstenošanas posmā**: no $-5\%$ līdz $+10\%$ (precizējas sprintu gaitā).

---

## 2. Izmaksu struktūra (Tiešās un netiešās izmaksas)

### 2.1. Tiešās izmaksas (Darbaspēks un materiāli)
Tiešās izmaksas ir tieši attiecināmas uz šī projekta aktivitātēm (ja projekts netiktu īstenots, šīs izmaksas nerastos):

| Lomas nosaukums komandā | Galvenie uzdevumi | Darbietilpība (stundas) | Vienības likme (EUR/h) | Tiešās izmaksas (EUR bez PVN) |
|:---|:---|:---:|:---:|:---:|
| **Projekta vadītājs / Sistēmu arhitekts** | Vadība, CFLA atskaites, arhitektūra, sadarbība ar Pasūtītāju. | 350 h | 55.00 | 19 250.00 |
| **Vadošais izstrādātājs** | Servera kodols, OCPP 2.1 ziņojumi, datubāze, REST API. | 650 h | 50.00 | 32 500.00 |
| **Drošības un tīklu inženieris** | Šifrētie sakari, digitālie sertifikāti, piekļuves lomas (RBAC). | 380 h | 50.00 | 19 000.00 |
| **Testēšanas (QA) inženieris** | Automatizētie testi, slodzes mērījumi, kļūdu reģistrs, UAT. | 380 h | 40.00 | 15 200.00 |
| **KOPĀ darbaspēka tiešās izmaksas:** | — | **1760 h** | — | **85 950.00** |
| Tiešie materiālie izdevumi (fiziskie USB/HDD nesēji, licence): | — | — | — | 3 500.00 |
| **KOPĀ tiešās izmaksas:** | — | — | — | **89 450.00** |

*Piezīme:* Vienības stundas likme ir aprēķināta pēc formulas: $(\text{Tiešās izmaksas} + \text{Attiecināmās netiešās izmaksas} + \text{Peļņas uzcenojums}) / \text{Plānotās stundas}$.

---

## 3. Izmaksu bāzlīnija un budžeta sadalījums pa mēnešiem

Izmaksu bāzlīnija ir formāli apstiprinātās un laika periodiem piekārtotās projekta izmaksas:

| Mēnesis | Plānotās aktivitātes un nodevumi | Mēneša izmaksas (EUR bez PVN) | Kumulatīvā summa no sākuma (EUR) |
|:---:|:---|:---:|:---:|
| **05/2025** | Prasības un arhitektūras koncepcija (Nodevums M1) | 10 200.00 | 10 200.00 |
| **06/2025** | Datubāzes dizains un drošības specifikācija (Nodevums M2) | 10 200.00 | 20 400.00 |
| **07/2025** | Servera kodola izstrāde (Sprinti 5 un 6) | 22 900.00 | 43 300.00 |
| **08/2025** | Bāzes prototipa pabeigšana un testi (Nodevums M3) | 23 000.00 | 66 300.00 |
| **09/2025** | Tarifi, API, slodzes testi, UAT un gala nodošana (Nodevums M4) | 23 150.00 | **89 450.00** |

---

## 4. Projekta rezerves

Finanšu stabilitātei tiek nodalītas divu veidu rezerves:
1. **Neparedzēto izdevumu rezerve (*Contingency Reserve*)**:
   * Paredzēta **zināmajiem riskiem** (tiem, kas identificēti risku analīzē, piemēram, neparedzēti staciju emulatoru integrācijas defekti).
   * Ietilpst apstiprinātajā izmaksu bāzlīnijā, un ar to rīkojas projekta vadītājs savu pilnvaru ietvaros (~5% apmērā no darba stundām).
2. **Vadības rezerve (*Management Reserve*)**:
   * Paredzēta **nezināmajiem riskiem** un ārkārtas izmaiņām ārpus sākotnējā tvēruma.
   * Neietilpst izmaksu bāzlīnijā; to pārrauga un par tās piešķiršanu lemj tikai Pasūtītājs (Sponsors).

---

## 5. Maksājumu kārtība un norēķinu plūsma

Saskaņā ar iepirkuma nolikuma un līguma projekta 4. sadaļu samaksa par izpildīto pakalpojumu notiek pa daļām:

1. **30% Priekšapmaksa (avanss)**:
   * **26 835.00 EUR (bez PVN)** tiek izmaksāti 3 darba dienu laikā pēc līguma noslēgšanas un atbilstoša rēķina saņemšanas.
2. **Starpposmu maksājumi par 1., 2. un 3. posma nodevumiem**:
   * Tiek veikti proporcionāli 3 darba dienu laikā pēc attiecīgā starpposma pieņemšanas-nodošanas akta parakstīšanas.
3. **Gala norēķins (pēc 4. posma)**:
   * Tiek veikts ieskaita veidā pret iepriekš samaksāto avansu un starpmaksājumiem pēc UAT pieņemšanas akta parakstīšanas un materiālu fiziskas nodošanas USB/HDD nesējā.

---

## 6. Finanšu kontrole un Nopelnītās vērtības analīze (Earned Value)

Lai sekotu faktiskajam izmaksu un darba progresam, tiek izmantota Nopelnītās vērtības analīzes (*Earned Value Management*) metodika:
* **PV (*Planned Value*)**: Plānotās izmaksas līdz konkrētajam datumam saskaņā ar bāzlīniju.
* **EV (*Earned Value*)**: Nopelnītā vērtība jeb reāli paveiktā un pieņemtā darba budžeta vērtība.
* **AC (*Actual Cost*)**: Faktiski iztērētās izmaksas (reģistrētās cilvēkstundas).

### Efektivitātes rādītāji:
* **Izmaksu novirze**: $CV = EV - AC$ (ja $CV < 0$, projekts tērē vairāk nekā plānots).
* **Grafika novirze**: $SV = EV - PV$ (ja $SV < 0$, projekts atpaliek no grafika).
* **Izmaksu efektivitātes indekss**: $CPI = EV / AC$ (mērķis: $\ge 1.0$).
* **Grafika efektivitātes indekss**: $SPI = EV / PV$ (mērķis: $\ge 1.0$).

### 10–15% Brīdinājuma slieksnis
Ja faktiskais cilvēkstundu patēriņš vai izmaksas pārsniedz plānoto bāzlīniju par vairāk nekā **10–15%**, projekta vadītājam ir pienākums nekavējoties rakstiski informēt Pasūtītāju un sagatavot korektīvo rīcības plānu, lai novērstu līgumsoda iestāšanos (Līguma 9.1. punkts: 0,2% par katru nokavēto dienu).
