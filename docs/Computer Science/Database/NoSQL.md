Database	Database
Table     	Collection
Row/Entity	Document
Column          Key



show db                 --? show all available databases
use namedb		---? access database
show collections        ---? show all the collections on the database
db.mydb.help()          --> show all functionalities of the database
db.dropDatabase()	---> To drop the database
db			 --> to see current database


db.name.insert({name : Tom, age: 12})
db.name.save({name : "Craterus", role : "General"}) # _id field is 

db.dbname.insertOne({name : "Perdicass", age : 35})

db.dbname.insertMany({name : "Meliyager", role : "Distraction"}, {name : "Coenus", role : "Right Flank"})

db.dbname.updateOne({name : "X1" , age : 25})


db.dbname.updateMany({name : "X2", age : 23},{name : "X3", age : 42})

db.updateOne({name : "X8", {set : $age : 14}})


db.collection.replaceOne({name : "W2"}, {name : "R4"})


db.dbname.deleteOne({name : "SAE"})
db.dbname.deleteMany({name : "XLS"})


db.collectionName.remove(); or db.collectioName.remove({})

------------------------------------------------------------------------------------
READ operations


db.collectionName.find({name : "CS"})
db.collectioName.findOne({name : "SS"})



db.collectionName.find({name : "OPTIO"})


db.collectioName.find({name : 'ERR'},{id : 0 , age : 1})


db.collectionName.find({name : 'KL'}, {id : false, address : true}).pretty()


Question
Update Tom's marks to 55 where marks are 50 (Use the positional operator $)


db.collectionName.updateOne({name : "Tom", marks : 50}, {"$set" : {"marks.$" : 55}})

--------------------------------------------------------------------------------------------

default port is 27,017


import pymongo

client = pymongo.MongoClient('localhost', 27_017)
db = client.mydb.mycollection()
