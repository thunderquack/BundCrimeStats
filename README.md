# BundCrimeStats

## Data Preparation

The repository does not store the source Excel workbooks because they are too large.

Download these files from Destatis:

- https://www.destatis.de/DE/Themen/Staat/Justiz-Rechtspflege/Publikationen/_publikationen-innen-strafverfolgung.html

Place the downloaded workbooks into `src/` with these names:

- `src/bund-2022.xlsx`
- `src/bund-2023.xlsx`
- `src/bund-2024.xlsx`

Then run `crime_stats_load.ipynb`.

It reads these sheets from each workbook:

- `csv-24311-05`
  Contains counts by article (`Art_der_Straftat`) for both `Abgeurteilte` and `Verurteilte`.
- `csv-24311-07`
  Contains decision type (`Art_d_Entscheidung`) by article.
- `csv-24311-47`
  Contains citizenship (`Staatsangehoerigkeit`) for `Verurteilte` by article.
- `csv-24311-03`
  Contains yearly totals for `Abgeurteilte` and `Verurteilte` for all crimes in Germany.

The loader writes these CSV files into `out/`:

- `out/by_article.csv` from `csv-24311-05`
- `out/decision_type.csv` from `csv-24311-07`
- `out/citizenship.csv` from `csv-24311-47`
- `out/year_totals.csv` from `csv-24311-03`

Run `conviction_rate_analysis.ipynb` after that.

It reads the prepared CSV files from `out/` and writes:

- `out/year_conviction_rates.csv`
- `out/article_conviction_rates.csv`
