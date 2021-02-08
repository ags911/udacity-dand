# The Truth About Airline Statistics
### by Darren Gidado

<a id='intro'></a>
## Introduction

#### What is the ASA?

ASA stands for 'American Statistical Association', ASA is the main professional organsiation for statisticians in the United States. The organization was formed in November 1839 and is the second oldest continuously operating professional society in the United States. Every other year, at the Joint Statistical Meetings, the Graphics Section and the Computing Section join in sponsoring a special Poster Session called The Data Exposition , but more commonly known as The Data Expo. All of the papers presented in this Poster Session are reports of analyses of a common data set provided for the occasion. In addition, all papers presented in the session are encouraged to report the use of graphical methods employed during the development of their analysis and to use graphics to convey their findings.

Quoted from citation: https://www.tandfonline.com/doi/abs/10.1198/jcgs.2011.1de

#### What is the ASA 2009 Data Expo?

The ASA Statistical Computing and Graphics Data Expo is a biannual data exploration challenge. Participants are challenged to provide a graphical summary of important features of the data. The task is intentionally vague to allow different entries to focus on different aspects of the data, giving the participants maximum freedom to apply their skills. The 2009 data expo consisted of flight arrival and departure details for all commercial flights on major carriers within the USA, from October 1987 to April 2008. This is a large dataset: there are nearly 120 million records in total, and takes up 1.6 gigabytes of space compressed and 12 gigabytes when uncompressed. The complete dataset and challenge are available on the competition website http://stat-computing.org/dataexpo/2009/.

Because the dataset is so large, we also provided participants introductions to useful tools for dealing with this scale of data: Linux command line tools, including sort, awk, and cut, and sqlite, a simple SQL database. Additionally, we provided pointers to supplemental data on airport locations, airline carrier codes, individual plane information, and weather.
This dataset reports flights in the United States, including carriers, arrival and departure delays, and reasons for delays, from 1987 to 2008.

Quoted from citation: https://www.tandfonline.com/doi/abs/10.1198/jcgs.2011.1de

#### Project Aims

This dataset reports flights in the United States, including carriers, arrival and departure delays, and reasons for delays, from 1987 to 2008. For our analysis, we are going to be using the three year period between 1989 to 1991 as our sample dataset as the whole dataset is too large to practically observe with Jupyter. Our goal is to ask many questions such as:

- How many flights are there?
- Which airlines have the most flights?
- What time of the week passengers fly the most?
- How does season change the frequency and the destination of travel?
- Which routes are the most popular?
- Which routes and airports experience the most delays?
- Which airports are the busiest in terms of inbound and outbound flights?
- Which popular routes are delayed the most?
- Which times are airports the busiest in terms of flights by each hour?
- How does flight distance affect departure and arrival delays?
- Which airline experiences the fewest delays?

<a id='conclusion'></a>
## Conclusion 📝

### 7.1. Interesting Findings

From our data, we can assess passengers fly more during the summer and least during the winter and more during midweek versus the weekend. The most popular time to travel for passengers is in the morning around 8:00. Most flights average a 110 minute flight time and an average distance is 632 miles. Interestingly, the average distance for flights increases during the winter months suggesting that passengers commute further to go on distant holidays or visit family and friends across the country. Airline carriers enjoy a competitive market with no more than 36% difference in total flights between carriers. Regarding carriers, we observed that flight delays increase with flight distance. Chicago O'Hare International is the busiest airport with over 1.5 million flights recorded over the 3 year period.

### 7.2. Project Answers

**How many flights are there?**\
15,031,014 flights.

**Which airlines have the most flights?**\
US Airways Inc.

**What time of the week passengers fly the most?**\
Monday to Friday.

**How does season change the frequency and the destination of travel?**\
Summer increases the frequency of average flights whilst winter decreases it.

**Which routes are the most popular?**
1. SFO - LAX | 69,180 Flights 
2. LAX - SFO | 68,754 Flights
3. LAX - PHX | 39,321 Flights

*LAX: Los Angeles Intl, SFO: San Fransisco Intl, PHX: Phoenix Sky Harbor Intl.*

**Which routes and airports experience the most delays?**\
GUC - HDN Gunisson to Haydon | 1980 minutes on average for route.\
PSE Mercedita Airport | 53.25 minutes delay on average is the highest for an airport.\
BQN Rafael Hernández Airport | -10.35 minutes delay (early) on average is lowest for an airport.

**Which airports are the busiest in terms of inbound and outbound flights?**\
Chicago O'Hare International.

**Which popular routes are delayed the most?**\
LAX - SFO |	68,754 Flights, 18.97 minutes delay on average.\
PHX - LAX |	38,756 Flights, 16.18 minutes delay on average.\
PHX - LAS |	30,778 Flights, 15.85 minutes delay on average.

**Which times are airports the busiest in terms of flights by each hour?**\
08:00 - 09:00 has over 1 million flights during the morning.

**How does flight distance affect departure and arrival delays?**\
Flight distance increases total departure and arrival delays with 0.221398 positive correlation.

**Which airline experiences the fewest delays?**\
Northwest Airlines.

### 7.3. Key Insights for Presentation

For the presentation, I decided to look at flight counts using simple vertical and horizontal bar charts before moving on to more complex plots for deeper analysis. I used an area plot for flight duration because it looked visually clearer than using a line chart. I used a histogram for the flight distance plot to keep things interesting since my plan was to use many different plot types for the slides. 

