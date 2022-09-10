# TodoList 

The web application where users can add or remove their to do list.   

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview


### The challenge

I was able to:

- View the optimal layout for each of the website's pages depending on their device's screen size
- To store data in MongoDB Atlas cloud service.
- Hosted the Web app in Heroku

### Links

- Solution URL: https://github.com/Soaphub/todoList/
- Live Url: https://floating-tundra-83202.herokuapp.com/ 

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Bootsrap
- Express.js
- Mongo DB for datatbase, Mongoose
- Mongo DB Atlas cloud services
- Mobile-first workflow


### What I learned

```.js
 app.get("/", function(req, res) {
  Item.find({}, function(err, itemsFound) {
    if (itemsFound == 0) {
      Item.insertMany(defaultItems, function(err) {
        if (err) {
          console.log(err);
        } else {
          res.redirect("/");
        }
      });
    } else {
      res.render("list", {
        listTitle: "Today",
        newListItems: itemsFound
      });
    }
  });
});
```

## Author

- Website - [Ambadi](https://floating-tundra-83202.herokuapp.com/)

## Acknowledgments

The udemdy coarse by Angela helped a lot in completing the project.
