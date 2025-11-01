# DSA210 Istanbul Mobility Project
**Analyzing the Impact of Weather and Special Days on Istanbul Public Transport**  
_Fall 2025 • DSA210 Term Project_

---

## Project Summary
This project explores how **weather conditions** and **special days** (such as national holidays, exam periods, or major events) influence **public transport usage in Istanbul**.  
By combining and analyzing open data from multiple sources, the project aims to uncover meaningful patterns in passenger volume fluctuations and provide insights that can help **municipalities and urban planners** make better data-driven decisions.

---

## Motivation
Every day, millions of Istanbul residents commute using public transport.  
However, usage patterns fluctuate dramatically—sometimes due to **rainy weather**, **extreme temperatures**, or **special holidays**.  
This project aims to **quantify and visualize** these dynamics to better understand:

- How daily ridership changes with weather conditions  
- The influence of holidays and weekends on passenger flow  
- Which lines or time periods experience the biggest variations  

By revealing these relationships, the project contributes to smarter and more responsive **urban mobility planning**.

---

## Data Sources
All datasets are **publicly available**:

| Source | Description | URL |
|--------|--------------|-----|
| **İBB Open Data Portal** | Daily passenger traffic and transportation metrics | [data.ibb.gov.tr/dataset/istanbul-trafik-indeksi](https://data.ibb.gov.tr/dataset/istanbul-trafik-indeksi) |
| **Meteoroloji Genel Müdürlüğü (MGM)** | Daily weather data: temperature, precipitation, and wind | [mgm.gov.tr/tahmin/il-ve-ilceler.aspx?il=İstanbul](https://www.mgm.gov.tr/tahmin/il-ve-ilceler.aspx?il=İstanbul) |
| **Public Holidays & Special Days Calendar** | National holidays, school start days, exam dates, and special events | Custom dataset (manually created) |

---

## Data Gathering and Preparation Plan
**Step 1:** Download daily public transportation data from İBB Open Data Portal  
**Step 2:** Collect Istanbul’s daily weather data from MGM  
**Step 3:** Create a custom calendar dataset of holidays and special events  
**Step 4:** Merge all data chronologically into a single timeline dataset  
**Step 5:** Clean missing or erroneous data and extract weekly/seasonal patterns  

**Final Dataset Columns:**
| Date | Passenger_Count | Temperature | Rain | Wind | Is_Holiday | Event_Type |
|------|------------------|--------------|------|------|-------------|-------------|

---

## Planned Analysis Steps
1. **Trend and Seasonality Analysis**  
   - Examine long-term changes and weekly/seasonal fluctuations in ridership.
2. **Weather Correlation Analysis**  
   - Identify relationships between weather variables (rainfall, temperature) and passenger counts.  
   - Hypothesis example: _“Passenger numbers decrease on rainy days.”_
3. **Special Day Effect**  
   - Compare weekday/weekend and holiday passenger levels.  
   - Analyze changes during major events (e.g., match days, national holidays).
4. **Visualization**  
   - Use Python (Pandas, Matplotlib, Seaborn) to create time series plots, heatmaps, and correlation charts.

---

## Expected Findings
- Decrease in passengers during **rainy or extremely hot days**  
- Significant drop in ridership on **holidays and Sundays**  
- Increase in ridership near **event venues** during special occasions  
- Station-based variability linked to geographic or demographic factors

---

## Limitations and Future Steps
- Currently at **data planning stage** — data collection begins **November 2025**  
- Possible limitations:  
  - Incomplete or inconsistent station-level data  
  - Missing weather records for specific dates  
  - Time constraints for comprehensive model testing  

**Next Steps:**
- Begin data merging and cleaning  
- Perform exploratory data analysis (EDA)  
- Share reproducible code and visualizations on GitHub  

---

## Final Note
This project takes a **relationship-based and visualization-oriented** approach rather than complex modeling.  
The goal is to provide **clear, interpretable insights** into Istanbul’s transportation dynamics.  
All scripts, datasets, and figures will be shared transparently on this repository.

---

## Tools and Libraries
- **Python** → `Pandas`, `NumPy`, `Matplotlib`, `Seaborn`
- **Jupyter Notebook**
- **GitHub** for version control and public sharing

---

### Author
**Efe Furkan Ekmekci**  
_DS210: Data Science Applications • Fall 2025_

[View Source Code on GitHub](#)
