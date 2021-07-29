# Dragon Clicker Reflections

## Single Dragon

I displayed a single unicode dragon image with increased font size. It
was displayed div based card that included a button for clicking and and output element to show the number of clicks. I used the html onclick on the button to identify the function to run. HTML elements were added to the DOM by appending them other DOM elements that had been identify using either the querySelector or getElementByID methods of the document.

## Double Dragons

Here I changed how I stored the dragon data. I created an array of objects, one for each dragon. The Objects contained the type of dragon, the class used to style the object, and the number of clicks. I included some filters to alter how the dragons image was styled.

I let the array control the number and order of dragons displayed, looping through the array, calling a factory style method and passing the array index.

## Dragon Arena

...
