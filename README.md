# Movies-ETL

## Overview
In order to create an automated pipeline that takes in new data and perform the appropriate transformations, we are creating a function that will do this for us. The function will extract movie data from wikipedia JSON data, as well as Kaggle data in CSV format. This function will transform the data, eliminate rows that we do not need, as well as transform certain rows into a uniform structure.  Once our data has been cleaned sufficiently, our function will load the data into our Postgres SQL database.


# Procedure

To make the function easier to understand, we created 4 files to break the process down into steps.   

1.We first created a basic function to encapsule the majority of our "extraction process.
2.We then added a portion of code into our function that worked specifically on cleaning the Wikipedia data found inside of the JSON file.  We then converted into a pandas DataFrame.
3.We then cleaned up the data in our Kaggle Data and our ratings data and then simply merged it with our wikipedia file based on common imdb numbers and then merged the ratings data to go with it.
4.The last portion of our function involved us linking with our Postgres SQL server and loading our data into PostGres SQL.

# Takeaway

The ETL Process will require different methods depending on the datasets you are interacting with, but it will ultimately always require you first inspecting the data, creating a plan to clean the data, and then executing said plan to a non destructable copy of the data.  This creates a process where we can safely clean and parse through the data so that we can proceed with only relevant data as well as data in a format that is compatible for us to properly conduct our analysis.