For total flights by carrier I decided to use a colourful pie chart which should catch the audiences attention since unique and vibrant colour selection is important. I also decided to explode the largest slice of the pie chart. For the delay section I used a combination of line charts and horizontal bar charts since it was the best way to show bivariate data that relies on categorical data. Next, I introduced a third variable which was categorical so I decided to use a heatmap. Heatmaps are great at showing multiple dimensions of data in a fun way, in our case it was for airport name, flight totals, and month. The darker the colour the more flights per grid box.

I used a combination chart to plot airlines vs month vs average distance. This allowed me to show multiple variables co-existing in the same axis clearly. Average flight delay vs distance used the scatterplot, another plot I was keen to try as it engages the audience with raw individual data points. This allowed us to use a line of best fit to intercept the points to see if there was a correlation visually. For routes by flights vs airline average delay it was the perfect time to use a grouped bar chart, I found some interesting colour palettes for my chart from coolor.co. I could plot multiple airlines for each route on the same bar axis and take an average of them if we wanted to. I used a swarm plot on the same data for another angle to see if we could find out more. Average airlines by delay had a similar treatment with the grouped bar chart instead replacing routes with airline carriers, this time I used a more modest colour palette. The random exploration at the end used simple bar charts again as they are a quick and easy to explore data.

#### References
Getting csv subdirectories: https://perials.com/getting-csv-files-directory-subdirectories-using-python/ \
Combine csv files: https://www.freecodecamp.org/news/how-to-combine-multiple-csv-files-with-8-lines-of-code-265183e0854/ \
Fix .info() display: https://www.geeksforgeeks.org/python-pandas-dataframe-info/ \
CMD: https://www.tomnash.eu/how-to-combine-multiple-csv-files-into-one-using-cmd/ \
Reset and drop index: https://stackoverflow.com/questions/39616424/pandas-reset-index-creating-level0-column \
Between values 1: https://stackoverflow.com/questions/31617845/how-to-select-rows-in-a-dataframe-between-two-values-in-python-pandas \
Between values 2: https://www.geeksforgeeks.org/python-pandas-series-between/ \
String Pad or str.pad: https://www.geeksforgeeks.org/python-pandas-series-str-pad/ \
String Slicing: https://geekflare.com/python-remove-last-character/ \
Datetime without date: https://stackoverflow.com/questions/32375471/pandas-convert-strings-to-time-without-date# \
Replace values: https://datatofish.com/replace-values-pandas-dataframe/ \
Dates to seasons: https://stackoverflow.com/questions/22615288/group-data-by-seasons-using-python-and-pandas \
Rename Index: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.rename_axis.html \
Sort Index by list: https://stackoverflow.com/questions/45389126/sort-index-by-list-python-pandas \
Loc: https://www.geeksforgeeks.org/python-pandas-dataframe-loc/ \
DT Day of Week: https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.dt.dayofweek.html \
Pandas Interate Dataframe: https://pythonbasics.org/pandas-iterate-dataframe/ \
Strip strings inside bracket: https://stackoverflow.com/questions/20894525/how-to-remove-parentheses-and-all-data-within-using-pandas-python \
Adding colour to pie charts: https://www.pythonprogramming.in/how-to-pie-chart-with-different-color-themes-in-matplotlib.html \
Using axvline to add average line: https://stackoverflow.com/questions/45724329/let-axvline-end-at-certain-y-value \
Plot MultiIndex = https://stackoverflow.com/questions/54451127/creating-a-heatmap-from-a-pandas-multiindex-series \
Modify sns heatmaps: https://stackoverflow.com/questions/42712304/seaborn-heatmap-subplots-keep-axis-ratio-consistent \
Marker styles: https://matplotlib.org/3.1.1/api/markers_api.html \
Sum text columns: https://cmdlinetips.com/2018/11/how-to-join-two-text-columns-into-a-single-column-in-pandas/ \
Melting Dataframe: https://pandas.pydata.org/docs/reference/api/pandas.melt.html \
Concat Dataframe: https://www.geeksforgeeks.org/python-pandas-merging-joining-and-concatenating/ \
Change Seaborn plot size: https://stackoverflow.com/questions/31594549/how-do-i-change-the-figure-size-for-a-seaborn-plot \
Rename Seaborn legend: https://stackoverflow.com/questions/53116532/modify-seaborn-line-relplot-legend-title \
Rename Columns: https://chartio.com/resources/tutorials/how-to-rename-columns-in-the-pandas-python-library/ \
Plot 3 variable bar chart: https://stackoverflow.com/questions/42128467/matplotlib-plot-multiple-columns-of-pandas-data-frame-on-the-bar-chart \
Filter between two values: https://stackoverflow.com/questions/31617845/how-to-select-rows-in-a-dataframe-between-two-values-in-python-pandas/40442778 \
Drop rows matching string: https://stackoverflow.com/questions/28679930/how-to-drop-rows-from-pandas-data-frame-that-contains-a-particular-string-in-a-p \
Percentage of value_counts = https://stackoverflow.com/questions/14281871/given-a-pandas-series-that-represents-frequencies-of-a-value-how-can-i-turn-tho


```python

```
