# manhole-2026

# Analysis of Open NYC data set — 01/2019 to 10/2026

[LP WILL UPDATE THIS WHEN PUBLISHED] This repository contains data, analytic code, and findings that support portions of the article, “[TKTKTKTK](https://www.google.com),” published Month Date, Year. Please read that article, which contains important context and details, before proceeding.

## Data

This analysis uses FDNY data.

The spreadsheets come from the following sources:

- Name of source:
  - `Fire Incident Dispatch Data - NYC Open Data: (https://data.cityofnewyork.us/Public-Safety/Fire-Incident-Dispatch-Data/8m42-w767/about_data)

Each of the spreadsheets contain, among others, the following columns relevant to the analysis:

- `INCIDENT_DATETIME` — when the the manhole fire was reported
- `STARFIRE_INCIDENT_ID` — a unique identifier of the incident 
- `ZIPCODE` — the location of the incident

## Methodology

The notebook [`manhole-2026.ipynb`](nhttps://github.com/lauraplive/manhole-2026/blob/main/notebook/manhole-2026.ipynb) performs the following analyses:

##### Part 1: Cleaning the data

- I spent some time understanding the dataset by comparing information about the dataset in python code with the dataset in an excel spreadsheet. In python, using a library called pandas, I looked for duplicates in the dataset, and looked for null results – spots where nothing was entered into the spreadsheet. Instead of getting rid of the rows with an empty cell, I decided to check the percentage of null results and found that the percentage was very low and that the zipcode section had the highest number with 1.48% null results. Overall, there were no duplicated rows, no duplicate of a unique identifier for the incident by the FDNY, and a low rate of null cells. I felt confident that the data was rather clean, so I forged ahead. 


##### Part 2: Analysis + graph generation

- I looked at the rates of FDNY-reported manhole fires for the fiscal and calendar years. And I looked at the months since 2019 with the highest number of manhole fires. I found that this past February had the second-highest rate since 2019. My primary finding is that 4884 manholes spewed flames or smoke so far in 2026, the highest number since 2019. In further analysis, I plan to look back further in the data, at least another 10 years. I will be cautious about making sure the measuring system was the same or comparable in all years documented. Next I plotted the fires using Plotly and tested out a few different display formats. I settled on a bar chart, and outputted that into DataWrapper.


## Outputs

The notebooks output this spreadsheet which contains TKTK: [`output/tktktk.csv`](output/tktktk.csv).

## Running the analysis yourself

You can run the analysis yourself. To do so, you'll need the following installed on your computer:

- Python 3
- The Python libraries specified in [`requirements.txt`](requirements.txt)

## Licensing

All code in this repository is available under the [MIT License](https://opensource.org/licenses/MIT). The data file in the output/ directory is available under the [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0) license. All files in the data/ directory are released into the public domain.

## Feedback / Questions?

Contact YOUR NAME HERE at your.name@email.com.