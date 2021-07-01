# Covid-Vaccination-RDF-Knowledge

WORK IN PROGRESS

A program that gathers information about Covid Vaccination Progress in different countries and merges it with other datasets to create an RDF Graph

# Datasets

The datasets used in this project are the following:

* https://www.kaggle.com/gpreda/covid-world-vaccination-progress
* https://www.kaggle.com/tanuprabhu/population-by-country-2020
* https://www.kaggle.com/dimanjung/religions-vs-gdp-per-capita
* https://www.kaggle.com/danevans/world-bank-wdi-212-health-systems
* https://www.kaggle.com/theworldbank/world-bank-intl-education

Their structure, data sources and latest versions can be found in their kaggle webpage. The expected input can be found in the `data` folder. However, it is not recommended to use those files as inputs, as they will most certainly be outdated. As far as the covid world vaccination progress is concerned, the nothebooks account for the vaccinations up until May 2021. Extension to further months is possible, just by following the template in `COVID_19_World_Vaccination_Dataset_analysis.ipynb` in cells 15 and 18.

# Notebooks

There are 3 notebooks in this project:

* `COVID_19_World_Vaccination_Dataset_analysis.ipynb`
* `rdf_creation.ipynb`
* `queries_sparql.ipynb`


`COVID_19_World_Vaccination_Dataset_analysis.ipynb` is responsible for reading, formatting and cleaning the data. It reades the resources from the `data` folder and saves the `complete_df.csv` with the final complete dataframe in the `outputs` folder.

In order to run this notebook you need to set up Google Cloud authentication (needed for bigquery) and get a JSON file containing your key.

Getting started with authentication: https://cloud.google.com/docs/authentication/getting-started

When you have the json file, you can use:

`
os.environ["GOOGLE_APPLICATION_CREDENTIALS"]="/path/to/file.json"
`

in `COVID_19_World_Vaccination_Dataset_analysis.ipynb` in cell no 19 to integrate it into your code.



`rdf_creation.ipynb` is the notebook responsible for the transition from pandas dataframe to an rdf database. Furthermore it performs some sparql querries to verify the integrity of the proccess and creates an ugly visualization of a portion of the rdf graph (saved in `outputs` folder)



`queries_sparql.ipynb` is where the sparql queries showcasing the database are located.