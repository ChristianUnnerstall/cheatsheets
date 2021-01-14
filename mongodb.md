#### mongo
````
mongo mongodb://<connection>
mongo mongodb://localhost:27017/myDatabase?ssl=true
````
#### mongo Commands
````
help
db.help()
db.<collection>.help()
show dbs
use <db>
show collections
show users
show roles
show profile
show databases
load()
````
#### mongodump
````
# backup data
mongodump --gzip --db "<database>" /out:"<directory>"
````
#### mongorestore
````
# restore data
mongorestore --drop --gzip --uri \ "<uri>" "<directory>"
````

##### .find()
````
db.<collection>.find({})
db.<collection>.find( { 'title': 'My Title' } )
db.<collection>.find( { 'title': { $regex: 'Title' } } )
````

##### .insertOne()
````
db.<collection>.insertOne( { 'title': 'My Title' } )
var doc = { 'title': 'My Title' }
````

#### Aggregation
##### $lookup
This aggregation pipeline describes a scenario where to lookup comments to one post. The lookup pipeline section sorts the comments in descending order.
````
const pipeline = [
    {
        "$match": {
            "_id": ObjectId(id)
        }
    },
    {
        "$lookup": {
            "from": "comments",
            "let": {"id": "$_id"},
            "pipeline": [
                {"$sort": {"date": -1}},
                {"$match": {
                    "$expr": {
                        "$eq": ["$post_id", "$$id"]
                    }
                }}
            ],
            "as": "comments"
        }
    }
]
...
collection.aggregate( pipeline )
````

##### $group
````
const pipeline = [
    { $match: {} },
    { $group: { _id: "$category", content: { $push: "$$ROOT" } }},
    { $sort: { "_id": 1}}
]
...
collection.aggregate( pipeline )
````

#### INDEX
##### Create Index
````
db.<collection>.createIndex({ "title": -1 }) // 1 for ascending order
````
##### Create Text Index
````
db.<collection>.createIndex({ "description": "text" })
````
##### Create unique Index
````
db.data.createIndex({ 'permalink': 1}, { unique: true } )
````
