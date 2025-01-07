# Dragon Clicker Reflections

## Initial Request
To create my Dragon Clicker, I added a dragon emoji and gave it the class "dragon". I also created a blank 'span' area below it as a space for the click count to be generated.

Using JavaScript, I used .querySelector to target the dragon emoji and an eventListener to recognize when the emoji was clicked on.

I created a function to increase the click count by one when the dragon emoji is clicked on. Using the .innerText property, I appended the HTML document to include the click count.

## Dragon Clicker Duo
With the change in request from the client to include a second dragon, I duplicated the first dragon in the HTML doc and then styled each differently to represent fire or water.

I found that after adding the second dragon, only the first counter was functioning. I modified the HTML and JavaScript so each dragon is using unique classes, and this worked, but I'm not sure it is the preferred solution.
