# Activity 3: Create a BI Dashboard Using Gemini Canvas

In this activity, you will use Gemini Canvas to create a live BI dashboard from a Crunchbase investment dataset.

Replace `[DATASET LINK]` with your own Google Sheets or dataset link.

---

## Prompt 1: Create the Live Dashboard

Use the prompt block below.

```text
Act as a Senior Data Analyst.

Create a live BI dashboard using the dataset below:

[DATASET LINK]

Dashboard requirements:
- Connect the dashboard to the dataset so that changes in the datasheet are reflected in the visualizations.
- Analyze the available columns and choose the most useful charts automatically.
- Show key investment insights clearly.
- Include important KPIs such as total funding, number of companies, average funding amount, top sectors, top investors, and funding trends over time.
- Use clear chart titles and labels.
- Make the dashboard easy to understand for non-technical users.

Output:
Create the dashboard layout and visualizations in Gemini Canvas.
```

---

## Prompt 2: Add Interactive Filters

Use the prompt block below.

```text
Improve the dashboard by adding interactive filters.

Filter requirements:
- Add a filter for sector or industry.
- When a sector is selected, all charts and KPIs should update based on that selected sector.
- Allow users to clear the filter and return to the full dataset view.
- If possible, add additional useful filters such as funding year, country, funding stage, or investor type.
- Keep the dashboard simple and easy to use.

Output:
Update the existing dashboard with interactive filters.
```

---

## Prompt 3: Improve Dashboard Insights

Use the prompt block below.

```text
Review the dashboard as a Senior Data Analyst.

Improve it by adding:
- Short insight summaries for each major chart.
- A section showing top-performing sectors.
- A section showing companies with the highest funding.
- A section showing funding trends over time.
- Any data quality warnings, such as missing values or inconsistent sector names.

Keep the dashboard clean, professional, and easy to present.
```

