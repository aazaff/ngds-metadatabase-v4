# ngds-metadatabase-v4 Node application

NGDS Node API and User Interface
March 28, 2019

Node express client


API 

GET

/action/record_search?qry=searchfield - Return set of records that meet search criteria

/action/record_show?id=guid - Return latest version of requested record_search

/harvest?sourceid=NN&offset=NN&max=NN  - calls csw-client and iterates db call makemdrecord to build

/preview?sourceid=NN&offset=NN&max=NN - retrieves remote records for viewing but doesnt load in database


User Interface Functions

Data functions 

- Search engine - search records
- View Record Details
	view record history - provenance - TBD
- Contribute build a metadata record - TBD
- Edit - TBD
	
Harvest 
- preview harvest record from source
	- add view of current internal history, diff, and single harvest button - TBD
	- single record harvest button - TBD
- harvest records from specified source
- view harvest history


-Nodejs 8.11.3 >=
    express
	pg
	csw-client
	

	
	

