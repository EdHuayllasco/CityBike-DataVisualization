# CitiBike Rebalancing Visualization

## Introduction

Citi Bike is a bike-sharing system operating in New York City. It is a bike rental program designed to provide a convenient and accessible form of public transportation in the city. Launched in May 2013, it has become one of the largest and most successful bike-sharing systems in the United States.

The Citi Bike program is a partnership between financial services company Citigroup and the Metropolitan Transportation Authority (MTA) of New York. The system consists of a fleet of distinctive blue bicycles and docking stations distributed throughout the city. New Yorkers and visitors can use Citi Bike by registering for the program and obtaining a membership, whether for a day, a week, or a year. Once registered, they can unlock a bike at any station using a membership card or the Citi Bike mobile app. After using the bike, it must be returned to a docking station within the allotted time to avoid additional charges.

Citi Bike has become a popular choice for getting around New York City. The bikes are designed to accommodate different types of riders, and an optional helmet is provided. The system is particularly useful for short trips and travel within congested urban neighborhoods, offering an eco-friendly and healthy alternative to motorized transportation.

In addition to its primary transportation function, Citi Bike has fostered a sense of community and contributed to an active and healthy lifestyle in the city. Users can enjoy scenic rides through parks and streets, as well as reap the health and environmental benefits that cycling provides.

## Problem

Since its introduction, Citi Bike has faced criticism from customers regarding its poor method of redistributing bikes to equalize the supply between stations. The heavy usage of the bike-share system during commuting hours results in stations quickly running out of bikes in residential areas in the morning and in commercial areas in the afternoon. Numerous recent Citi Bike-related tweets and articles reflect this dissatisfaction. Additionally, negative reviews of the service on TripAdvisor from disappointed tourists further emphasize this issue.

## Data

The anonymous trip system data can be found at: [Citi Bike System Data](https://www.citibikenyc.com/system-data).

- CsvtoJson: Converts monthly CSV files to JSON format (nodes).
- Append Year: Combines all JSON files by year to form the respective nodes.
- Translate To Hour: Generates real-time JSON nodes for departures/arrivals.

## Visualization

- JS
  - D3-tip: Tooltips for SVG-based visualizations using d3.js.
  - Maps: Creates an interactive map with custom markers and a legend based on station data. Marker colors and tooltip information vary based on station data values.

- CSS
  - Applies specific styles.

- HTML
  - Index: Creates the structure for visualizing the dataset.

## Installation

1. Install `venv`.
2. Install requirements (stored in `requirements.txt`).
3. Activate the virtual environment: . .venv/bin/activate
4. Run `python app.py` to execute the program.

## Results

To visualize the dataset, execute the program using the app. Here are some initial results:
### Index View
We have a heatmap where we can differentiate all the nodes that represent the stations, we can consult by year, month inputs, outputs or input/output conglomerate.Each time you select a different year or month the graphs are updated the legend is dependent on time based demand
<p align="center">
  <kbd>
    <img src="/static/images/8.jpg" alt="Stations Map" width="300"/>
  </kbd>
</p>
You can click on each color of the legend which will allow you to show only the stations of each cluster.
<p align="center">
  <kbd>
    <img src="/static/images/17.png" alt="Stations color" width="300"/>
  </kbd>
</p>
<p align="center">
  <kbd>
    <img src="/static/images/18.png" alt="Stations color" width="300"/>
  </kbd>
</p>
---
Once you click on a station, the station will be marked in green to be able to visualize it and it will show you two graphs, each graph shows the demand based on inputs and outputs based on 24 hours a day through that station. period of time is a specific month or a year, and also based on the days the same is in a specific month or year.
<p align="center">
  <kbd>
    <img src="/static/images/9.jpg" alt="Marked Station" width="300"/>
  </kbd>
</p>
<p align="center">
  <kbd>
    <img src="/static/images/16.png" alt="Station Hours/Days graph bar" width="300"/>
  </kbd>
</p>
The second section we can request, based on each station shown above, a time series graph based on facebook-prophet which shows a summary of the 2015-2018 behavior based on the demand of each station day by day.
<p align="center">
  <kbd>
    <img src="/static/images/6.jpg" alt="Time Series" width="300"/>
  </kbd>
</p>
<p align="center">
  <kbd>
    <img src="/static/images/14.jpg" alt="Time Series E20 St." width="300"/>
  </kbd>
</p>
The third part started with 3 sections, but it has been modified. On the left we have a sankey diagram whose function is to see the volume of the trajectories from station to station and the right graph shows the different clustering that is formed over time in seasons.
<p align="center">
  <kbd>
    <img src="/static/images/5.jpg" alt="Third section" width="300"/>
  </kbd>
</p>
<p align="center">
  <kbd>
    <img src="/static/images/4.jpg" alt="Third section" width="300"/>
  </kbd>
</p>
A Sankey chart (also known as a Sankey diagram or Sankey flowchart) is a type of visualization that represents the direction and flow of resources, quantities, or values between different items or categories. This type of graph is especially useful for showing the distribution of resources, energy, costs, or any other type of flow that can be quantified. For our data set, we can specify a group of stations to graph. In addition, we can specify the time based on months/days and hours in order to better understand the visualization, this in order to make the graphic visualization readable. all dynamically.
<p align="center">
  <kbd>
    <img src="/static/images/5.jpg" alt="72Th Station Sankey Graph by hour" width="300"/>
  </kbd>
</p>
<p align="center">
  <kbd>
    <img src="/static/images/13.jpg" alt="Group Stations Sankey Graph by day" width="300"/>
  </kbd>
</p>
Finally, the clustering issue uses 3 parameters, the demand (inputs/outputs), the geographical location and also the time lapses (the data ratio year/month/day/hour/minute/seconds) in our case we are reducing the dimensions with PCA to use only up to days. as a result the clusters change based on demand, time and location. You can select by months and days to know how the clusters are grouped in different ways depending on the days and the demands.
<p align="center">
  <kbd>
    <img src="/static/images/12.jpg" alt="Third View" width="300"/>
  </kbd>
</p>
<p align="center">
  <kbd>
    <img src="/static/images/3.jpg" alt="Group Clusters" width="300"/>
  </kbd>
</p>
Also, by clicking on the color of the legend, that certain group of clusters can appear or disappear, in addition to the fact that once the mouse is placed over the station, its information will appear, as in the first map.
<p align="center">
  <kbd>
    <img src="/static/images/10.jpg" alt="Group Clusters Color Pink" width="300"/>
  </kbd>
</p>
Author: Edward Luis Huayllasco Carlos