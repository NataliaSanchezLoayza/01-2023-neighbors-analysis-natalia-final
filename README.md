# Analysis of Brookhaven Police Department Neighbors App Data Set — 01/2021 to 05/2022

This repository contains data, analytic code, and findings that support portions of the article, “[TKTKTKTK](https://www.google.com),” published Month Date, Year. Please read that article, which contains important context and details, before proceeding.

## Data

This analysis uses 1 spreadsheet.

The spreadsheets come from the following sources:

- Name of source:
  - `msg_extracts.csv`: Raw data of all of the emails alerts that Brookhaven Police Department received from the Neighbors App from January 2021 to May 2022

The spreadsheet contains, among others, the following columns relevant to the analysis:

- `to` — email addresses of the Brookhaven police officers that received the alarms
- `date` — date alerts were received
- `body_title` — short description of the content of the alert

## Methodology

The notebook [`analysis 1-natalia.ipynb`](notebooks/analysis 1-natalia.ipynb) performs the following analyses:

##### Part 1: Unique number of recipients

- Select the column `to` and use the value_counts() function to get a list of the the unique emails addresses and the number of times those addresses received the alerts
 - Create a new dataFrame called 'unique_count' to contain the previous list and export the new dataFrame as a csv file


##### Part 2: Tallies over time

- Description of what you did with the data

##### Part 2: Tallies of the body_text column values containing “package” and “car”

- Description of what you did with the data


## Outputs

The notebooks output this spreadsheet which contains TKTK: [`output/tktktk.csv`](output/tktktk.csv).

## Running the analysis yourself

You can run the analysis yourself. To do so, you'll need the following installed on your computer:

- Python 3
- The Python libraries specified in [`requirements.txt`](requirements.txt). You can install them by running `pip install -r requirements.txt`

## Licensing

All code in this repository is available under the [MIT License](https://opensource.org/licenses/MIT). The data file in the output/ directory is available under the [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0) license. All files in the data/ directory are released into the public domain.

## Feedback / Questions?

Contact YOUR NAME HERE at your.name@email.com.
