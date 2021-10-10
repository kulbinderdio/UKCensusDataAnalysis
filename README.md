# UKCensusDataAnalysis

This project is aiming to show a way of loading the UK Census 2010 data into a Postgres database and analyse that data using Jupyter Notebook.
For this we will be using Python, Postgres, PostGIS, QGIS(possibly), GeoPandas and other tools.

For a detailed description of the Census data have a look at https://www.ons.gov.uk/census/2011census
During the course of this projet I will endeavour to explain terms that are specific to this data and area of analysis such as OAs, LSOAs, MSOAs, etc

Assumption : You have Python 3.8 or higher already installed

##Setup
1. Install Postgresql.  See https://www.postgresql.org/download/
2. Install PostGIS extension. See https://postgis.net/install/
3. Install pgAdmin4. See https://www.pgadmin.org/download/ (or other database client software)
4. Create a database called data. See https://www.postgresql.org/files/documentation/pdf/14/postgresql-14-A4.pdf
5. Install Jupyter Notebook.  See https://jupyter.org/install
6. Download file CensusMetaData.csv
7. Download and open file CensusAnalysisSetup.ipynb in Jupyter Notebook. Run this file
8. Download and open file RetrieveAndSaveCensusData.ipynb in Jupyter Notebook. Run this file (this will take some time)
9. Your database should now be populated with millions of rows of UK 2011 census data
10. Before we start to perform some analysis on this data we will create a few indexes to speed up our queries.
The easiest way to do this is via the database client software (pdAdmin4)
Connect to the database and bring up a query session and run the following code
