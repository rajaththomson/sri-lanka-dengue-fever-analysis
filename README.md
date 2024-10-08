# Sri Lanka Dengue Analysis

This repository contains an in-depth analysis of dengue cases in Sri Lanka, focusing on the relationship between weekly rainfall and the incidence of dengue fever. The project aims to identify lagged effects of rainfall on dengue outbreaks across various districts, with a significant emphasis on the Colombo district.

## Table of Contents
1. [Introduction](#introduction)
2. [Data Description](#data-description)
3. [Methodology](#methodology)
   - [Data Preprocessing](#data-preprocessing)
   - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
   - [Visualizations](#visualizations)
4. [Key Findings](#key-findings)

## Introduction
Dengue fever is a major public health concern in Sri Lanka, often exacerbated by climatic variations such as rainfall. This analysis seeks to explore how different rainfall patterns correlate with reported dengue cases, particularly in Colombo, over time. By examining lagged effects, this project provides insights into predicting dengue outbreaks and guiding preventative measures.

## Data Description
The analysis is based on three primary datasets:
- **Dengue Cases**: Weekly reported cases of dengue across various districts in Sri Lanka.
- **Rainfall Data**: Weekly rainfall measurements in millimeters for the same districts.
- **Weather Data**: Weekly weather and environmental data for districts in Sri Lanka.

The dataset covers the period from **2007** to **2024**.

## Methodology

### Data Preprocessing
Data preprocessing steps included:
- **Data Importation**: Loading datasets for dengue cases and rainfall measurements.
- **Data Cleaning**: Handling missing values and ensuring data consistency.
- **Date Handling**: Transforming date formats for easier analysis.
- **Creating Lagged Features**: Generating lagged rainfall variables (1 to 15 weeks) to evaluate their impact on dengue cases.

### Exploratory Data Analysis (EDA)
The exploratory analysis involved:
- **Statistical Summaries**: Analyzing descriptive statistics of dengue cases and rainfall.
- **Correlation Analysis**: Assessing the correlation between dengue cases and rainfall, including examining lagged effects.
- **Heatmap Creation**: Visualizing correlations to identify patterns.

### Visualizations
The visualizations produced include:

#### Time-Series Analysis of Dengue Cases
This analysis forecasts dengue cases using the **SARIMA** model, revealing predicted versus actual cases over time. The model captures weekly trends and seasonality in dengue incidence, highlighting notable deviations during significant external events:
- **COVID-19 Pandemic (March 2020)**: The pandemic disrupted typical dengue transmission patterns, influenced by lockdowns, changes in healthcare priorities, and decreased human mobility, leading to a divergence between predicted and actual dengue cases.
- **Vaccination Rollout (September 2021)**: The introduction of COVID-19 vaccines altered public health resource allocations, potentially affecting responses to dengue outbreaks and marking the end of lockdowns.
- **Floods (May 2017 & September 2019)**: Flooding events contributed to increased mosquito breeding sites, directly impacting dengue transmission.

#### Dengue Cases per 100,000 Population by District
- **Urbanization and Dengue Cases**: High urbanization areas like Colombo consistently reported higher dengue cases, suggesting a correlation between urbanization and increased dengue risk. Conversely, medium urbanization areas showed fewer cases, indicating a reduced impact of urbanization.
- **Monthly Trends**: 
  - **Peak in June**: Most districts exhibited high dengue cases in June, likely influenced by seasonal factors affecting mosquito populations.
  - **Exceptions**: Jaffna and Mannar showed extreme cases from November to January, indicating local factors influencing outbreaks during these months.
  
#### Regional Variations
- **Trincomalee and Batticaloa**: These districts had cases peaking from November to May, suggesting unique environmental or socioeconomic factors that warrant further investigation.

#### Spatial Visualization of Dengue Cases in Sri Lanka by Week
- **Insights**:
  - **Dengue Incidence in Colombo and Surrounding Districts**: A consistent trend of high dengue cases in Colombo and neighboring districts indicates potential spread mechanisms related to population mobility and common environmental conditions.
  - **Exception Cases**: Anomalies in northern and other regions suggest localized outbreaks or specific vector breeding sites differing from Colombo.

#### Effect of Lagged Rainfall on Dengue Cases
- **Insights**:
  - **Correlation between Rainfall and Dengue Cases**: The correlation between lagged rainfall and dengue cases increases from Lag 1 (0.05) to Lag 6 (0.18), emphasizing the influence of rainfall within the past 4 to 6 weeks on dengue transmission. This correlation decreases significantly by Lag 15 (-0.09).
  - **Biological Life Cycle of Mosquitoes**: The timing of rainfall impacts mosquito breeding cycles and transmission dynamics, highlighting the relevance of recent rainfall in predicting dengue cases.

### Rainfall and Dengue Correlation in Colombo: A Focused Examination
- **Insights**:
  - **Correlation Trend**: In Colombo, the correlation between dengue cases and lagged rainfall peaks at Lag 4 (0.26) and remains strong at Lags 5 and 6 (0.27), emphasizing the importance of localized models for understanding rainfall's impact on dengue.
  - **Declining Correlation Beyond Six Weeks**: Correlation values decline after Lag 6, suggesting that older rainfall events become less relevant for current dengue transmission.

## Key Findings
1. **Lagged Effects**: Rainfall from **4 to 6 weeks prior** significantly correlates with increased dengue cases, indicating a strong relationship between mosquito breeding conditions and past rainfall.
2. **District-Specific Trends**: The Colombo district consistently shows high dengue case rates, highlighting the need for targeted public health interventions.
3. **Rainfall Impact**: Moderate rainfall (between 100 mm and 200 mm) tends to correlate with higher dengue incidences, while extreme rainfall can reduce cases.
