# Storytelling Data Visualization on Exchange Rates

## Overview
In this notebook, I examined the exchange rate between the euro and U.S. Dollar between 1999 and 2021, specifically how the rate changed during the presidencies of George W. Bush, Barak Obama, and Donald Trump. 

## Installation and Setup
This project can be run directly from gituhub or downloaded and run in Jupyter notebook.

### Codes and Resources Used

- Editor Used: Jupyter notebook 6.5.2
- Python Version: Python 3.10.9

### Python Packages Used

- General Purpose:
    - Datetime
- Data Manipulation: 
    - NumPy and Pandas
- Data Visualization: 
    - Matplotlib
    - Seaborn

## Data

### Source Data

 The [dataset](https://www.kaggle.com/lsind18/euro-exchange-daily-rates-19992020) from kaggle.com contains the daily exchange rate between the euro and various other world currencies.  Daria Chemkaeva compiled it from data made available by the European Central Bank. 

### Data Acquisition

The dataset was already downloaded and proviced in .csv format by dataquest as euro-daily-hist_1999_2020.csv.  I imported it using Pandas.read_csv()

### Data Preprocessing

Since I ws looking at only euro's exchange rate with the U.S. Dollar, first I split off the 'Period\\Unit:' and '[US dollar ]' columns into a new dataframe, then renamed them to Time and US_dollar.  I then converted all of the date/time values to datetime datatypes.  For the US_dollar column, I dropped all rows containg '-' and then converted the rest to float datatype. 

## Code structure

    ├─ Storytelling Data Visualization on Exchange Rates.ipynb
    ├─ euro-daily-hist_1999_2020.csv
    ├─ Readme.md
    ├── Visuals
    │   ├── presidencies.jpg
    │   ├── unsmoothed_rate.jpg
    │   ├── unsmoothed_vs_rolling.jpg
    

## Results and evaluation
By graphing the euro/dollar exchange rate and color-coding them by presidential term, I found that the rate increased during Bush and Trump's terms and decreased during Obama's and through research discovered it is common for the exchange rate to rise and fall during Republicans' and Democrats' presidencies, respectively. 

## Future work
I would like to explore how the exchange rates were affected by major world events such as 9/11 and the Covid pandemic.  It would also be interesting to compare multiple other currencies, and look for trends such as which rates tend to rise and fall together, if there are trends in certain geographic areas, or if currencies with similar relative strengths perform similarly. 

## Acknowledgments/References

Guided Project: Dataquest
Dataset: Daria Chemkaeva, Kaggle.com, and The European Central Bank.

## Visuals
[](https://github.com/PatrickTSmith/Data_Analyst_Portfolio/2_3 Storytelling Data Visualization on Exchange Rates/unsmoothed_rate.jpg)
[](https://github.com/PatrickTSmith/Data_Analyst_Portfolio/2_3 Storytelling Data Visualization on Exchange Rates/unsmoothed_vs_rolling.jpg)
[](https://github.com/PatrickTSmith/Data_Analyst_Portfolio/2_3 Storytelling Data Visualization on Exchange Rates/presidencies.jpg)

## License
Source code is licensed under the [GPL 3.0 License](https://www.gnu.org/licenses/gpl-3.0.en.html).

Contents of this site are © Copyright 2023 Patrick T. Smith. All rights reserved.
