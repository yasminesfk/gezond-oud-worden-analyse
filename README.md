# Gezond Oud Worden – Data-analyseproject

## Overzicht
Dit project onderzoekt welke regio in Nederland de hoogste gezonde levensverwachting heeft. Het team gebruikte open datasets van o.a. het CBS en RIVM, analyseerde indicatoren als inkomen, opleidingsniveau, beweging en toegang tot medische zorg, en presenteerde de bevindingen in grafieken en infographics.

## Projectstructuur
```bash
GezondOudWorden/
├── data/                        # Alle ruwe CSV-bestanden
│   ├── Gezonde_levensverwachting__vanaf_1981.csv
│   ├── 71950ned_TypedDataSet.csv
│   └── ...
├── database/                   # .db-bestanden met SQL-tabellen
│   ├── Dataset1_gezondelevensverwachting_vanaf_198.db
│   └── Dataset2_gezondelevensverwachting_per_aandoening.db
├── notebook/                   # Python notebooks
│   └── data-analyse.ipynb
├── images/                     # PNG-visualisaties en infographics
│   ├── Levensverwachting_per_regio.png
│   ├── Opleidingsniveau_vs_gezondheid.png
│   └── infographic_gezond_oud_worden.png
├── docs/                       # Documentatie en verslaglegging
│   ├── Reflectie_op_het_proces.pdf
│   ├── Verslag_data_ontsluiting.pdf
│   └── Rapport_data_analyse.pdf
└── README.md
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
