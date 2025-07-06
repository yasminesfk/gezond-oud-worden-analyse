# Gezond Oud Worden – Data-analyseproject

## Overzicht
Dit project onderzoekt welke regio in Nederland de hoogste gezonde levensverwachting heeft. Het team gebruikte open datasets van o.a. het CBS en RIVM, analyseerde indicatoren als inkomen, opleidingsniveau, beweging en toegang tot medische zorg, en presenteerde de bevindingen in grafieken en infographics.

## Projectstructuur
```bash
GezondOudWorden/
├── data/                        # Alle ruwe CSV-bestanden
│   ├── Geregistreerde_criminaliteit_Noord_Nederland.csv
│   ├── Regionale_kerncijfers_Nederland_22012025_144703.csv
│   ├── Gezonde_levensverwachting__vanaf_1981_29012025_112744.csv
│   ├── klik_lv_ggd_20192022.csv
│   ├── 71950ned_TypedDataSet_29012025_112846.csv
│   ├── Gezondheidsmonitor__bevolking_18_jaar_of_ouder__regio__2022_22012025_151906.csv
│   ├── Dataset4_Gem_Levensverwachting_PER_PRO_filtered.csv
│   ├── Hoogst_behaalde_onderwijsniveau.csv
│   └── Inkomen_van_huishoudens__huishoudenskenmerken__regio__indeling_2023__22012025_150250 (1).csv
├── database/                   # .db-bestanden met SQL-tabellen
│   ├── Dataset1_gezondelevensverwachting_vanaf_198.db
│   ├── Dataset2_gezondelevensverwachting_per_aandoening.db
│   ├── Dataset3_REG_criminaliteit_Noord.db
│   ├── Dataset4_Gem_Levensverwachting_PER_PRO.db
│   ├── Dataset5_inkomen_huishoudens.db
│   ├── Dataset6_Regionale_kerncijfers_Nederland.db
│   ├── Dataset6_regio_kerncijfers.db
│   ├── Dataset7_Hoogst_behaalde_onderwijsniveau.db
│   └── Dataset8_gezondheidmonitor_bevolking_18jaar.db
├── notebook/                   # Python notebooks
│   └── gezond-oud-worden-analyse.ipynb
├── images/
├── graphs/                # Grafieken gegenereerd in Python
│   │   ├── Bewegen_en_sport_Voldoet_aan_beweegrichtlijn.png
│   │   ├── Bewegen_en_sport_Wekelijkse_sporters.png
│   │   ├── Inkomen_Gemiddeld besteedbaar inkomen 1000 euro.png
│   │   ├── Inkomen_Gemiddeld gestandaardiseerd inkomen 1000 euro.png
│   │   ├── Inkomen_Mediaan besteedbaar inkomen 1000 euro.png
│   │   ├── Inkomen_Mediaan gestandaardiseerd inkomen 1000 euro.png
│   │   ├── Ervaren_gezondheid_(goed_zeer_goed).png
│   │   ├── Eén_of_meer_langdurige_aandoeningen.png
│   │   ├── Psychische_klachten_(MHI-5__60).png
│   │   ├── Bij_geboorte_by_GGD_regio.png
│   │   ├── Onderwijsniveau 5 categorieën_11 Basisonderwijs.png
│   │   ├── Onderwijsniveau 5 categorieën_12 Vmbo, havo-, vwo-onderbouw, mbo1.png
│   │   ├── Onderwijsniveau 5 categorieën_21 Havo, vwo, mbo2-4.png
│   │   ├── Onderwijsniveau 5 categorieën_31 Hbo-, wo-bachelor.png
│   │   ├── Onderwijsniveau 5 categorieën_32 Hbo-, wo-master, doctor.png
│   │   ├── Rokers.png
│   │   ├── Alcoholgebruik_Overmatige_drinkers_onder_bevolking.png
│   │   └── Alcoholgebruik_Voldoet_aan_richtlijn_alcoholgebruik.png
└── infographic/           # Visueel ontworpen overzicht
    └── infographic_gezond_oud_worden.jpg
```

## Centrale vraag
> Welke regio in Nederland scoort het hoogst op het gebied van gezonde levensverwachting?

## Gebruikte indicatoren
- **Opleidingsniveau** (hoogopgeleiden per regio)
- **Inkomen** (besteedbaar inkomen per huishouden)
- **Beweging** (procentuele naleving bewegingsrichtlijnen)
- **Toegang tot medische zorg** (huisartsen per 10.000 inwoners)

## Tools & technologieën
- **Python** (`pandas`, `matplotlib`, `seaborn`, `sqlite3`)
- **SQLite** – opslag en querying van data
- **Canva** – ontwerp van infographics

## Resultaten
Uit de gecombineerde analyse blijkt dat **de provincie Utrecht** de hoogste gezonde levensverwachting heeft, op basis van bovengenoemde indicatoren.

## Leerpunten
- CSV-bestanden bevatten soms headers die fouten veroorzaken in scripts; opgelost door handmatige opschoning.
- Correlatie- en regressieanalyses boden inzicht in indicatorrelaties.
- Visualisaties werkten goed maar kunnen sterker met kleurcontrasten.

## Gebruik
Je kunt het project lokaal uitvoeren door de notebooks te openen in Jupyter en de SQLite-databases aan te roepen via `sqlite3` of `pandas.read_sql()`:

```python
import pandas as pd
import sqlite3

conn = sqlite3.connect('database/Dataset1_gezondelevensverwachting_vanaf_198.db')
df = pd.read_sql("SELECT * FROM Dataset1_gezondelevensverwachting_vanaf_198_table", conn)
```

## Credits
**Projectteam**:
- Tijl van Rijt
- Yasmine Safak
- Joey Molenaar
- Abdelilah Lahmar
- Dhiradj Pershad

**Begeleiding:** docenten van Hogeschool Rotterdam

## Werkwijze
We hebben als team gewerkt volgens de scrummethode. 
Tijdens het project waren er vaste scrumsessies waarin we rollen verdeelden, taken bespraken, en voortgang bijhielden. 
De scrummethode hielp ons om gefaseerd en gestructureerd toe te werken naar het eindproduct.

## Licentie
MIT License – vrij te gebruiken met bronvermelding.
