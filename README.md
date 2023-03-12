# Analyzing_resturants_No_SQL

## Part 1: Database and Jupyter Notebook Set Up

Imported data and libraries: PyMongo and Pretty Print.

Created an instance of the Mongo Client.

Confirmed I created database and loaded the data properly:

Listed the databases you have in MongoDB. Confirmed that uk_food is listed.
Listed the collection(s) in the database to ensure that establishments were there.
Found and displayed one document in the establishments collection using find_one and display with pprint.
Assigned the establishments collection to a variable to prepare the collection for use.

## Part 2: Updated the Database

Modified the database.

Made the following changes to the establishments collection:

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

Found the BusinessTypeID for "Restaurant/Cafe/Canteen" and returned only the BusinessTypeID and BusinessType fields.

Updated the new restaurant with the BusinessTypeID.

Removed any establishments within the Dover Local Authority from the database, and checked the number of documents to ensure they were deleted.

Used update_many to convert latitude and longitude to decimal numbers.

## Part 3: Exploratory Analysis

Used count_documents to display the number of documents contained in the result.

Displayed the first document in the results using pprint.

Converted the result to a Pandas DataFrame, printed the number of rows in the DataFrame, and displayed the first 10 rows.

