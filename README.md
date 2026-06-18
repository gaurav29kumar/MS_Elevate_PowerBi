# Air Quality Analysis Dashboard — Power BI

A Power BI report built during my Microsoft Elevate internship (Feb–Mar 2026, in collaboration with AICTE). The project focuses on analyzing air quality data across Indian states and locations, with a specific look at SO₂ and NO₂ emission levels, pollution risk, and data reliability over time.

---

## What This Report Does

The dashboard is spread across three pages, each serving a different analytical purpose:

**Page 1 — Emission Trends**
This is the main overview page. It has two line charts tracking SO₂ and NO₂ concentrations over time (broken down by year, quarter, month, and day), a KPI card showing state-level counts, and two slicers — one to filter by state/location and another to filter by emission reduction category. There's also a simulated SO₂ projection line layered onto the actual readings, which makes it easy to compare real vs. expected emission behavior.

**Page 2 — Location-Level Breakdown**
This page goes deeper into individual monitoring locations. A pivot table cross-references SO₂ readings by year and month. A detail table lists location, state, and average SO₂ values. The stacked bar chart shows the proportion of "dangerous" readings per location — so you can quickly spot which sites consistently report hazardous air quality.

**Page 3 — State & Reliability Overview**
A treemap that maps all monitoring stations by state and location, colored by data reliability score. It gives a bird's-eye view of where the data is solid and where readings might need to be taken with a grain of salt.

The report uses navigation buttons between pages so it feels more like an app than a static file.

---

## Key Metrics Tracked

- **SO₂ (Sulfur Dioxide)** — average and simulated values over time
- **NO₂ (Nitrogen Dioxide)** — trend over time
- **Is_Dangerous** — binary flag indicating whether a reading crossed a hazardous threshold
- **Emission Reduction** — categorical measure for filtering improvement trends
- **Data Reliability** — quality score for each monitoring station
- **Location & State** — geographic breakdown across Indian monitoring sites

---

## File

| File | Description |
|------|-------------|
| `Airquality.pbix` | Power BI Desktop report file (open with Power BI Desktop) |

---

## How to Open

1. Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
2. Clone or download this repository
3. Open `Airquality.pbix` in Power BI Desktop
4. The data is embedded in the file — no external database connection needed

---

## Context

This was built as part of the **Microsoft Elevate – Power BI for Business Applications** internship program, run in collaboration with AICTE (Feb 2026 – Mar 2026). The goal was to take raw environmental monitoring data and turn it into something a non-technical stakeholder could actually use — filter by location, spot dangerous zones, and track whether emissions are improving over time.

The `Simulated_So2` measure in particular was something I added to model what SO₂ levels would look like under a reduction scenario, which gave the trend page more analytical depth than just plotting raw readings.

---

## Tools Used

- Power BI Desktop
- DAX (for the `Simulated_So2` measure and aggregations)
- Power Query (data shaping and column transformations)
