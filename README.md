upiphany_test
=============
Hey this is a minimal proof of concept version chrome extension. To install it go to chrome://extensions/ in chrome and browse to the directory after clicking Load unpacked extension.
Using it:
-Select text
-Click little Hello button in top right of browser.
-Fill in notes and tags seperated by spaces. Click save.
-When you come back to the page the browser will alert you with saved content on the page.

What we need to do to make this fully functional:
-I'm working on finding out how to highlight the same content when you get back to the page.
-I'll make a User object.
-Link up to databse.
-Most importantly the webpage we send all the content to/outline page.


This code:
I made this more robust than the previous semi-hacky version I had. It has classes (well JS's class implementation...) for projects and references which each have properties. It'll be really easy to expand the number of fields we have.
The mechanism is that once you click save in popup.html, is tells background.js which asks content.js for the selected text and gets the tags and notes from the popup. It saves them under the project (just a predefined variable here but once I create a User object you'll be able to select projects you're working on). When you load a new tab it registers in the background which then checks if you have something saved under the url and sends it to that tab which displays it.
This part of the project is really simple... It's the webpage that's the special part and what we need to sell this idea.
