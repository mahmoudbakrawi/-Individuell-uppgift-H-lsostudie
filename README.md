# Hälsostudie – Individuell uppgift

## Projektbeskrivning

Detta projekt är en individuell uppgift inom Pythonprogrammering och statistisk dataanalys.

Syftet är att analysera hälsodata med Python och använda beskrivande statistik, visualiseringar, simuleringar och hypotesprövning för att undersöka olika samband i datasetet.

Analysen genomförs i Jupyter Notebook.

## Dataset

Datasetet innehåller information om 800 personer och följande variabler:

| Variabel | Beskrivning |
|---|---|
| `age` | Ålder i år |
| `sex` | Kön (M/F) |
| `height` | Längd i centimeter |
| `weight` | Vikt i kilogram |
| `systolic_bp` | Systoliskt blodtryck i mmHg |
| `cholesterol` | Kolesterolvärde i mmol/L |
| `smoker` | Rökvanor (Yes/No) |
| `disease` | Sjukdomsstatus (0/1) |

Datafilen finns i `data/health_study_dataset.csv`.

## Metoder och analyser

Projektet innehåller följande delar:

### 1. Beskrivande statistik

Beräkning av medelvärde, median, minimum och maximum för numeriska variabler.

### 2. Datavisualisering

Visualisering av data med hjälp av:

- Stapeldiagram för rökvanor uppdelat på kön.
- Boxplot för systoliskt blodtryck uppdelat på kön.
- Spridningsdiagram för sambandet mellan vikt och kolesterol.

### 3. Korrelationsanalys

Undersökning av sambandet mellan vikt och kolesterol med Pearsons korrelationskoefficient.

### 4. Simulering

Simulering av sjukdomsförekomst hos 1 000 personer med hjälp av sannolikheten från datasetet.

### 5. Konfidensintervall

Beräkning av ett 95-procentigt konfidensintervall för det genomsnittliga systoliska blodtrycket med två metoder:

- t-fördelning.
- Bootstrap.

Resultaten från metoderna jämförs.

### 6. Hypotesprövning

Undersökning av hypotesen att rökare har högre genomsnittligt systoliskt blodtryck än icke-rökare.

Ett ensidigt Welch's t-test används med signifikansnivån 0,05.

### 7. Statistisk styrka (Power)

Simulering med 1 000 upprepningar för att undersöka hur ofta hypotesprövningen upptäcker en statistiskt signifikant skillnad vid olika antagna ökningar av blodtrycket.

## Sammanfattning av resultat

- Det genomsnittliga systoliska blodtrycket var 149,18 mmHg.
- Ett 95-procentigt konfidensintervall beräknades med t-fördelning och bootstrap. Metoderna gav liknande resultat.
- Korrelationsanalysen visade ett svagt positivt samband mellan vikt och kolesterol (r = 0,256).
- Hypotesprövningen gav ett p-värde på 0,326. Ingen statistiskt signifikant skillnad kunde påvisas mellan rökare och icke-rökare.
- Power-simuleringen visade att sannolikheten att upptäcka en statistiskt signifikant skillnad ökade när den antagna skillnaden mellan grupperna blev större.

## Projektstruktur

```text
-Individuell-uppgift-H-lsostudie/
│
├── data/
│   └── health_study_dataset.csv
│
├── notebooks/
│   └── del_1_analys.ipynb
│
├── .gitignore
├── README.md
└── requirements.txt
```

## Verktyg och bibliotek

Projektet är utvecklat med:

- Python 3.14.7
- Jupyter Notebook
- Pandas – datahantering och analys
- NumPy – numeriska beräkningar och simuleringar
- Matplotlib – datavisualisering
- SciPy – statistiska tester och beräkningar

## Så kör du projektet

1. Klona eller ladda ner projektet.
2. Öppna projektmappen i Visual Studio Code.
3. Skapa och aktivera en virtuell Python-miljö.
4. Installera biblioteken från `requirements.txt`:

   ```bash
   pip install -r requirements.txt
   ```

5. Öppna `notebooks/del_1_analys.ipynb`.
6. Välj rätt Python-miljö och kör notebookens celler i ordning.

## Källor och dokumentation

- [Python Documentation](https://docs.python.org/3/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [NumPy Documentation](https://numpy.org/doc/stable/)
- [Matplotlib Documentation](https://matplotlib.org/stable/)
- [SciPy – t-test](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.ttest_ind.html)
- [SciPy – Bootstrap](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.bootstrap.html)

## Slutsats

Projektet visar hur Python kan användas för att analysera hälsodata och undersöka statistiska samband.

Genom att kombinera beskrivande statistik, visualisering, simulering och hypotesprövning går det att få en bättre förståelse för datamaterialet och hur statistisk osäkerhet påverkar resultaten.