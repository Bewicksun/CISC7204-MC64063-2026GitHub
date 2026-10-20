## 官方数据来源与核对记录

# Source record and data checks

Retrieved and checked on 20 October 2026. This folder contains the completed monthly analysis for Assignment 02 Pair 01, extending the Assignment 01 topic.

## Monthly visitor arrivals

Macao Government Tourism Office (MGTO), Total Visitor Arrivals, showing **Source: DSEC**. Filter: monthly, January 2019 to December 2025.

https://dataplus.macaotourism.gov.mo/Indicator/VisitorsSummary/SummaryBar?lang=E&periodtype=M&start=241&end=324

The official page contains the month categories and the Total_Value data series. The original web page is not redistributed in this repository. The source page covers all 84 months in 2019–2025; the project selects only 2019 and 2023–2025, producing 48 rows in `visitor_monthly.csv`. Units: arrival counts, not unique individuals. All four yearly sums equal the official annual totals.

## Monthly gaming revenue

Gaming Inspection and Coordination Bureau (DICJ), Monthly Gross Revenue from Games of Fortune. The official HTML pages link to the following data files:

- 2019: https://www.dicj.gov.mo/web/en/information/DadosEstat_mensal/2019/report_en.xml
- 2023: https://www.dicj.gov.mo/web/en/information/DadosEstat_mensal/2023/report_en.xml
- 2024: https://www.dicj.gov.mo/web/en/information/DadosEstat_mensal/2024/report_en.xml
- 2025: https://www.dicj.gov.mo/web/en/information/DadosEstat_mensal/2025/report_en.xml

The source pages are the same addresses with `index.html` in place of `report_en.xml`. Original XML files remain available from the linked official sources. Use the current year's **Monthly Gross Revenue** column, not the preceding-year comparison or the accumulated column. Units: MOP million; nominal gross revenue from games of fortune. The data do not represent the total of every gaming activity. The extracted values are in `gaming_monthly.csv`.

## Annual background data

The seven annual rows continue the Assignment 01 dataset, checked against:

- Visitor totals 2019–2023: Macao Yearbook 2024, Appendix 19, Tourism. https://yearbook.gcs.gov.mo/uploads/yearbook_pdf/2024/myb2024eAP19.pdf
- DSEC 2024 visitor release: https://www.gcs.gov.mo/news/detail/en/N25AUB2Zwi
- DSEC 2025 visitor release: https://www.gcs.gov.mo/news/detail/en/N26AWC98hd
- DICJ 2021 statistics, games of fortune row, for 2019: https://www.dicj.gov.mo/web/cn/information/DadosEstat/2021/content.html
- DICJ 2025 statistics, games of fortune row, for 2020–2025: https://www.dicj.gov.mo/web/pt/information/DadosEstat/2025/content.html

The 2025 gaming annual value is 247404 MOP million, replacing the rounded 247400 in the Assignment 01 code.

## Reconciliation and calculation rules

- Each input CSV contains 48 unique Year–Month keys with no missing values. The merge has 48 rows; the 2019 baseline has 12 rows; the study has 36 months in 2023–2025.
- Visitor monthly sums agree exactly with the annual values for 2019, 2023, 2024, and 2025.
- Gaming monthly sums agree with the annual values in 2023–2025.
- The published 2019 monthly gaming values sum to **292456** MOP million, while the published annual total is **292455**. Both are retained. The difference of 1 MOP million is about 0.00034% of the annual value. Monthly values are published in whole MOP million; the monthly and cumulative columns can therefore differ slightly when summed. Do not silently adjust a month to force agreement.
- Monthly indices use the corresponding published 2019 monthly value. The annual chart uses the published annual totals, including 292455 for 2019. Annual indices are not averages of monthly indices.
- Gap = visitor recovery index minus gaming recovery index, measured in percentage points. Summary means and medians each use the 12 monthly gaps in the given year.
- Underlying calculations are not rounded. Text reports one decimal place. Tables and CSVs retain more precision.

The raw values and all outputs are local; rerunning the analysis does not require internet access.

## Exercise references

Module 01 Lab 02: `DataFrame.plot(kind='line')`.
Module 02 Lab 01: `Series.plot(kind='bar')`.
Module 02 Lab 02: `DataFrame.plot(kind='box')`.

The script uses only pandas and Matplotlib, with basic merging, filtering, groupby, pivot, labels and reference lines. Data retrieval is kept outside the student-facing analysis script.


## Usage permissions

This educational project reproduces small tables of publicly published, aggregate statistics with source attribution; it contains no individual records. DSEC publications state that reproduction of their data is allowed when the source is quoted (example: https://dsec.gov.mo/getAttachment/38cb0812-a040-43c9-93ca-605593ea7e8c/e_ssem_fr_2016_m10.aspx?disposition=attachment). No explicit open-data licence for the DICJ tables was verified. Public access is not a blanket redistribution licence: the original websites and XML archives are not included, and no licence is asserted over government source material. Check the relevant agency terms before further reuse.
