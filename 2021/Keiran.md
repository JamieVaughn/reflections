# Dragon Clicker Project Process Reflections

### July 19, 2021
I used a JS event listener on the dragon button (which was accessed via a query selector) to increment a `value` variable and update the inner text of the output HTML element. It was important to me to use query selectors to reference the important HTML elements, because I figured that I would want to reference those elements more times in the future, if the app scales up in some way.

Brendan's use of the [onlick event](https://www.w3schools.com/jsref/event_onclick.asp) attached to his dragon button in his HTML file was cool to see, and something I want to keep in mind for the future, if the client wants to add different numbers with each click in the future.

### July 20, 2021
With the addition of a dragon onto the screen, I decided that a) I needed to reference the `clicks` value inside the function that increments it, and b) I needed a generic function that would increment the `clicks` for any dragon on the page. In my HTML file, I added more structure to differentiate the two (or more, potentially) dragons from each other. Each dragon is surrounded by a `div` with a class of `.dragon`, a class of `.${color}` to style their background-color, and then each is labeled individually with an `id` describing their element (e.g., `#fire` or `#water`). Therefore, the `output` element in each dragon `div` can be referenced uniquely by using the `id` selector.

In the JS, I rehauled the clicker function to pass in two arguments: first, the amount to increment the clicks by (shamelessly inspired by Brendan's function); and second, the `id` attribute of the dragon `div`, referred to as "element" simply because the client seems to like elemental dragons. I then create a `selector` variable where I create a string that becomes my query selector for the output that I want to change. I then create my `clicks` var by coercing the current text of the selected output into a number, and then I can increment `clicks` by the passed-in `value`, and I can reset the text of the output to `clicks` after incrementing it.

I decided that I wanted to create a local `clicks` var within the function, instead of creating two global `clicks` variables, because if the client wants to put more dragons on the page, then local variables will scale easier than needing to create many global variables. I also decided to call these functions with the HTML `onclick` attribute and pass values into the function from the HTML instead of calling the function twice in the JS because, if the client decides that they want the user to generate dragons on the page, I can add that attribute easily to each dragon.

While I was structuring the HTML of the dragon `div`, I thought about the possbility of the client wanting the user to generate dragons of their own, and I believe that having generic `.dragon` and `${color}` classes and a unique `#element` ID lets each dragon be uniquely referenced while still being styled in a similar way. I anticipated the possibility of the client wanting more than one dragon of the same "element" to appear onscreen, and that might not be the case, but at least `${color}` classes can scale up better than applying CSS styles to the IDs instead.