# Activity 6: Data Analysis

# Interactive Dashboard Prompt: Global FDI Inflows (% of GDP)

Create a polished, interactive analytical dashboard using the supplied World Bank dataset for indicator **BX.KLT.DINV.WD.GD.ZS — Foreign direct investment, net inflows (% of GDP)**.

## Objective

Build a dashboard that lets users understand:

1. How FDI inflows as a percentage of GDP have changed over time.
2. How countries compare with one another.
3. Which countries currently have the highest and lowest FDI inflows relative to GDP.
4. How Sri Lanka compares with regional peers and the global distribution.
5. Which countries show sustained improvement, deterioration, high volatility, or unusual spikes.
6. How FDI performance differs across World Bank regions and income groups, where classification data is available.

The dashboard should be designed for an economic analyst, policymaker, investor, researcher, or business user.

## Core KPI Cards

At the top, show dynamic KPI cards based on the selected year / filters:

- **Global Average FDI Inflows (% GDP)**
- **Global Median FDI Inflows (% GDP)**
- **Selected Country FDI (% GDP)**
- **Selected Country Global Rank**
- **Selected Country Regional Rank**
- **Year-over-Year Change (percentage points)**
- **5-Year Average**
- **10-Year Average**
- **Countries with Positive FDI**
- **Countries with Negative FDI**

For Sri Lanka specifically, display:

- Latest available FDI inflows (% GDP)
- Previous-year value
- Change vs previous year
- 5-year average
- 10-year average
- Global percentile
- Regional percentile
- Highest historical value
- Lowest historical value
- Historical peak year
- Historical trough year

Do not manufacture figures when data is missing. Clearly show “N/A” or “Not available”.

## Dashboard Filters

Add interactive filters for:

- Country
- Region
- World Bank income group
- Year
- Year range
- Country group / peer group
- Positive vs negative FDI
- Top N / Bottom N

Include a **Reset Filters** button.

The country selector should support multi-select so users can compare several countries simultaneously.

## Page 1 — Executive Overview

Create an executive summary view containing:

### KPI section
Show the headline metrics described above.

### Main chart: Global FDI trend

Create a line chart showing the selected country's FDI inflows (% GDP) over time.

Allow the user to:

- Select one country
- Select multiple countries
- Change year range
- Highlight Sri Lanka
- Add the global median as a benchmark
- Add the regional average as a benchmark

### Global ranking

Create a horizontal bar chart showing the **Top 10 countries by FDI inflows (% GDP)** for the selected year.

Add a toggle for:

- Top 10
- Bottom 10

Clearly distinguish extremely high values from normal observations.

### Global map

Create a world choropleth map showing FDI inflows (% GDP) by country for the selected year.

Use a diverging scale so:

- Negative values
- Low positive values
- Moderate values
- High values
- Extreme values

are visually distinguishable.

Hover tooltip should show:

- Country
- Year
- FDI inflows (% GDP)
- Global rank
- Regional rank
- Change vs previous year

## Page 2 — Country Comparison

Create a dedicated comparison page.

Allow users to select up to 5–10 countries.

Show:

### Comparison line chart
FDI inflows (% GDP) over time for all selected countries.

### Latest-year ranking table

Columns:

| Rank | Country | Region | Income Group | Latest Year | FDI % GDP | YoY Change | 5Y Avg | 10Y Avg | Percentile |
|---|---|---|---|---|---:|---:|---:|---:|---:|

Enable sorting by every numeric column.

### Benchmark chart

Compare the selected country against:

- Global average
- Global median
- Regional average
- Income-group average

Use the latest common year.

## Page 3 — Sri Lanka Focus

Create a dedicated Sri Lanka analytical page.

Title:

**Sri Lanka FDI Performance**

Show a prominent Sri Lanka KPI section.

### Sri Lanka historical trend

Display FDI inflows (% GDP) from the earliest available year to the latest available year.

