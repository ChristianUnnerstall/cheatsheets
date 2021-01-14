### General
````
bin/elasticsearch                                                # start elasticsearch instance
curl -X GET 'http://localhost:9200/?pretty=true'                 # view instance metadata
curl -X POST 'http://localhost:9200/_shutdown'                   # shutdown elasticsearch instance
curl -X GET 'http://localhost:9200/_cat?pretty=true'             # list all admin methods
curl -X GET 'http://localhost:9200/_cat/indices?pretty=true'     # list all indices
curl -X GET 'http://localhost:9200/_cluster/health?pretty=true'  # view cluster health
````
### Indexing
````
curl -X GET 'http://localhost:9200/<index name>'                 # view specific index
curl -X POST 'http://localhost:9200/<index name>'                # create an index
curl -X DELETE 'http://localhost:9200/<index name>'              # delete an index
curl -X GET 'http://localhost:9200/<index name>/_search'         # search an index
curl -X GET 'http://localhost:9200/<index name>/<type>/_search'  # search an index type
````
### Working with documents
````
#### Retrieving and modifying documents.
curl -X GET 'http://locahost:9200/<index name>/<type>/<id>'      # retrieve a specific document
curl -X POST 'http://locahost:9200/<index name>/<type>/'         # create a document
curl -X PUT 'http://locahost:9200/<index name>/<type>/<id>'      # create/update a specific document
curl -X DELETE 'http://localhost:9200/<index name>/<type>/<id>'  # delete a specific document
### Mappings and Settings
````
### Mappings
````
curl -X GET 'http://localhost:9200/<index name>/_mappings'         # view mappings for index
curl -X GET 'http://localhost:9200/<index name>/<type>/_mappings'  # view mappings for an index type
````
### Settings
````
curl -X GET 'http://localhost:9200/<index name>/_settings'         # view setting information for an index
curl -X GET 'http://localhost:9200/<index name>/<type>/_settings'  # view setting information for an index type
````
