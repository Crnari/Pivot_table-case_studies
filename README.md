# Pivot Table Case Studies

> **En español:** Diez casos de negocio resueltos en Excel con tablas dinámicas, sobre unas
> 198.000 filas de datos. Cada caso parte de un dataset crudo y responde preguntas concretas
> usando campos calculados, agrupaciones, segmentaciones y gráficos. Todas las cifras fueron
> verificadas contra los datos originales. El detalle de cada caso está en `docs/`.

Ten business cases solved in Excel with PivotTables, across roughly 198,000 rows of data. Each case
starts from a raw dataset and answers a set of stakeholder questions using calculated fields,
grouping, custom value calculations, slicers and conditional formatting.

Every figure reported here was recomputed independently in Python against the raw data to verify
the PivotTable output.

## Cases

| # | Case | Rows | Write-up |
|---|---|---|---|
| 1 | U.S. voter demographics, 2012 | 255 | [docs](docs/01-voters.md) |
| 2 | San Francisco city payroll | 24,285 | [docs](docs/02-salaries.md) |
| 3 | Global shark attack records | 5,292 | [docs](docs/03-sharks.md) |
| 4 | Daily stock prices, 510 symbols | 29,440 | [docs](docs/04-stocks.md) |
| 5 | MLB team statistics, 1995-2015 | 624 | [docs](docs/05-baseball.md) |
| 6 | San Diego burrito ratings | 237 | [docs](docs/06-burritos.md) |
| 7 | Daily weather conditions, 2016 | 363 | [docs](docs/07-weather.md) |
| 8 | Spartan Race Facebook posts | 393 | [docs](docs/08-spartan.md) |
| 9 | Apple App Store catalogue | 7,197 | [docs](docs/09-apple.md) |
| 10 | Wine tasting scores | 129,971 | [docs](docs/10-wine.md) |

## Techniques

Calculated fields · date and numeric grouping · Show Values As (% of Column, % of Row, % of Parent,
Difference From, % Difference From, Rank) · value and Top-N filters · slicers and timelines ·
PivotCharts (bar, line, pie, 100% stacked column, combo with secondary axis) · conditional
formatting (color scales, data bars) · helper columns with `IF()`

## A note on calculated fields

Excel evaluates a calculated field against the **sum** of each source field, not row by row, so a
ratio written the obvious way returns the wrong number once rows are aggregated. Every ratio in
this workbook is expressed as a division of two additive quantities so the result stays correct at
any level of the table:

```
Temp Spread         = (Max Temp / # of Days) - (Min Temp / # of Days)
Average Total Score = ((Tortilla + Temp + Fillings + Synergy + Wrap) / 5) / # Reviews
Active Engagements  = (Shares + Comments) / # of Posts
```

## Files

- `PivotTable_Case_Studies.xlsx` — cases 1 to 9
- `PivotTable_Case_Studies_Wine.xlsx` — case 10, split out for file size
- `docs/` — written analysis and screenshots for each case

Source data is not saved with the PivotTables, so the workbooks refresh on open.

---

Datasets are course materials from the Maven Analytics Excel PivotTables course, included for
reproducibility.

**Cristian Cruz** · [GitHub](https://github.com/Crnari) · [LinkedIn](https://linkedin.com/in/cristian-cruz-n)
