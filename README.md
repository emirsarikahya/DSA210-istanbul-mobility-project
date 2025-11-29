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
2. **OpenWeatherAPI** – [Daily temperature, rain information data for Istanbul](https://archive-api.open-meteo.com/v1/archive)  
3. **Public Holidays and Special Days Calendar** – National holidays and weekdends.

I am aiming to analyze these sources and merge collected data with timeline.

---

## DATA GATHERING AND PREPARATION PLAN
**Step 1:** From İBB open data portal I will download daily usage data of public transportation in Istanbul.  
**Step 2:** From openweather site I will gather Istanbul’s daily weather data.  
**Step 3:** I will create csv file which says when there is holiday.  
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



---

## HYPOTHESIS TESTING AND VISUALIZATION

Based on the data collected and analyzed, statistical t-tests were performed to validate the relationships between the variables. Visualizations were generated to inspect the distribution and mean differences.

### 1. Impact of Weather (Rain vs. Dry) on Passenger Numbers

To determine if rain significantly impacts public transport usage, we analyzed the daily passenger counts categorized by weather condition.

**Hypotheses:**
* **Null Hypothesis ($H_0$):** There is no significant difference in the average number of passengers between rainy days and dry days ($\mu_{rain} = \mu_{dry}$).
* **Alternative Hypothesis ($H_1$):** There is a significant difference in the average number of passengers between rainy days and dry days ($\mu_{rain} \neq \mu_{dry}$).

**Visual Analysis:**
Below, the boxplot and mean bar chart visualize the distribution and average passenger counts for rainy versus dry days.

![Rain vs Dry Distribution](screenshots/rain_vs_dry_boxplot.png)
![Rain vs Dry Average](screenshots/rain_vs_dry_mean_bar.png)

**Statistical Test Results:**
* **t-statistic:** 1.446041830594893
* **p-value:** 0.14907454286848537

**Conclusion:**
Since the **p-value (0.149)** is greater than the standard significance level of $\alpha = 0.05$, we **fail to reject the Null Hypothesis**.

* **Interpretation:** Both the visual overlaps in the boxplot and the statistical test suggest that rain does not significantly alter public transportation usage in Istanbul. This indicates that daily commuting habits (work/school) are inelastic and continue regardless of precipitation.

---

### 2. Impact of Day Type (Workday vs. Weekend/Holiday)

To confirm the effect of business days versus off-days (weekends and public holidays), a similar analysis was conducted.

**Hypotheses:**
* **Null Hypothesis ($H_0$):** There is no significant difference in the average number of passengers between workdays and weekends/holidays ($\mu_{workday} = \mu_{weekend}$).
* **Alternative Hypothesis ($H_1$):** There is a significant difference in the average number of passengers between workdays and weekends/holidays ($\mu_{workday} \neq \mu_{weekend}$).

**Visual Analysis:**
The difference in usage intensity is clearly visible in the following plots.

![Workday vs Offday Distribution](screenshots/workday_vs_offdays_boxplot.png)
![Workday vs Offday Average](screenshots/workday_vs_offdays_mean_bar.png)

**Statistical Test Results:**
* **t-statistic:** 11.499409613895953
* **p-value:** 2.0346914158481092e-22

**Conclusion:**
Since the **p-value ($2.03 \times 10^{-22}$)** is significantly lower than the significance level of $\alpha = 0.05$, we **reject the Null Hypothesis**.

* **Interpretation:** There is an extremely strong statistical difference between passenger numbers on workdays versus holidays. The boxplot shows a distinct separation in the medians, and the t-test confirms this difference is not due to chance. This confirms that the primary driver of public transport usage in Istanbul is routine commuting, which drops drastically during off-days.

