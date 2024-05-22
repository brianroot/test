# Human Rights Watch quantitative analysis of the criminalization of unhoused people in Los Angeles, California

Code by Brian Root; report authored by John Raphling.

### Introduction
This repository includes the analytical code that was used for all data analysis included in the Human Rights Watch report on the criminalization of unhoused people, released in August 2024. This repository includes raw data that was provided by city agencies (e.g. Los Angeles Police Department, Los Angeles Sanitation, and Los Angeles Homeless Services Authority) in response to California Public Records Act (PRA) requests or on the city’s open records repository.  The folders include additional coding data used in data processing and all analytical code used to produce our findings. The analysis scripts have been annotated to explain what each snippet is producing. All code is in R.

### Doc
The “doc” folder contains all of Human Rights Watch’s original California Public Records Act requests to city and/or city/county agencies.

### Data
The folder "import/input" contains the raw data as provided by city agencies. The following describes the raw data:
#### Los Angeles Police Department
- "import/input/LAPD/structured data/ARRESTS AND RFCS IDENTIFIED AS HOMELESS.xlsx" is raw data provided to HRW by LAPD in response to a public records act request for data on all arrests of unhoused people between 1/1/2016 and 12/31/2022.

- "import/input/LAPD/structured data/Arrest_Data_downloaded5_9_23.csv" and "import/input/LAPD/structured data/Arrest_Data_through2019_downloaded.csv" contain data on all LAPD arrests downloaded from the city open records [portal]( https://data.lacity.org/).

- "import/input/LAPD/structured data/CRIMES WITH HOMELESS AS VICTIM_R.xlsx" is raw data provide in response to the PRA request regarding known offenses with an unhoused victim.

-   "import/input/LAPD/structured data/Crime_Data_from_2020_to_Present.csv" and "import/input/LAPD/structured data/Crime_Data_from_2010_to_2019_20231107.csv" are LAPD datasets on reported crime downloaded from the city open records [portal]( https://data.lacity.org/).

-   "import/input/LAPD/structured data/USE OF FORCE_R.xlsx" was provided in response to our PRA request for all data on use of force and whether the subject was unhoused.

-   "import/input/LAPD/structured data/41.18_Arrests_2021_-_2023 - Raw File.csv" contains data on 41.18 arrests downloaded from the LA Controller’s [site]( https://controller.lacity.gov/landings/4118).

#### Los Angeles Homeless Services Agency (LAHSA)

- "import/input/LAHSA/Request 1 - Services and locations starting 2019-01-01.xlsx" contains data on services provided to unhoused people by LAHSA staff and was provided to HRW by LAHSA in response to our PRA request.

- "import/input/LAHSA/PRK Clients Served - Entire Program History.xlsx" is also in response to our PRA request and provides data on clients of LAHSA’s Project Roomkey program.

- "import/input/LAHSA/29192 - HRW PRA on ISP.xlsx" is also in response to our PRA request and provides data on clients of LAHSA’s Inside Safe program.

#### Los Angeles Sanitation (LASAN)

- "import/input/LASAN/WPIMS Data - 201910010_20230217_ver2.xls" includes data provided by LASAN to HRW in response to our PRA request for all information about cleanings related to the unhoused population including CARE, CARE+, Operation Healthy Streets, Special Enforcement Cleaning Zones and other LAMC 41.18 enforcement.

#### “Frozen” subfolders
Any sub-folders titled “../frozen” contain additional data, typically created by Human Rights Watch, used for processing or coding the original data. For example, “processing/frozen/offenses_recoded.csv” contains Human Rights Watch’s coding of the raw offense data provided by LAPD. 

###Processing

This folder contains the scripts in the “processing/src” folder and additional datafiles needed to process the data in the “processing/frozen” folder. There are separate processing scripts for data from each agency. Each processing script is annotated to describe what each code snippet is doing. Within the processing scripts, locations are joined with additional geographic data which was processed outside of the R code using various geocoding apis and functions in GIS software. Geocoded addresses and locations are brought into the processing scripts via the “frozen” folder.
“processing_other” contains processing code for processing the LAHSA point-in-time unhoused count as well as census data for the overall city population.
“tidy_census_processing” contains a script for downloading and cleaning data downloaded from the US Census Bureau and CPI inflation data.


### Analysis

