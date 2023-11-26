# nosql-challenge

# Part 1: Database and Jupyter Notebook Set Up

Used NoSQL_setup_starter.ipynb for this section of the challenge.

Imported the data provided in the establishments.json file. Name the database uk_food and the collection establishments.
Copied the text used to import the data from the Terminal to a markdown cell in your notebook.

Within jupyter notebook, imported the libraries needed: PyMongo and Pretty Print (pprint).

Created an instance of the Mongo Client.

Confirmed that the database was created and loaded the data properly:

List the databased currently in MongoDB. Confirm that uk_food is listed.
List the collection(s) in the database to ensure that establishments is there.
Find and display one document in the establishments collection using find_one and display with pprint.

Assign the establishments collection to a variable to prepare the collection for use.

# Part 2: Update the Database

Used NoSQL_setup_starter.ipynb for this section of the challenge.

Make the following changes to the establishments collection:

Added the following information to the database:
{
    "BusinessName":"Penang Flavours",
    "BusinessType":"Restaurant/Cafe/Canteen",
    "BusinessTypeID":"",
    "AddressLine1":"Penang Flavours",
    "AddressLine2":"146A Plumstead Rd",
    "AddressLine3":"London",
    "AddressLine4":"",
    "PostCode":"SE18 7DY",
    "Phone":"",
    "LocalAuthorityCode":"511",
    "LocalAuthorityName":"Greenwich",
    "LocalAuthorityWebSite":"http://www.royalgreenwich.gov.uk",
    "LocalAuthorityEmailAddress":"health@royalgreenwich.gov.uk",
    "scores":{
        "Hygiene":"",
        "Structural":"",
        "ConfidenceInManagement":""
    },
    "SchemeType":"FHRS",
    "geocode":{
        "longitude":"0.08384000",
        "latitude":"51.49014200"
    },
    "RightToReply":"",
    "Distance":4623.9723280747176,
    "NewRatingPending":True
}

Found the BusinessTypeID for "Restaurant/Cafe/Canteen" and returned only the BusinessTypeID
and BusinessType fields.

Updated the new restaurant with the BusinessTypeID found.

Removed any establishments within the Dover Local Authority from the database, and check the 
number of documents to ensure they were deleted.

Used update_many to convert latitude and longitude to decimal numbers.
Used update_many to convert RatingValue to integer numbers.

# Part 3: Exploratory Analysis

Used NoSQL_analysis_starter.ipynb for this section of the challenge

Used the following questions to explore the database, and find the answers
Use count_documents to display the number of documents contained in the result.

Displayed the first document in the results using pprint.

Converted the result to a Pandas DataFrame, print the number of rows in the DataFrame,
and displayed the first 10 rows.

Questions to answer:
  Which establishments have a hygiene score equal to 20?

  Which establishments in London have a RatingValue greater than or equal to 4?

  What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, 
  nearest to the new restaurant added, "Penang Flavours"?

  How many establishments in each Local Authority area have a hygiene score of 0?

  
