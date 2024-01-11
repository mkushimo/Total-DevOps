mongod --version: It will gives the MongoDB Server version.

mongo -version: It will gives the MongoDB Shell version.
Mongo Shell is the command line client.

To login into mongo db just type mongo command.

db.createCollection("students"): It will create a collection called students.


db.students.insertOne( {
    name: "Mithun",
    age: 07,
    status: "A"
 } )
