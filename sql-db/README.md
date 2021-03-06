# ngds-metadatabase-v4 Database Notes
March 28, 2019

Metadata

	TABLES 
	
	md_record - top level entity - unique identifer for a record
	md_version - version tracker for each record
	mdvnode - recursive deconstructed data for each record/version
	
	API

	HARVEST Functions
	
	makeMdRecord - top level metadata record insert
	makeMdVersion - create a new metadata version 
	makeNodeJ - uses jtor and insert data into mdvnode
	mdn_jtor - parses json object into rows

	VIEWS  Functions
	
	mdn_jsonout(version_id) - provides a json object based on the id
	mdn_bag - internal used by jsonout
	
	mdn_get_object() - get each instance (top level) of an object in a record 
	mdn_find_object() - return the full object given its node id
	

	VIEWS 
	
	mdview - errors - replaced with mdn_bag, but a view would be useful problem with the treepath - invalid characters
	
Schemas - define the structure of metadata.  Schema definitions are designed so that metadata records can be mapped new schema structures without
          changing the originating data. 
		  
	Schemas - Master table
	schema_node - is the deconstructed schema 
	schema_map - translates a schema into a federated schema or other schema
	
Activity & Process - defines the automation controls and log of changes that occur.

	Activity_definition - Master level definition, made up of zero-many processes
	Process Definition - process definition can be external jobs, or zero to many process_rulesets
	Process_ruleset - A PR is a set of rules that that can be applied to a metadata record or records
	rule_definitions - defines each rule.  A rule can be different types and acts on a node endpoint or object.  Conditional logic is defined
	
		
Collections 

	Collections - user defined groups of metadata records.  A standard collection is the set of harvest sources
	collections_process - relates the collection to a processing job 
	collection_process_records - is the transaction log of processed records for a job. Identifies specific version changes
	

