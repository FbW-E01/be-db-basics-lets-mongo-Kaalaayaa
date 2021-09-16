# Backend - Database - Basics - Let's MonGO

## Let's monGO

Add your answers directly into this README file.

1. Explain ObjectIDs in MongoDB; what are they?
Every document in the collection has an “_id” field that is used to uniquely identify the document in a particular collection it acts as the primary key for the documents in the collection. “_id” field can be used in any format and the default format is ObjectId of the document.

An ObjectID is a 12-byte Field Of BSON type. The first 4 bytes representing the Unix Timestamp of the document. The next 3 bytes are the machine Id on which the MongoDB server is running. The next 2 bytes are of process id. The last Field is 3 bytes used for increment the objectid.

2. You have a collection called "users" with a document like this: `{ _id: 1, name: "Veera" }`. What query would you use to update the name to "Princess Veera Silkenfur"?

db.users.updateOne(
    { "name": "Veera"},
    { $set: { "name": "Princess Veera Silkenfur" } }
)


3. How do you make a collection?

db.createCollection("collectionName")

 or 

db.collectionName.insertOne({ name:"hello", lastName: "World"})


4. So the (old) mongo shell is kind of like a JavaScript REPL. What is a REPL? Which other REPL have we used?

A read–eval–print loop (REPL), also termed an interactive toplevel or language shell, is a simple interactive computer programming environment that takes single user inputs, executes them, and returns the result to the user; a program written in a REPL environment is executed piecewise.



5. So the (old) mongo shell is kind of like a JavaScript REPL. You can use things like variables, try...catch  statements and loops. Experiment with it and find at least three other JavaScript things that we have used that work in the (old) shell. If you can, try to find even more!

- defining and calling function : 
function myFunction(){
  print("Hello World");
}

myFunction()


- Replacing a word in a string:

const username = "Kala";
var output = "<username> please enter your password: ";
output.replace("<username>", username);

- Creating and Manipulation Arrays:

const weekDays = ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"];

weekDays.unshift("Sunday");


6. (Research) So the old shell is pretty cool. How is the new shell better?

Improved syntax highlighting.
Improved command history.
Improved logging.


7. (Research) How can you insert multiple documents at the same time?

db.products.insertMany( [
      { item: "card", qty: 15 },
      { item: "envelope", qty: 20 },
      { item: "stamps" , qty: 30 }
   ] );


8. (Research) You have a collection called `cats` with a documents like this: `{ name: "Veera" }, { name: "Rauli" }, { name: "BenBen" }` - How can you insert the field `cute: true` into all of them with one command?

db.cats.updateMany({}, {$set: {cute: true}})



9. (Task) Start a timer for 30 minutes. Spend all that time getting to know and reading https://docs.mongodb.com/manual/introduction/ - how far did you get? What was the most cool or interesting thing you learned?



10. Find one SQL Cheatsheet and one MongoDB Cheatsheet and add links to them here.

https://learnsql.com/blog/sql-basics-cheat-sheet/


https://www.mongodb.com/developer/quickstart/cheat-sheet/

































🌿
