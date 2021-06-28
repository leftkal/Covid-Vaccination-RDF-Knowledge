# Covid-Vaccination-RDF-Knowledge

WORK IN PROGRESS

A program that gathers information about Covid Vaccination Progress in different countries and merges it with other datasets to create an RDF Graph



In order to run the code you need to set up Google Cloud authentication (needed for bigquery) and get a JSON file containing your key.
Getting started with authentication: https://cloud.google.com/docs/authentication/getting-started

After you have the json file you use:

`
os.environ["GOOGLE_APPLICATION_CREDENTIALS"]="/path/to/file.json"
`

in preproccess.ipynb in cell no 19 to integrate it into your code.
