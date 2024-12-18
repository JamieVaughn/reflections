# Clicker Game Reflections

## First Dragon

At first my first code worked but not 100% the way I wanted it too and when I started to change things / fix bug it became a little tough. So for the sake of organization I rewrote the code. Also wanted to make the clicker game more adaptable for future changes, and possible future design customization with CSS. Both  javaScript, and CSS are now linked inside the Html. 

This clicker new updated game was built with the idea of setting up the html page as usual head - body - h1 with the Title of the game - h2 being where the score will be shown - a span with an id of score board with int. val being 0 till button is used and allowing the script to update the new score per action (button click) Also an img for the image of the item that will be targeted for the game. button was created with an id of click me with an increment unit of +1 for each click action within the js clicker. 

The css style is kept simple fore now just helping create a block style display for the 1st image. Also added a height, width and margin to keep future images or content organized, have some aspect of design, as well as be a bit more esteticly pleasing. 

Also targeted the html in the style sheet to overide default, the font size and box size for the same reasons. 

In the clicker.js document a function was created to start the variable score with int. val of 0 - along with targeting the buttion and creating an eventlistenter which calls the add to score function when the person clicks the button for the game.

When the button is clicked i console log "clicked" so that we know that the function is working correctly. Added it for debugging purposes. 

Over all for me it was a lot easier to break each down to three seperate folders and hoping it will allow for an easier transition to more cusomization or updated content request from our dragon clicker client.

Create 2 seperate functions for each button and added a few divs to wrap the image and the buttons so that they align a bit better. 
