# Python for Data Analysis Workshop
## Using World Development Indicators Dataset

---

## Course Objectives

By the end of this 8-session workshop, participants will be able to:

1. **Import and export data** using pandas from CSV files, and save results to multiple formats (CSV, Excel, JSON).
2. **Inspect datasets** systematically — understanding shape, data types, distributions, and unique values — to quickly orient themselves to any new dataset.
3. **Assess data quality** by identifying missing values, duplicates, outliers, and inconsistencies using pandas diagnostics.
4. **Clean real-world data** by handling nulls, correcting data types, standardizing string fields, and removing or imputing problematic records.
5. **Transform data** through subsetting (filtering rows and selecting columns), feature engineering, and renaming/reorganizing structures.
6. **Reshape data** between wide and long (tidy) formats using `melt`, `pivot`, and `pivot_table` to support different analytical needs.
7. **Aggregate and summarize data** using `groupby`, multi-level aggregations, and ranking operations to extract meaningful insights.
8. **Create interactive visualizations** with Plotly Express — including line charts, bar charts, scatter plots, choropleth maps, and faceted views — to communicate findings clearly.

---

## Dataset: World Development Indicators

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

**Data Quality Notes (discovered during preparation):**
- GDP and GDP per capita have ~352 missing values
- Life expectancy and population each have ~217 missing values
- Suicide mortality rate has ~1,380 missing values (most prevalent missing field)

---

## Course Outline

### Session 1 — Getting Started: Data Import & Export
*Topics:* Python & Jupyter basics, reading CSV files, exploring file arguments, saving data to CSV/Excel/JSON  
*Key functions:* `pd.read_csv()`, `df.to_csv()`, `df.to_excel()`, `df.to_json()`

### Session 2 — Knowing Your Data: Inspection & Profiling
*Topics:* Shape, dtypes, head/tail, describe, value counts, unique values, info summary  
*Key functions:* `df.shape`, `df.info()`, `df.describe()`, `df.value_counts()`, `df.nunique()`

### Session 3 — Data Quality Assessment
*Topics:* Identifying missing values, detecting duplicates, spotting outliers, data quality reporting  
*Key functions:* `df.isnull()`, `df.duplicated()`, `df.describe()` (IQR method)

### Session 4 — Data Cleaning
*Topics:* Handling missing values (drop/fill/impute), fixing data types, standardizing strings, removing duplicates  
*Key functions:* `df.dropna()`, `df.fillna()`, `df.astype()`, `str.strip()`, `str.title()`

### Session 5 — Data Transformation: Subsetting & Feature Engineering
*Topics:* Filtering rows, selecting columns, boolean conditions, creating new columns, `apply()` and lambda  
*Key functions:* `df.loc[]`, `df.iloc[]`, Boolean indexing, `df['new_col'] = ...`, `df.apply()`

### Session 6 — Data Reshaping
*Topics:* Wide vs. long format, melting, pivoting, pivot tables, sorting and ranking  
*Key functions:* `pd.melt()`, `df.pivot()`, `df.pivot_table()`, `df.sort_values()`, `df.rank()`

### Session 7 — Data Aggregation & Summarization
*Topics:* GroupBy mechanics, single and multiple aggregations, custom functions, rolling windows, cumulative stats  
*Key functions:* `df.groupby()`, `.agg()`, `.transform()`, `.rolling()`, `.cumsum()`

### Session 8 — Data Visualization with Plotly Express
*Topics:* Line charts, bar charts, scatter plots, box plots, choropleth maps, faceted charts, customization  
*Key functions:* `px.line()`, `px.bar()`, `px.scatter()`, `px.box()`, `px.choropleth()`, `px.facet_*`

---

## Prerequisites

- Basic Python knowledge (variables, lists, loops, functions)
- Jupyter Notebook or JupyterLab installed
- Libraries: `pandas`, `plotly`, `openpyxl`

**Install all dependencies:**
```bash
pip install pandas plotly openpyxl nbformat
```

---

## Workshop Notes

- Each session is approximately **60 minutes**
- Notebooks include explanatory markdown, code cells with comments, and exercises at the end
- All sessions use the **same dataset** — skills build progressively
- Sessions 1–4 focus on data engineering fundamentals; Sessions 5–8 on analytics and visualization

