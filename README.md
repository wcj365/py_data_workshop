# Python for Data Analysis Workshop

## CPE and Job Code

TBD

## Course Format & Schedule

- Hands-on workshop
- Cover both Python coding and GAO practices 
- One hour per session
- Two sessions per week
- Total eight sessions

## Development Environment

  - Posit Workbench
  - VS Code

If you don't have access to Posit Workbench, please 

## Prerequisites

Familiarity with the following is a plus:

  - Markdown
  - Python
  - Jupyter Notebooks

If you are not familiar with the above, no worries. We will cover them in the first session.

## Course Objectives

By the end of this 8-session workshop, participants will be able to:

1. **Setup projects and follow GAO best practices**

2. **Import and Inspect datasets**
   - using pandas from CSV files, and save results to multiple formats (CSV, Excel, JSON).
4. systematically — understanding shape, data types, distributions, and unique values — to quickly orient themselves to any new dataset.
5. **Assess data quality** by identifying missing values, duplicates, outliers, and inconsistencies.
6. **Clean real-world data** by handling nulls, correcting data types, standardizing string fields, and removing or imputing problematic records.
7. **Transform data** through subsetting (filtering rows and selecting columns) and renaming existing columns, createing derived variables.
8. **Reshape data** between wide and long (tidy) formats using `melt`, `pivot`, and `pivot_table` to support different analytical needs.
9. **Aggregate and summarize data** using `groupby` to aggregate and aggregate functions to summarize data within each group.
10. **Create interactive visualizations** with Plotly Express to create interactive data visualizations to explore data and communicate findings.

---

## Python Packages to be Used

 - pandas
 - plotly
 - openpyxl
 - nbformat

## Dataset to be Used

The World Bank's World Development Indicators (WDI)

We will use this dataset through out.

**File:** `World_Dev_Indicators.csv`

| Property | Value |
|----------|-------|
| Rows | 4,340 |
| Columns | 11 |
| Countries | 217 |
| Years | 2006–2025 |

**Columns:**

| Column | Type | Description |
|--------|------|-------------|
| `Year` | int | Year of observation |
| `Country` | str | Country name |
| `Country Code` | str | ISO 3-letter country code |
| `Region` | str | World Bank region (7 regions) |
| `Income Group` | str | World Bank income classification |
| `Lending Type` | str | World Bank lending category |
| `GDP (current US$)` | float | Gross domestic product in USD |
| `GDP per capita (current US$)` | float | GDP divided by population |
| `Life expectancy at birth, total (years)` | float | Average life expectancy |
| `Population, total` | int | Total population |
| `Suicide mortality rate (per 100,000 population)` | float | Suicide rate per 100k people |

---

## Course Outline

### Session 1 — Getting Started: Development Environment and GAO Standards

- Posit Workbench and VS Code IDE
- Project structure and required packages
- GAO audit requirements and best practices
- Jupyter Notebooks, Markdown, and Python Refresher

### Session 2 — Data Import/Export and Understanding

*Topics:* data import, Shape, dtypes, head/tail, describe, value counts, unique values, info summary  
*Key functions:* `pd.read_csv()`, `df.to_excel()`, `df.shape`, `df.info()`, `df.describe()`, `df.value_counts()`, `df.nunique()`

### Session 3 — Data Quality Assessment

*Topics:* Identifying missing values, detecting duplicates, spotting outliers, data quality reporting  
*Key functions:* `df.isnull()`, `df.duplicated()`, `df.describe()` (IQR method)

### Session 4 — Data Cleansing

*Topics:* Handling missing values (drop/fill/impute), fixing data types, standardizing strings, removing duplicates  
*Key functions:* `df.dropna()`, `df.fillna()`, `df.astype()`, `str.strip()`

### Session 5 — Data Subsetting 

*Topics:* Filtering rows, selecting columns, boolean conditions, creating new columns, `apply()` and lambda function  
*Key functions:* `df.loc[]`, `df.iloc[]`, Boolean indexing, `df['new_col'] = ...`, `df.apply()`

### Session 6 — Data Reshaping

*Topics:* Wide vs. long format, melting, pivoting, pivot tables, sorting and ranking  
*Key functions:* `pd.melt()`, `df.pivot()`, `df.pivot_table()`, `df.sort_values()`, `df.rank()`

### Session 7 — Data Aggregation 

*Topics:* GroupBy mechanics, single and multiple aggregations, custom functions, rolling windows, cumulative stats  
*Key functions:* `df.groupby()`, `.agg()`, `.transform()`, `.rolling()`, `.cumsum()`

### Session 8 — Data Visualization

*Topics:* Line charts, bar charts, scatter plots, box plots, choropleth maps, faceted charts, customization  
*Key functions:* `px.line()`, `px.bar()`, `px.scatter()`, `px.box()`, `px.choropleth()`, `px.facet_*`

---



