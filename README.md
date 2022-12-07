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
- Load libraries and data
- Select the column `to` and use the value_counts() function to get a list of the the unique emails addresses and the number of times those addresses received the alerts
 - Create a new dataFrame called 'unique_count' to contain the previous list and export the new dataFrame as a csv file


##### Part 2: Tallies over time

- Load libraries and data, parsing the date column
- Select the "date" column and convert it to utc (coordinated universal time)
- Create a new dataFrame with this information and reset the index to be the 'date'
- Resample the date by month
- Create a new dataFrame called 'brookhaven_resampling' to contain the data and export the new dataFrame as a csv file


##### Part 3: Tallies of the body_text column values containing “package” and “car”

- Load libraries and data
- Create a new column 'package_car' and use the lambda function to select any messages that contain 'package' or 'car' in the 'body_title" column. All messages containing either of these words will appear in the new column 'package_car' as a True or False statement.
- Use the value_counts() function on this new column
Create a new dataFrame called 'brookhaven_car_package' to contain the data and export the new dataFrame as a csv file

## Outputs

The notebooks output this spreadsheet which contains 3 csv files:

[`output/car_package-Sanchez.csv`](output/car_package-Sanchez.csv)
[`output/unique_count-Sanchez.csv`](output/unique_count-Sanchez.csv)
[`output/resampling-Sanchez.csv`](output/resampling-Sanchez.csv)

## Running the analysis yourself

You can run the analysis yourself. To do so, you'll need the following installed on your computer:

- Python 3
- The Python libraries specified in [`requirements.txt`](requirements.txt). You can install them by running `pip install -r requirements.txt`

## Licensing

All code in this repository is available under the [MIT License](https://opensource.org/licenses/MIT). The data file in the output/ directory is available under the [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0) license. All files in the data/ directory are released into the public domain.

## Feedback / Questions?

Contact Natalia Sanchez Loayza at natalia.sanchezloayza37@journalism.cuny.edu.
