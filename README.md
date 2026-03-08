# Data Visualization Portfolio
### R · Python · Shiny · Streamlit · Plotly · ggplot2

A collection of interactive data dashboards and visualization projects built to demonstrate
analytical depth, design quality, and business communication skills.
Each project targets a real-world business domain and answers concrete analytical questions
using publicly available data.

---

## Portfolio Structure

| # | Project | Tool | Dataset | Domain | Status |
|---|---------|------|---------|--------|--------|
| 1a | [Sales Intelligence Dashboard](#1a-sales-intelligence-dashboard) | R Shiny | Superstore (Kaggle) | Retail / E-commerce | 🔨 In Progress |
| 1b | [Brazilian E-Commerce Dashboard](#1b-brazilian-e-commerce-dashboard) | Python Streamlit | Olist (Kaggle) | Retail / E-commerce | ⬜ Planned |
| 2 | Geospatial Health Map | R Shiny | WHO GHO | Public Health | ⬜ Planned |
| 3 | Automated Research Report | Quarto | Eurostat | Policy / Research | ⬜ Planned |
| 4 | Financial Market Tracker | Python Plotly Dash | Yahoo Finance API | Finance | ⬜ Planned |
| 5 | Survey Results Visualizer | R (ggplot2) | Afrobarometer | Social Research | ⬜ Planned |
| 6 | Climate & Emissions Dashboard | R Shiny | UNDATA / Global Carbon Project | Environment | ⬜ Planned |
| 7 | ML Model Explainability Dashboard | Python Streamlit | UCI ML Repository | Data Science | ⬜ Planned |
| 8 | HR / People Analytics Dashboard | R Shiny | IBM HR Attrition (Kaggle) | Human Resources | ⬜ Planned |
| 9 | Animated Data Story | R (gganimate) | Gapminder | Global Development | ⬜ Planned |
| 10 | Parameterized Report Generator | Quarto + officer | World Bank API | Consulting / Reporting | ⬜ Planned |

---

## Project Details

---

### 1a. Sales Intelligence Dashboard

**Tool:** R Shiny · Plotly · DT
**Data:** [Superstore Sales Dataset — Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)
**Domain:** Retail / E-commerce
**Live Demo:** *(deploy link — shinyapps.io)*
**Folder:** `01a_superstore_shiny/`

#### Business Questions Answered

**Revenue & Profitability**
- What is total revenue, profit, and margin across any selected period?
- Which months and seasons consistently drive the highest revenue?
- Is the business growing year-over-year across product categories?
- Where is money being lost — which products or segments run negative profit?

**Product & Category**
- Which sub-categories generate the most revenue but lowest (or negative) profit?
- Does discounting hurt profit margin — and at what discount threshold does it break?
- Which category performs most consistently across all regions and segments?

**Customer & Segment**
- Which customer segment (Consumer, Corporate, Home Office) drives the most value?
- Are certain segments more profitable, or just higher volume?
- Which segment responds worst to discounting?

**Geography**
- Which US states and regions generate the most revenue and profit?
- Are there high-revenue states with poor underlying margins?
- Which regions are underperforming relative to their order volume?

**Operations**
- What is the most-used shipping mode, and how has the mix shifted over time?
- Does shipping mode correlate with profit margin?

#### Dashboard Tabs

| Tab | Key Charts |
|-----|------------|
| Overview | KPI cards, monthly revenue + orders dual-axis, segment donut |
| Categories | Top 15 sub-categories bar, profit margin heatmap, sales vs profit bubble |
| Geography | US choropleth by state, top 10 states bar |
| Trends | YoY category lines, shipping mode area stack, discount vs profit scatter |
| Data | Searchable, paginated order-level table |

#### Stack

```
shiny · bslib · plotly · shinyWidgets · DT · dplyr · lubridate · scales · tidyr
```

#### Setup

```r
# 1. Download dataset → save as data/superstore_raw.csv
# 2. Install dependencies
source("install_packages.R")
# 3. Clean data
source("R/prep_data.R")
# 4. Run app
shiny::runApp()
```

---

### 1b. Brazilian E-Commerce Dashboard

**Tool:** Python Streamlit · Plotly · Folium
**Data:** [Olist Brazilian E-Commerce — Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
**Domain:** Retail / E-commerce
**Live Demo:** *(deploy link — Streamlit Cloud)*
**Folder:** `01b_olist_streamlit/`

> ⬜ In development — see Project 1a above for the R Shiny implementation.

#### Planned Business Questions

- Which Brazilian states drive the highest order volume and revenue?
- What is the relationship between delivery time and customer review score?
- Which product categories have the worst on-time delivery rates?
- How does seller location affect shipping performance?
- What does the monthly order trend look like across 2017–2018?

---

## Technical Stack Summary

| Layer | R | Python |
|-------|---|--------|
| App framework | Shiny | Streamlit · Plotly Dash |
| Charting | Plotly · ggplot2 · gganimate | Plotly · Matplotlib |
| Maps | leaflet · sf | Folium · geopandas |
| Tables | DT | st.dataframe · AgGrid |
| Reporting | Quarto · officer | Jinja2 · WeasyPrint |
| Data wrangling | dplyr · lubridate · tidyr | pandas · numpy |
| APIs | httr · wbstats | requests · yfinance · wbdata |

---

## Design Philosophy

Every dashboard in this portfolio is built around three principles:

**1. Answer real business questions first.**
Charts exist to answer questions, not to demonstrate technical skill.
Each project starts from a defined list of analytical questions a business stakeholder would actually ask.

**2. Interactivity with purpose.**
Filters, sliders, and drill-downs are included only where they let the user explore a meaningful dimension — not as decoration.

**3. Production-grade aesthetics.**
Dark themes, consistent typography, and deliberate color palettes.
These are portfolio pieces — they need to look like something a client would pay for.

---

## About

Built by **Adu Grand** — founder of [EU StudyAssist](https://eustudyassist.com), Lead R Instructor,
and data visualization practitioner working across education, environmental research, and
international student mobility.

Available for freelance data visualization projects on Upwork.

**Tools:** R · Python · Shiny · Streamlit · Quarto · ggplot2 · Plotly · SQL · GIS
**Contact:** *(your contact / Upwork profile link)*

---

*Last updated: March 2026*
