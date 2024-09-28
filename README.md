# Data Provenance
### CWTS Leiden Open Ranking
The analyses in this project are all based on data provided by the CWTS Leiden Open Ranking. This data in return is based on data provided by OpenAlex - a catalogue of scientific works, authors and institutions. The full data can be downloaded under the following DOI-URL: https://doi.org/10.5281/zenodo.10579113

### Country Code Data
To create some of the maps, I needed a three letter country code that was not provided in the CWTS Leiden Open Ranking. Therefore, I used [the wikipedia iso country codes dataset](https://www.kaggle.com/datasets/juanumusic/countries-iso-codes) provided on Kaggle to add this information to the table.

### Times Higher Education (THE) University Ranking
The latest timeperiod included in the most recent CWTS Leiden Open Ranking is 2018-2021. Accordingly, I used the [THE ranking from the year 2021](https://www.kaggle.com/datasets/matheusgratz/world-university-rankings-2021) which is also available on Kaggle.

### University Microdata
I only found a full dataset of university microdata for European universities. This data can be downloaded from the [project Website of the European Tertiary Education Register (ETER)](https://eter-project.com/data/data-for-download-and-visualisations/database/) using a free account. It is possible to customize the dataset by selecting variables of interest and downloading them.

### ROR ID
Unfortunately, I found no way to easily join the THE data with the other data, as it did not include ROR IDs (a unique persistent identifier for research institutions). The university names that the THE uses also do not conform any of the university names from the other datasets. Hence I prompted chatGPT-4o to write me a small python script that downloads this information from the ROR API. The script is also included in this repository (ROR_API.ipynb). Unfortunately, many of the THE university names were interpreted incorrectly by the ROR API which led to the loss of quite a few datapoints for the correlation analysis.