Annotate important peaks, troughs, and major changes.

### Benchmarking

Compare Sri Lanka against:

- Global average
- South Asia average
- South Asian countries individually
- Sri Lanka's World Bank income-group average, where classification data is available

### Sri Lanka ranking

Show Sri Lanka's:

- Global rank
- South Asia rank
- Global percentile
- South Asia percentile

for the selected year.

### Peer comparison

Create a chart comparing Sri Lanka against South Asian economies.

Use a selectable peer list so the user can add/remove countries.

### Recent performance

Calculate:

- 1-year change
- 3-year change
- 5-year change
- 5-year CAGR only where mathematically meaningful
- 5-year average
- 10-year average
- Maximum
- Minimum
- Standard deviation
- Range

Clearly distinguish **percentage-point changes** from **percentage growth rates**.

## Page 4 — Global Rankings

Create a ranking explorer.

Users should be able to select a year and see:

### Top performers
Top 10 / Top 20 / Top 50 countries by FDI inflows (% GDP).

### Bottom performers
Bottom 10 / Bottom 20 / Bottom 50.

### Biggest improvers

Rank countries by change in FDI inflows (% GDP) between two user-selected years.

Example:

**2015 → 2025 change**

### Biggest deteriorations

Rank countries with the largest declines between the selected start and end year.

### Most consistent performers

Calculate a consistency metric based on the user's selected period, such as:

- Average FDI
- Standard deviation
- Coefficient of variation where appropriate
- Number of positive years
- Number of negative years

Do not interpret a high raw FDI value automatically as “better”; label the metric neutrally as **FDI inflows (% of GDP)**.

## Page 5 — Regional & Income-Group Analysis

Create aggregated comparisons by:

- World region
- Income group

Show:

### Regional trend

Line chart of average FDI inflows (% GDP) by region over time.

### Regional comparison

Bar chart of latest-year average and median FDI inflows (% GDP).

### Income-group comparison

Compare:

- Low income
- Lower-middle income
- Upper-middle income
- High income

Use both average and median because country-level FDI can contain extreme outliers.

### Selected country vs peer group

Show the selected country alongside:

- Peer-group average
- Peer-group median
- Peer-group 25th percentile
- Peer-group 75th percentile

## Page 6 — Volatility & Outliers

Create an analytical page focused on unusual FDI behavior.

### Volatility

Calculate rolling volatility, for example:

- 3-year standard deviation
- 5-year standard deviation

Rank countries by volatility.

### FDI stability

Create a scatter plot:

**X-axis:** 5-year average FDI inflows (% GDP)

**Y-axis:** 5-year standard deviation

**Bubble size:** latest-year FDI

This should identify:

- High FDI / low volatility
- High FDI / high volatility
- Low FDI / low volatility
- Low FDI / high volatility

### Outlier detection

Flag unusually large annual changes.

For example, define an outlier as an annual movement beyond a statistically appropriate threshold such as:

**absolute change > 2 standard deviations from the country's historical annual change**

Allow the threshold to be configurable.

Show:

- Country
- Year
- Previous FDI
- Current FDI
- Change
- Z-score / outlier score

## Page 7 — Time-Series Explorer

Allow users to select:

- Country
- Start year
- End year

Then display:

- Annual FDI
- YoY change
- 3-year rolling average
- 5-year rolling average
- Historical maximum
- Historical minimum
- Average
- Median
- Standard deviation

Provide a detailed downloadable table.

## Important Calculations

Create the following calculated metrics where the underlying data is sufficient:

### YoY change
Current year FDI minus previous year FDI.

Express this as **percentage points**, not percent growth.

### Multi-year change
Ending FDI minus starting FDI.

### Average
Arithmetic mean over the selected period.

### Median
Median over the selected period.

### Standard deviation
Standard deviation over the selected period.

### Rolling average
3-year and 5-year rolling averages.

### Rank
Country rank for the selected year.

Handle ties appropriately.

