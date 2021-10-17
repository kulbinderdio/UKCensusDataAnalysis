# UKCensusDataAnalysis

This project is aiming to show a way of loading the UK Census 2010 data into a Postgres database and analyse that data using Jupyter Notebook.
For this we will be using Python, Postgres, PostGIS, QGIS(possibly), GeoPandas and other tools.

After initial setup described below, the Retrieve..... script is used to download the Key Statistics data for several of the questions in the 2011 UK Census. This data is. then loaded into a single table as key/value pair data allowing a very simple database structure to be used. The XXX. script will then give examples of using this data to extract key facts as well as drawing maps showing this data in pictorial format. 
The data being used is released at Output Area (OA) level are relatively small geographical areas, England and Wales have over 181,000 such OAs.
As well as showing Pythin techniques for the creation of database tables and data retrieval this will show how libraries like GeoPandas can be used to retrieve this data and create maps. Once the. data has been loaded into the database other tools such as QGIS could equally be used to retrieve and display this data.

For a detailed description of the Census data have a look at https://www.ons.gov.uk/census/2011census
The specific census data we are retrieving is Key Statistics data and can be found at https://www.nomisweb.co.uk/census/2011/key_statistics

Assumption : You have Python 3.8 or higher already installed

##Setup
1. Install Postgresql.  See https://www.postgresql.org/download/
2. Install PostGIS extension. See https://postgis.net/install/
3. Install pgAdmin4 (optional). See https://www.pgadmin.org/download/ (or other database client software)
4. Create a database called data. Dont' forget to call CREATE EXTENSION POSTGIS; (see PostGIS documentation) See https://www.postgresql.org/files/documentation/pdf/14/postgresql-14-A4.pdf
5. Install Jupyter Notebook.  See https://jupyter.org/install
6. Download file CensusMetaData.csv
7. Download and open file CensusAnalysisSetup.ipynb in Jupyter Notebook. Run this file
8. Download and open file RetrieveAndSaveCensusData.ipynb in Jupyter Notebook. Run this file (this will take some time)
9. Your database should now be populated with millions of rows of UK 2011 census data

