# BundCrimeStats

## Source sheets for CSV export

The source Excel files are stored in `src/`:

- `src/bund-2022.xlsx`
- `src/bund-2023.xlsx`
- `src/bund-2024.xlsx`

These Excel files were taken from Destatis:

- https://www.destatis.de/DE/Themen/Staat/Justiz-Rechtspflege/Publikationen/_publikationen-innen-strafverfolgung.html

For CSV export, use these sheets from each workbook:

- `csv-24311-05`
  Contains counts by article (`Art_der_Straftat`) for both `Abgeurteilte` and `Verurteilte`.
- `csv-24311-07`
  Contains decision type (`Art_d_Entscheidung`) by article.
- `csv-24311-47`
  Contains citizenship (`Staatsangehoerigkeit`) for `Verurteilte` by article.

Expected output CSV datasets:

- `by_article.csv` from `csv-24311-05`
- `decision_type.csv` from `csv-24311-07`
- `citizenship.csv` from `csv-24311-47`
