#### Connect
````
var elasticsearch=require('elasticsearch');
var client = new elasticsearch.Client( {  
  hosts: [
    'https://[username]:[password]@[server]:[port]/',
    'https://[username]:[password]@[server]:[port]/'
  ]
});
module.exports = client;
````
#### Status
````
var client = require('./connection.js');
client.cluster.health({},function(err,resp,status) {  
  console.log("Client Health ",resp);
});
````
#### Create Indices
````
var client = require('./connection.js');
client.indices.create({  
  index: 'books'
},function(err, resp, status) {
  if(err) {
    console.log(err);
  }
  else {
    console.log("create", resp);
  }
});
````
#### Delete Indices
````
var client = require('./connection.js');
client.indices.delete({index: 'books'}, function(err,resp,status) {  
  console.log("delete", resp);
});
````
#### Index document
````
var client = require('./connection.js');
client.index({  
  index: 'books',
  id: '1',
  type: 'books',
  body: {
    "Name": "The Book",
    "ISBN": "xyz",
    "Type": "Book",
    "Pages": 204
  }
},function(err, resp, status) {
    console.log(resp);
});
````
#### Count documents
````
client.count({index: 'books',type: 'books'}, function(err, resp, status) {  
  console.log("books", resp);
});
````
#### Delete document
````
var client = require('./connection.js');
client.delete({  
  index: 'books',
  id: '1',
  type: 'books'
},function(err, resp, status) {
    console.log(resp);
});
````
#### Searching documents
````
var client = require('./connection.js');
client.search({  
  index: 'books',
  type: 'books',
  body: {
    query: {
      match: { "name": "the" }
    },
  }
},function (error, response, status) {
    if (error){
      console.log("search error: "+error)
    }
    else {
      console.log("Response");
      console.log(response);
      console.log("Hits");
      response.hits.hits.forEach(function(hit){
        console.log(hit);
      })
    }
});
````
