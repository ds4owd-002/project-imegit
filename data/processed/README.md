# README

## General information

1.  Title of Dataset:\
    Household drinking water and sanitation service coverage in African and Asian countries (JMP-derived dataset, 1990–2016)

2.  Author Information

    **Author A**

    -   First name: Augustine Azubuike kalu Madumere
    -   Surname: Madumere
    -   ORCID iD:0009-0004-8168-9117
    -   Email:[austin.madumere\@gmail.com](mailto:austin.madumere@gmail.com){.email}

3.  Date of data collection (single date, range, approximate date):\
    Original household survey data were collected between approximately 1990 and 2016 by national statistical offices and survey agencies.\
    This derived dataset was compiled from the WHO/UNICEF Joint Monitoring Programme (JMP) household database and downloaded in June 2019.

4.  Geographic location of data collection:\
    Countries in Africa and Asia included in the JMP global database.

5.  Information about funding sources that supported the collection of the data:\
    The original data compilation and estimation were carried out by the WHO/UNICEF Joint Monitoring Programme for Water Supply, Sanitation and Hygiene (JMP).\
    (Add your own course/project funding information if relevant.)

## Sharing / access information

1.  Licenses/restrictions placed on the data:\
    This dataset is derived from WHO/UNICEF JMP household data on drinking water and sanitation coverage. Users should cite JMP appropriately and comply with JMP terms of use. The structure and processing code for this derived dataset may be shared under a Creative Commons Attribution 4.0 International (CC BY 4.0) licence.

2.  Links to publications that cite or use the data:

    -   (Add links to your own report/thesis once available.)

3.  Links to other publicly accessible locations of the data:

    -   WHO/UNICEF JMP household data portal: <https://washdata.org/data/household>

4.  Links/relationships to ancillary data sets:

    -   Other JMP indicator files can be linked by country code and year.

5.  Was data derived from another source?\
    Yes. This dataset was derived from country-level files in the WHO/UNICEF Joint Monitoring Programme (JMP) global database.

## Methodological information

1.  Description of methods used for collection/generation of data:\
    The original data are based on nationally representative household surveys and censuses compiled by the WHO/UNICEF JMP. This derived dataset aggregates all country files downloaded in June 2019 into a single dataset restricted to selected variables and to African and Asian countries.

2.  Methods for processing the data:

    -   Dropped index columns from the raw CSV.\
    -   Split the original `Country` variable into `iso3` and `country_name`.\
    -   Used ISO3 codes to assign each country to a continent and kept only Africa and Asia.\
    -   Reshaped indicators `x1`, `x2`, `x3` into a long format and recoded them into service level categories (`improved`, `piped`, `sewer`, `no_facility`, `open_defecation`).\
    -   Set percentage values outside the 0–100% range to missing.\
    -   Saved the processed dataset to `jmp_processed.csv`.

3.  Instrument- or software-specific information needed to interpret the data:

    -   The dataset is stored as `jmp_processed.csv` and can be opened in standard statistical software.\
    -   Data processing and analysis were performed in R using the tidyverse packages.

4.  Standards and calibration information, if appropriate:

    -   Not applicable.

5.  Environmental/experimental conditions:

    -   Not applicable.

6.  Describe any quality-assurance procedures performed on the data:

    -   Basic checks on value ranges and consistency of service categories.\
    -   Documentation of variables in `data_dictionary.csv`.

7.  People involved with sample collection, processing, analysis and/or submission:

    -   Original household data collection: national statistical offices and survey agencies, coordinated by the WHO/UNICEF JMP.\
    -   Processing and analysis of this derived dataset: (Augustine Madumere, ETH Zurich/Global health Engineering).
