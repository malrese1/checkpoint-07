# Week 10

## Mongoose

### Question #1

Describe the differences between a SQL and NoSQL database, and when you might use each.

SQL databases are primarily called as Relational Databases whereas NoSQL database are primarily called as non-relational or distributed database.

SQL databases scale vertically, while NoSQL databases scale horizontally.

SQL databases emphasizes on ACID properties  whereas the NoSQL database follows the Brewers CAP theorem

NoSQL handles hierarchical data better than SQL. Hence, NoSQL is preferable to SQL when managing big data.



### Question #2

What's wrong with this Mongoose code and how might we fix it?

```js
var results = AuthorModel.find({name: "Bob"});
console.log(results);
```

> Hint: Assuming there is a document with a name of "Bob", why does `results` not contain an author model on the second line?

```js
// needs a callback function
var results = AuthorModel.find({name: "Bob"}, function(results){
   console.log(results);
 });


### Question #3

Convert the Ruby and ActiveRecord code below into Javascript and Mongoose code:

```rb
@andy = Instructor.find_by(name: "Andy")
@andy.wishlist_items.create(description: "Resin Laying Deer Figurine, Gold")
```

```js
// Your answer...
```

### Question #4

Convert the following create method in Mongoose to ActiveRecord.

```js
var author = new Author({name: req.body.name})
author.save(function(err){
  if (!err){
    res.redirect("authors")
  }
})
```

```rb
# Your answer...
```
author = Author.create(name: => "author's name")

## Express

### Question #5

What is module.exports and why do we use it?

```text
Your answer...
```
it is an object thats returned as a result of a require call. we use this to scope functions

### Question #6

Write one Express route for each of the four HTTP methods.

Then, make each route respond with a one-word string containing the RESTful action that would most likely be associated with this route.

```js
var express = require("express");
var app = express();

// Your code starts here...

```

### Question #7

Describe the differences between Express and Rails as backend frameworks.

```text
Your answer...
```

### Question #8

What do the following lines of code do?

```js
var bodyParser = require("body-parser")
app.use(bodyParser.json())
app.use(bodyParser.urlencoded({extended: true}))
```

```text
Your answer...
```

### If You Finish Early...

Take a look at these [front end developer interview questions](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/README.md)
