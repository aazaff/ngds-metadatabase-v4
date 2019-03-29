# ngds-metadatabase-v4

NGDS database design for sustainable metadata lifecycle. Design objectives -
- Upgrade to current system platforms
- Meet current security standards
- Reduce reliance on distributed data that is slowly degrading
- Reduce number of servers for reduced costs
- Aggregate resource data for improve usage
- Metadata schema(s) define in database for consistent workflow and state transitions
- Database defined - automation language, collections, and version control with provenance tracking
- Transactional methods allow large scale automation of metadata processing
- Better support for future NGDS projects

Requirements
- Postgres 11.1
	gdal
	ltree
-Nodejs 8.11.3 >=
    express
	pg
	csw-client
	
Status
3/28/2019
- Basic Harvest functions working in database and application
- Basic search functions 
- CSW-client for harvest


	
	

