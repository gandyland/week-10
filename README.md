# Week 10

## Mongoose

### Question #1

Describe the differences between a SQL and NoSQL DB, and when you might use each.

```text
SQL uses tables to store the data in very strict fashion while NoSQL does not have the same strictness and allows us to add varying types of data. I think.
```

### Question #2

What's wrong with this mongoose code and how might we fix it?
(Hint: Assuming there is a document with a name of "Bob", why is results not an author model on the second line?)

```js
var results = AuthorModel.find({name: "Bob"});
console.log(results);
```

```js
Its missing the callback function so just need to add one.

var results = AuthorModel.find({name: "Bob"}, function(results){
  console.log(results);
});
```

### Question #3

Convert the following ActiveRecord sequence to Mongoose:

```rb
@andy = Instructor.find_by(name: "Andy")
@andy.wishlist_items.create(description: "Resin Laying Deer Figurine, Gold")
```

```js
Instructor.findOne({name: "Andy"), function(err, andy){
  andy.wishlist_items.push({description: "Resin Laying Deer Figurine, Gold");
  andy.save();
});
```

### Question #4

Convert the following create method in Mongoose to ActiveRecord.

```js
  var authors = {
  create: function(req, res){
  var author = new AuthorModel({name: req.body.name})
  author.save(function(err){
    if (!err){
      res.redirect("authors")
    }
  })
  }  
}
```

```rb
@author = Author.create!(name: params[:name])
```
## Express

### Question #5

How does module.exports help us with separation of concerns?

```text
Module.exports allows us to separate our js files by exposing their contents as one global variable.
```

### Question #6

Write one Express route for each of the four HTTP methods.

Then, make each route respond with a one-word string containing the RESTful action that would most likely be associated with this route.

```js
var express = require("express");
var app = express();


wat?

```

```js
seriously, wat?

just go ahead and mark this one incorrect.
```
### Question #7

Describe the differences between Express and Rails as backend frameworks.

```text
Express has fewer rules and gives you more leeway in how you can use it and structure it.

Rails is written in Ruby and has a buttload of rules it has to follow.
```

### Question #8

What is the importance of using body-parser in our express application for post requests?

```js
I think it is necessary for processing the information from the post request.
```
