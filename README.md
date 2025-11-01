# DSA210 – Istanbul Mobility Project  
**Analyzing the Impact of Weather and Special Days on Istanbul Public Transport | DSA210 Fall 2025 Project**

---

## PROJECT SUMMARY
This project aims to search effects of special days and weather conditions to the public transportation.  
Main idea is to compare and merge daily passanger interference with daily weather conditions and special days and get meaningful pattern.

---

## MOTIVATION
Every day millions of people goes school, work or elsewhere by public transportation.  
But sometimes public transportation have huge human traffic, sometimes it changes to opposite way.  
Rainy weather, special holidays and weekends effect this situation more deeply.  
This project aims to understand dinamics of these type of changes.  
My aim is to provide effects of weather and special days to the public transportation with datas that I merged.  
In this way, I want to contribute to municipalities and transportation planners being able to anticipate such changes and make more efficient plans in the future.

---

## DATA SOURCES
The data I will use in this project will be publicly available.  
Data sources that I am gonna use:

1. **İBB Open Data Portal** – [Daily human traffic through public transportation](https://data.ibb.gov.tr/dataset/istanbul-trafik-indeksi)  
2. **Meteoroloji Genel Müdürlüğü (MGM)** – [Daily temperature, rain or wind information data for Istanbul](https://www.mgm.gov.tr/tahmin/il-ve-ilceler.aspx?il=İstanbul)  
3. **Public Holidays and Special Days Calendar** – National holidays, exam days, start of school like special days.

I am aiming to analyze these sources and merge collected data with timeline.

---

## DATA GATHERING AND PREPARATION PLAN
**Step 1:** From İBB open data portal I will download daily usage data of public transportation in Istanbul.  
**Step 2:** From MGM site I will gather Istanbul’s daily weather data.  
**Step 3:** I will create calendar file which includes national holidays and special days.  
**Step 4:** Combining all this data on a historical basis and making it analyzable.  
**Step 5:** Cleaning up missing or erroneous records and extracting weekly and seasonal characteristics.  

At the end of these steps we have a dataset that includes:  
Every day passenger number + weather condition + holiday information.

---

## PLANNED ANALYZE STEPS
1. Seeing the change in daily passenger numbers over time (trend and seasonality analysis)  
2. Examine the relationship between weather and passenger numbers (For example: is there a drop in passenger numbers on rainy days?)  
3. To test whether there are station-based differences on public holidays and weekends  
4. Visualizing the findings with graphics.

---

## EXPECTED FINDINGS
I expect a decrease in passenger numbers on rainy days;  
a decrease at certain times on very hot days;  
a significant decrease on holidays or Sundays;  
and an increase on certain routes during special events (For example: match days).

---

## LIMITATIONS AND FUTURE STEPS
I do not currently have actual data.  
I have only completed the data sources and planning phase at this stage.  
I will begin data downloading, cleaning, and initial analysis in November.  

Time constraints, missing station data, or gaps in weather data may limit the accuracy of the analysis.

---

## FINAL NOTE
This project aims to offer a simple but effective data approach to understanding daily transportation habits in Istanbul.  
Instead of complex modeling, a relationship-based perspective based on explanation and visualization will be done.  
The code and outputs obtained throughout the process will be shared transparently on GitHub.
