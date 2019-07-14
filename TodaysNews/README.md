# Mongoose-Scraper
### A web app that lets users view and leave comments on the latest news. 

This full-stack application allows a client to scrape headlines, links, and (if available) excerpts from the Daily Universe website.  The client can then save the articles in a database, delete saved articles, make notes on specific articles, and delete those notes.

![Daily Universe website](public/css/images/dailyuniverse.JPG)

### Scraping

The application uses "request" and "cheerio" for scraping the Daily Universe HTML.  The articles scraped are compared to the ones in the database, and if the articles hasn't already been stored, it is put into an object which is rendered on the "/scrape" route with the help of the "express-handlebars" npm package.  Both the scrape page and the Saved Articles page display links to the associated articles so that the user may check out the full articles before saving or writing a comment.

![Scrape route](public/css/images/scrape.gif)

### Saved Articles

The articles are saved to the database with the help of the Mongoose NPM. According to their page, "Mongoose is a MongoDB object modeling tool designed to work in an asynchronous environment."  This application uses Article and Note models with the Article model containing an array "note" that stores the ObjectIds of any associated Note. From the Saved Articles page, the client can delete an article from the database or navigate to the article's Note/Comment page in order to see any associated notes/comments or to make a comment.  The data on all routes is redered with "express-handlebars".

![Saved Articles Route](public/css/images/savedPage.JPG)

### Comment Section 

The client can make a note or read a comment by navigating to the "/articles/_id" route where the user can read, delete, or create a comment/note.

![Article Comments Route](public/css/images/notePage.JPG)

##### About this Application

This repository is for an application deployed at: https://boiling-island-52680.herokuapp.com/
This repository is for a full stack JavaScript application, employing various technologies, including NPM packages (Express, Express-Handlebars, Body Parser, Morgan, Mongoose, Request and Cheerio), Handlebars templating, database handling, and styling with CSS. 
The application allows the client to interact with a server to submit and update data. The application employs a simple client/server full-stack approach, with a front end (HTML-Handlebars, CSS), middleware (Express, Body-parser) and back end (Mongoose models).  This project was created and is maintained by me, Marjika Howarth.
