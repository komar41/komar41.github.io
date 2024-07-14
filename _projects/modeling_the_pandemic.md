---
layout: page
title: Modeling the Pandemic
description: Visualizing impact of COVID in Chicago, using socio- demographic and COVID data
img: "assets/img/projects/modeling_the_pandemic/thumbnail.png"
importance: 7
category: Other
---

<h5><u>Access this project</u></h5>
<b>GitHub repo: </b> <a href='https://github.com/uic-cs418/modeling-the-pandemic'>https://github.com/uic-cs418/modeling-the-pandemic</a> <br>
<b>Tools used: </b> NumPy, pandas, geopandas, matplotlib, seaborn, beautifulSoup, scikit-learn.

<p align='justify'>
The aim of this project was to model the impact of COVID-19 in Chicago neighborhoods, using sociodemographic data (age, income, education, etc.) and COVID-19 statistics (hospitalizations, deaths, etc.). The sociodemographic and COVID-19 data used here is for each ZIP code.
</p>

<h5><u>Data Collection & Wrangling</u></h5>
<p align='justify'>
The following steps were performed to clean the dataset:
<ul>
    <li>Collecting Covid death and case data for individual zipcodes, while sociodemographic data was available for counties or census tracts. To align granularity, sociodemographic data was scraped based on zipcodes from the Census Reporter <a href="https://censusreporter.org/profiles/86000US60607-60607/">website</a>.</li>
    <li>For Chicago, instances with 'Manner of Death' as 'ACCIDENT' or 'SUICIDE' were removed from the Covid death data.</li>
    <li>Chicago's zipcode-based boundary data, used for visualizing Covid impact on individual zipcodes, was obtained from the Chicago Data Portal. Instances where zipcodes were outside Chicago were removed from both Covid death and case data.</li>
    <li>Date columns were converted to datetime type.</li>
    <li>Unnecessary columns were removed from both Covid case and death datasets.</li>
    <li>Covid deaths and cases were aggregated for all zipcodes.</li>
    <li>Covid deaths and cases were merged with Sociodemographic data.</li>
    <li>Normalization of Covid deaths and cases was performed by each zipcode's population, resulting in values rounded to two decimal points (cases per 1,000 / deaths per 1,000).</li>
</ul>
</p>

<h5><u>Exploratory Data Analysis & Visualization</u></h5>
<p align='justify'>
<b>Time series analysis.</b> In the beginning of 2022, number of cases nearly rose to 50,000 per day which was far more than the initial Covid outbreak.
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/uic-cs418/modeling-the-pandemic/blob/main/assets/time-series.png?raw=true" alt="Time series analysis" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>

<p align='justify'>
<b>Geospatial analysis.</b> The neighborhood with zipcode 60604 had the most number of covid cases per 1,000 population. Regarding covid death rates, Chicago's south side is more affected than the north.
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/uic-cs418/modeling-the-pandemic/blob/main/assets/geospatial.png?raw=true" alt="Geospatial analysis" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>

<p align='justify'>
<b>Correlation analysis.</b> It is evident, that there is some correlation with economic standing of a neighborhood and the impact of Covid-19.
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/uic-cs418/modeling-the-pandemic/blob/main/assets/correlation.png?raw=true" alt="Correlation analysis" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h5><u>Data Modeling</u></h5>
<p align='justify'>
<b>Random forest regression</b> (RFR) model was used to predict COVID-19 deaths per capita as a function of sociodemographic variables in each zipcode. The RFR was poor at predicting extreme values (death rates that were either zero or much higher than usual). Therefore, the final model is trained on data filtered to remove zipcodes with death rates of either zero or greater than the 95th percentile. This resulted in a training error rate of 0.29 deaths per thousand people and a test error rate of 0.78 deaths per thousand people.
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/uic-cs418/modeling-the-pandemic/raw/main/assets/rfr.png" alt="Random forest regression" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<p align='justify'>
<b>Principal components analysis</b> (PCA) was used to help visualize the distribution of COVID-19-related death rates in the multivariate sociodemographic dataspace. There is not an obvious pattern in the distribution of death rates over the first two principal components. One reason for this may be that the zipcodes represented here include several different types of areas (e.g., rural, urban, and suburban) and the relationship between sociodemographic variables and COVID-19 death rates may not be consistent across all of these areas.
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/uic-cs418/modeling-the-pandemic/blob/main/assets/pcp.png?raw=true" alt="Principal components analysis" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h5><u>Takeaways</u></h5>
<p align='justify'>
<ul>
    <li>Household income and housing value have a negative correlation with Covid death rate, while poverty level has a positive correlation with Covid death rate.</li>
    <li>The percentage of people taking public transit to work seemed to be the most important feature in predicting Covid across the cities and states.</li>
    <li>Other important features include ethnicity, owning vs renting, population density, poverty level and housing value.</li>
    <li>Our random forest regression model predicted Covid deaths with a training error rate of 0.29 (deaths per 1000) and a test error rate of 0.78 (deaths per 1000) on the new dataset.</li>
    <li>The model can be further improved by breaking it down by the type of area it is predicting Covid death rates for (urban or rural).</li>
</ul>
</p>
<p align='justify'>
To get more details about the project look into this <a href="https://github.com/uic-cs418/cs418-spring22-bored-grad-yacht-club/blob/main/CS418_final_report.ipynb">notebook</a> and <a href="https://github.com/uic-cs418/modeling-the-pandemic/blob/main/Reports%20%26%20Presentations/CS418_final_presentation.pdf">ppt</a>.
</p>
<p align='justify'>
<b>Group:</b> Bored Grad Yacht Club
</p>
<h5><u>Team Members:</u></h5>
<p align='justify'>
<ul>
    <li>Kazi Shahrukh Omar</li>
    <li>Christopher Owen</li>
    <li>Abdul Rafey Siddiqui</li>
    <li>Nguyen Hoa Pham</li>
    <li>Gautam Kushwah</li>
</ul>
</p>
