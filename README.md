# Human Rights Watch quantitative analysis of the criminalization of unhoused people in Los Angeles, California

Code by Brian Root; report authored by John Raphling.

### Introduction
This repository includes the analytical code that was used for all data analysis included in the Human Rights Watch report on the criminalization of unhoused people, released in August 2024. This repository includes raw data that was provided by city agencies (e.g. Los Angeles Police Department, Los Angeles Sanitation, and Los Angeles Homeless Services Authority) in response to California Public Records Act requests or on the city’s open records repository.  The folders include additional coding data used in data processing and all analytical code used to produce our findings. The analysis scripts have been annotated to explain what each snippet is producing. All code is in R.

### Doc
The “doc” folder contains all of Human Rights Watch’s original California Public Records Act requests to city and/or city/county agencies.

### Data
The folder "import/input" contains the raw data as provided by city agencies. The following describes the raw data:
#### Los Angeles Police Department
- "import/input/LAPD/structured data/ARRESTS AND RFCS IDENTIFIED AS HOMELESS.xlsx" is raw data provided to HRW by LAPD in response to a public records act request for data on all arrests of unhoused people between 1/1/2016 and 12/31/2022.

- "import/input/LAPD/structured data/Arrest_Data_downloaded5_9_23.csv" and "import/input/LAPD/structured data/Arrest_Data_through2019_downloaded.csv" contain data on all LAPD arrests downloaded from the [city open records portal]( https://data.lacity.org/) 
