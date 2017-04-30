---
title: A Simple Example
position: 1.1
type: post
description: Create Book
right_code: |
  ~~~ javascript 
  A: enable channel 1 for 30 minutes every 2 hours
  ~~~
  {: title="Rules" }
  !CODE_START!
    <img src="!SITE_URL!/assets/screenshot.jpg" alt="...">
  !CODE_END!
  {: title="Schedule" }
---
title
: The title for the book

score
: The book's score between 0 and 5

The book will automatically be added to your reading list
{: .success }

Adds a book to your collection.

~~~ javascript
$.post("http://api.myapp.com/books/", {
  "token": "YOUR_APP_KEY",
  "title": "The Book Thief",
  "score": 4.3
}, function(data) {
  alert(data);
});
~~~
{: title="jQuery" }