### Percentile
Country's percentile position relative to the selected comparison group.

### Positive-year ratio
Number of years with positive FDI divided by number of years with available observations.

### Peak / trough
Highest and lowest observed FDI values and corresponding years.

## Data Quality Handling

Treat missing observations as missing, not zero.

Do not calculate averages using missing observations as zero.

Display the number of countries contributing to aggregate statistics.

Where possible, show:

- Number of observations
- Missing-data count
- Latest available year
- Source

Allow the dashboard to warn users when countries do not have comparable latest-year observations.

Do not compare countries using different years without clearly labeling the comparison.

For cross-country rankings, default to the **latest common selected year**, but also allow users to explicitly select a year.

## Outlier Handling

Do not automatically remove extreme observations.

Extreme FDI values may represent genuine economic events.

Show them, flag them, and provide context instead of silently winsorizing or deleting them.

Consider providing an optional toggle:

**Include / Exclude extreme outliers from aggregate statistics**

while keeping the default as **Include**.

## Visual Design

Use a clean, modern economic-data aesthetic.

Recommended structure:

**Header**
Dashboard title + source + latest data year.

**Filter bar**
Country | Region | Income Group | Year | Period | Peer Group | Reset

**KPI row**

**Main analytical visualization**

**Supporting charts**

**Detailed table**

Use consistent number formatting:

- FDI: 1–2 decimal places
- Percentage-point changes: 1–2 decimals
- Rankings: integers
- Country counts: integers

Use clear labels such as:

**FDI inflows (% of GDP)**

rather than ambiguous labels such as “FDI”.

Tooltips should contain useful context rather than repeating axis labels.

## Interactivity

Include:

- Cross-filtering
- Hover tooltips
- Drill-down from region → country
- Click-to-filter
- Multi-country selection
- Dynamic ranking
- Dynamic year selection
- Dynamic peer selection
- Reset filters
- Download/export data
- Download chart where supported

When a country is selected in one visual, update the other visuals accordingly.

## Executive Insights

Add a dynamic **Key Insights** panel that automatically generates concise observations such as:

- “Sri Lanka's FDI inflows are X percentage points below the South Asia median.”
- “Country X ranks Yth globally in the selected year.”
- “FDI increased/decreased by X percentage points over the selected period.”
- “Country X's 5-year volatility is higher/lower than its peer group.”
- “The selected country is in the top/bottom X% globally.”

Only generate an insight when the underlying data supports it.

Avoid causal claims such as “FDI fell because of policy uncertainty” unless explanatory data has separately been provided.

## Source & Methodology Panel

Include a clearly visible methodology section.

Source:

**World Bank — World Development Indicators**

Indicator:

**BX.KLT.DINV.WD.GD.ZS**

Definition:

**Foreign direct investment, net inflows (% of GDP)**

Explain that the indicator measures net FDI inflows relative to GDP and is sourced from IMF balance-of-payments data supplemented by World Bank/OECD estimates.

Also disclose:

- Annual frequency
- Data coverage
- Latest available year
- Missing-value treatment
- Ranking methodology
- Regional aggregation methodology
- Volatility methodology
- Outlier methodology

## Dashboard Success Criteria

The finished dashboard should allow a user to answer, within a few clicks:

1. What is Sri Lanka's latest FDI inflow as a % of GDP?
2. How has Sri Lanka's FDI performance changed over time?
3. How does Sri Lanka compare with South Asian countries?
4. How does Sri Lanka rank globally?
5. Which countries currently have the highest FDI inflows relative to GDP?
6. Which countries have improved the most over the selected period?
7. Which countries show the greatest FDI volatility?
8. How does the selected country's FDI compare with its regional and income-group peers?
9. What were the historical peak and trough years?
10. Are the latest observations directly comparable across countries?

Prioritize analytical clarity over decoration. The dashboard should tell a coherent economic story while allowing users to explore the underlying data themselves.