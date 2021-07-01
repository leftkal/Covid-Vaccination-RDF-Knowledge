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

Their structure, data sources and latest versions can be found in their kaggle webpage. The expected input can be found in the `data` folder. However, it is not recommended to use those files as inputs, as they will most certainly be outdated. As far as the covid world vaccination progress is concerned, the nothebooks account for the vaccinations up until May 2021. Extension to further months is possible, just by following the template in `COVID_19_World_Vaccination_Dataset_analysis.ipynb`.

In order to run the code you need to set up Google Cloud authentication (needed for bigquery) and get a JSON file containing your key.
Getting started with authentication: https://cloud.google.com/docs/authentication/getting-started

After you have the json file you use:

`
os.environ["GOOGLE_APPLICATION_CREDENTIALS"]="/path/to/file.json"
`

in preproccess.ipynb in cell no 19 to integrate it into your code.
