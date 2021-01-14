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
