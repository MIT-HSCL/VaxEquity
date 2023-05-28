# VaxEquity
## Incorporating Equity into Vaccine Access
### Abstract
COVID-19 vaccine access inequity was a major challenge during the pandemic. This inequity was present between countries and regions and within cities. We developed a novel approach to measure and improve vaccine access equity to address this issue. Our approach first created a vaccination attainment index based on CDC COVID-19 data. We then selected the most relevant spatial, e. g., the density of medical facilities, and socioeconomic factors, to train an XGBoost mod-el on the county level of the United States. Using this model on census tracts within counties, we used the Gini and Theil indices to measure equity. We identified the main drivers of vaccine ac-cess based on SHAP values. With the main drivers identified (percentage of American Indian and Alaska native population, health insurance coverage, and transportation options), we conducted a case study on Cambridge, MA. We improved the short-term access equity by adjusting each cen-sus tract’s density of medical facilities (from Gini 0.14 to 0.13). Our novel approach provides deci-sion-makers with a tool to identify and address drivers of vaccine access equity in their region and predict vaccination attainment on the tract level. These insights are crucial to ensuring equal ac-cess to vaccines and other essential healthcare services for everyone.

---
### Readme
A detailed explanation of the underlying project and methodology can be found in the related Capstone report by Matthias Schumm and Mehdi Tagorti. It can be found on MIT's [DSpace](https://dspace.mit.edu/). At this time (May 28th 2023) the file has not yet been made available. 

####  Models used
- The final model as referenced in the Capstone report can be found in the file "Modeling_XGBoost_Final.ipynb" with a correction available as "Modeling_XGBoost_Final-Copy1.ipynb".

- The linear model discarded can be found in the notebook "Modeling_Linear.ipynb".

### Data Preparation
**NOTE**: The required input files for the final models are included in this repository. Only if you want to **RECREATE** them, you must execute the data preparation steps. Those steps require extensive computing power due to large file sizes.

In order to recreate the files used as input for the final models, both notebooks in "Data_Preparation" must be run.
They in return require the notebook in "SIC_Details" to filter the medical facilities to be considered.

---
### Missing Large Files
There are several files that are too large [+50 MB] for GitHub. We have curated these files in a [Dropbox Folder](https://www.dropbox.com/sh/o7k22a0uzot50l0/AAAH96UEuuAC6BFMve8Me4rpa?dl=0).

The Dropbox folder contains the following files:
- `Counties_Medical_Facilities.zip` - Country level shapefiles for medical facilities
- `Counties_Transportation.zip` - County level shapefiles for transportation information
- `Tracts_Medical_Facilities.zip` - Tract level shapefiles for medical facilities
- `Tracts_Transportation.zip` - Tract level shapefiles for transportation information
- `SIC_Tract_Details.dbf.zip` - DBF file that belongs in the `SIC_Details` directory
- `Data_Preparation_Archive.zip` - three files that belong in the "Data Preparation" directory
    - `COVID-19_Vaccinations_in_the_United_States_County.csv`
    - `ACS_Tracts.csv`
    - `SVI2020_US_Tract.csv`
