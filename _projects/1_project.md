---
layout: page
title: Subway
img: 'assets/img/projects/subway/thumbnail.png'
description: CTA ridership data visualization (Halsted, O'Hare, and Sox 35th station)
importance: 1
category: Other
---

<h5><u>Access this project</u></h5>
<b>Demo URL:</b> <a href='https://ktqjmz-kazi0shahrukh-omar.shinyapps.io/cs424-project1-kzo'>https://ktqjmz-kazi0shahrukh-omar.shinyapps.io/cs424-project1-kzo/</a> <br>
<b>Introduction video:</b> <a href='https://youtu.be/crEsxcrTsXU'>https://youtu.be/crEsxcrTsXU</a> <br>
<b>GitHub repo:</b> <a href='https://github.com/komar41/CS-424-Project-1-kzo'>https://github.com/komar41/CS-424-Project-1-kzo</a> <br>
<b>Tools used:</b> R and Shiny.

<p align='justify'>
This project is intended for visualizing the trends and interesting patterns in Chicago 'L' Station ridership data of three CTA stations in Chicago namely: UIC-Halsted, O'Hare, and Sox-35th. UIC–Halsted (formerly Halsted or U of I-Halsted) serves the University of Illinois at Chicago, the University Village neighborhood, and the Greektown neighborhood all located in the Near West Side. O'Hare station is located at O'Hare International Airport. The Sox-35th station is situated at 142 West 35th Street in the Armour Square neighborhood. Currently, the station serves Guaranteed Rate Field, the stadium of the Chicago White Sox, and takes its name from this location.
</p>

<h5><u>User Interface</u></h5>
<p align='justify'>
The <b>overview</b> page is to give users an overview of ridership data of the three CTA stations from the year 2001 to 2021. First, users will need to select a particular station. The yearly bar chart on the left will give a general overview of how ridership data in a chosen CTA station changed over the years. On the right side, users can choose between three chart types: daily, monthly, or weekdays. Users also have to select a particular year for which the chart on the right side will be displayed. Users can also see the raw data below each chart.
</p>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/subway/overview/Overview 1.png" title="overview" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Overview page
</div>

<p align='justify'>
The <b>comparison</b> page gives a quick comparison of ridership data between two stations. Users can select station, chart type, and year filter for charts on both left and right sides. Here also users can see the raw data below each chart.
</p>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/subway/overview/Overview 2.png" title="comparison" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Comparison page
</div>

<p align='justify'>
On the <b>interesting findings</b> page, users can choose to see some of the interesting insights found from the ridership data of these three CTA stations. For example, if user picks the option "March 2020", they will see how the CTA ridership declined in all three stations due to the covid outbreak starting March 2020.
</p>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/subway/overview/Overview 3.png" title="findings" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Interesting findings page
</div>

<h5><u>About the Data</u></h5>
Data source: <a href='https://data.cityofchicago.org/Transportation/CTA-Ridership-L-Station-Entries-Daily-Totals/5neh-572f'>Chicago Data Portal</a>. The file size is 39MB.

<p align = 'justify'>
The original data is very detailed and contains ridership data of all the CTA stations in Chicago starting 2001 to 2021. The dataset shows entries at all turnstiles, combined, for each station. Daytypes are as follows: W = Weekday, A = Saturday, U = Sunday/Holiday.
</p>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/subway/data/Data 1.png" title="data" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Sample data
</div>

<p align = 'justify'>
For the purpose of this project, ridership data is filtered for three particular stations namely: UIC-Halsted, O'hare, and Sox-35th. After filtering the data, three separate TSV files were created for each of the stations. Later, these three TSV files were used to create the visualizations of the app. R language was used to read and filter the dataset. The code used for filtering the original dataset and creating the TSV files is provided below:
</p>


---
    library(dplyr)

    cta <- read.csv(file = "CTA_-_Ridership_-__L__Station_Entries_-_Daily_Totals.tsv", sep = "\t", header = TRUE)

    cta_halsted <- cta %>% filter(stationname == "UIC-Halsted")

    write.table(cta_halsted, file = "cta_halsted.tsv", row.names=FALSE, sep="\t")

    cta_ohare <- cta %>% filter(stationname == "O'Hare Airport")

    write.table(cta_ohare, file = "cta_ohare.tsv", row.names=FALSE, sep="\t")

    cta_sox <- cta %>% filter(stationname == "Sox-35th-Dan Ryan")

    write.table(cta_sox, file = "cta_sox.tsv", row.names=FALSE, sep="\t")


<br>
<h5><u>Interesting Findings</u></h5>

<p align = 'justify'>
    <b>Findings 1:</b> Starting August 23, 2021 UIC reopened for in-person classes for the first time since Covid lockdown restrictions.
</p>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/subway/findings/Findings 1.png" title="data" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Findings 1
</div>


<p align = 'justify'>
    <b>Findings 2:</b>  Starting March 2020 CTA ridership declined due to the covid outbreak. However, throughout the year O'Hare was the busiest among the three stations due to being located at the O'Hare International Airport.
</p>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/subway/findings/Findings 2.png" title="data" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Findings 2
</div>


<p align = 'justify'>
    <b>Findings 3:</b> On March 24, 2014 at 2:50 a.m. local time, a CTA passenger train overran the bumper at O'Hare, injuring 34 people. Following the accident, the line between O'Hare and Rosemont was closed, with a replacement bus service in place.
</p>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/subway/findings/Findings 3.png" title="data" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Findings 3
</div>


<p align = 'justify'>
    <b>Findings 4:</b> In July 2008, service was suspended on the Blue Line for approximately 3 weeks between the O’Hare and Rosemont stations for construction.
</p>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/subway/findings/Findings 4.png" title="data" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Findings 4
</div>


<p align = 'justify'>
    <b>Findings 5:</b> The coldest temperature in Chicago in 34 years (-23°) was recorded on the morning of January 30, 2019 during a bitter cold couple of days. Presumably, UIC remained closed and thus the drop in CTA ridership.
</p>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/subway/findings/Findings 5.png" title="data" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Findings 5
</div>


<p align = 'justify'>
    <b>Findings 6:</b> During each year, the lowest ridership recorded at Halsted station is 25th December. (With exception of polar vortex on January 30, 2019 and Covid outbreak in 2020 and 2021)
</p>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/subway/findings/Findings 6.png" title="data" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Findings 6
</div>


<p align = 'justify'>
    <b>Findings 7:</b> O'Hare station was temporarily closed from Sep 28, 2019 to Oct 6, 2019 due to construction (signal improvements).
</p>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/subway/findings/Findings 7.png" title="data" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Findings 7
</div>


<p align = 'justify'>
    <b>Findings 8:</b> On September 24, 2016, Chicago White Sox stadium had a record attendance of 47,754 hosting a concert of Chance the Rapper.
</p>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/subway/findings/Findings 8.png" title="data" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Findings 8
</div>


<p align = 'justify'>
    <b>Findings 9:</b> October 22, 2005: The first-ever World Series game in Chicago White Sox stadium. The White Sox get their first World Series game victory since 1959, defeating the Houston Astros 5–3. Attendance: (41,206)
    <br>

    October 23, 2005: The stadium hosted Game 2 of the World Series. The Sox won 7–6. Additionally, The Sox would win the next two games in Houston to win their first World Series title since 1917. Attendance: (41,432)
</p>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/subway/findings/Findings 9.png" title="data" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Findings 9
</div>


<p align = 'justify'>
    <b>Findings 10:</b> October 10, 2021: Guaranteed Rate Field hosted its first playoff game since 2008 with the White Sox facing the Houston Astros in the ALDS with the Sox trailing 2 games to none. (Attendance: 40,288)
    <br>

    October 12, 2021: Guaranteed Rate Field hosted game 4 of the ALDS between the White Sox and Astros. The Astros won 10-1 and advanced to the ALCS. (Attendance: 40,170)
</p>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/subway/findings/Findings 10.png" title="data" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Findings 10
</div>
<br>

<h5><u>Setup and Installations</u></h5>

<u><b>Install R:</b></u> <br>

Download R from <a href="https://www.r-project.org/">https://www.r-project.org/</a> (4.1.2). Click "download R".

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/subway/installation/1.png" title="install" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    R installation
</div>

You can select the default link <a href="https://cloud.r-project.org">https://cloud.r-project.org/</a>.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/subway/installation/2.png" title="install" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Select default link
</div>

Download and install a version that match your OS.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/subway/installation/3.png" title="install" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Match OS installation
</div>

<u><b>Install RStudio:</b></u> <br>

Download and install RStudio from <a href="https://rstudio.com/products/rstudio/">https://rstudio.com/products/rstudio/</a>.

<div class="row">
    <div class="col-sm mt-3 mt-5md-0">
        {% include figure.html path="assets/img/projects/subway/installation/4.png" title="install" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    RStudio installation
</div>

Download the free version.

<div class="row">
    <div class="col-sm mt-3 mt-5md-0">
        {% include figure.html path="assets/img/projects/subway/installation/5.png" title="install" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    RStudio free version
</div>

<u><b>Setup the project:</b></u> <br>

Create a folder in your local machine where you want the project to locate at. Open the terminal and set the direction to the created folder. Run the following command: `git clone https://github.com/komar41/Subway.git`.

<div class="row">
    <div class="col-sm mt-3 mt-5md-0">
        {% include figure.html path="assets/img/projects/subway/installation/6.png" title="install" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    git clone
</div>

Open RStudio. Go to "File" and select "Open Project".

<div class="row">
    <div class="col-sm mt-3 mt-5md-0">
        {% include figure.html path="assets/img/projects/subway/installation/7.png" title="install" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Open project in RStudio
</div>

Choose the project folder ("Subway") that you cloned from GitHub.

<div class="row">
    <div class="col-sm mt-3 mt-5md-0">
        {% include figure.html path="assets/img/projects/subway/installation/8.png" title="install" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Select project folder
</div>

Open the file "app.R" and press "Run App" button on RStudio. 

<div class="row">
    <div class="col-sm mt-3 mt-5md-0">
        {% include figure.html path="assets/img/projects/subway/installation/9.png" title="install" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Run app
</div>

Rstudio will tell you if you are missing some of the packages. When the pop-up shows up, click "Yes" to install all those packages.

<div class="row">
    <div class="col-sm mt-3 mt-5md-0">
        {% include figure.html path="assets/img/projects/subway/installation/10.png" title="install" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Install missing packages
</div>

After Installation of those packages, RStudio will start a Shiny app on your local machine.

<div class="row">
    <div class="col-sm mt-3 mt-5md-0">
        {% include figure.html path="assets/img/projects/subway/installation/11.png" title="install" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Shiny app in local machine
</div>