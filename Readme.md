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

---

Author: Edward Luis Huayllasco Carlos