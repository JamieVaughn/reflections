# Dragon Clicker Project Process Reflections

### July 19, 2021
I used a JS event listener on the dragon button (which was accessed via a query selector) to increment a `value` variable and update the inner text of the output HTML element. It was important to me to use query selectors to reference the important HTML elements, because I figured that I would want to reference those elements more times in the future, if the app scales up in some way.

Brendan's use of the [onlick event](https://www.w3schools.com/jsref/event_onclick.asp) attached to his dragon button in his HTML file was cool to see, and something I want to keep in mind for the future, if the client wants to add different numbers with each click in the future.

### July 20, 2021
With the addition of a dragon onto the screen, I decided that a) I needed to reference the `clicks` value inside the function that increments it, and b) I needed a generic function that would increment the `clicks` for any dragon on the page. In my HTML file, I added more structure to differentiate the two (or more, potentially) dragons from each other. Each dragon is surrounded by a `div` with a class of `.dragon`, a class of `.${color}` to style their background-color, and then each is labeled individually with an `id` describing their element (e.g., `#fire` or `#water`). Therefore, the `output` element in each dragon `div` can be referenced uniquely by using the `id` selector.

In the JS, I rehauled the clicker function to pass in two arguments: first, the amount to increment the clicks by (shamelessly inspired by Brendan's function); and second, the `id` attribute of the dragon `div`, referred to as "element" simply because the client seems to like elemental dragons. I then create a `selector` variable where I create a string that becomes my query selector for the output that I want to change. I then create my `clicks` var by coercing the current text of the selected output into a number, and then I can increment `clicks` by the passed-in `value`, and I can reset the text of the output to `clicks` after incrementing it.

I decided that I wanted to create a local `clicks` var within the function, instead of creating two global `clicks` variables, because if the client wants to put more dragons on the page, then local variables will scale easier than needing to create many global variables. I also decided to call these functions with the HTML `onclick` attribute and pass values into the function from the HTML instead of calling the function twice in the JS because, if the client decides that they want the user to generate dragons on the page, I can add that attribute easily to each dragon.

While I was structuring the HTML of the dragon `div`, I thought about the possbility of the client wanting the user to generate dragons of their own, and I believe that having generic `.dragon` and `${color}` classes and a unique `#element` ID lets each dragon be uniquely referenced while still being styled in a similar way. I anticipated the possibility of the client wanting more than one dragon of the same "element" to appear onscreen, and that might not be the case, but at least `${color}` classes can scale up better than applying CSS styles to the IDs instead.

### July 24, 2021
I moved the `addClick()` function into a `dragonFactory()` function that returns a dragon object, which also contains the `clicks` variable, a `selector` variable, and a `showDragon()` function. The two variables stored in the object are used in the `addClick()` function, just as in the last design iteration.

What's completely new is the `showDragon()` function, which is called on the `nav` buttons and displays each elemental dragon card. I went back and forth on the best way to structure this function (manipulate `innerHTML`? use `createElement()` and `appendChild()`?) before settling on manipulating the `innerHTML` of the `.arena`. From my research, it's faster than creating multiple elements and appending them, so I just set the innerHTML to the HTML necessary to show each dragon. (I also added in little emojis next to the dragons on each card, because I don't like the visual effect of `hue-rotate` on the colors of the dragon emoji. I plan to create an SVG of the dragon, and then I can change the colors with CSS that way.)

I still anticipate the client wanting to see multiple dragons onscreen at once! In which case, I think I will create a Boolean `onScreen` value on the dragon object, to keep track of whether or not each dragon card is onscreen, and then I can add and delete dragon cards based on that. I'll also have to create a `hideDragon()` function on the dragon object, and chance the `onclick` function attached to the nav button, but that should be simple.

### July 28, 2021
In order to organize the dragons and elements better, I created an `elements` array and a `stable` array. The `elements` array contains a list of elements used to create the dragons (right now: fire water, earth, air, heart - but which could be modified easily, and upon user engagement). The `stable` array is an array of dragon objects, created by iterating over the `elements` array with the `dragonFactory()` function. In this way, the data is more organized.

I also decided to spawn the navigation buttons on the page in the same way that I spawned the dragon objects, so I made an `addButton()` function to add buttons to the UI for however many elements/dragons exist.

I simplified the CSS so that the classes take the element names (instead of colors), just so I have to pss fewer arguments. I also replaced the dragon emoji with an SVG whose `fill` I can customize with CSS :)

I envision that the `elements` array could be added to via a form on the page, if the client wants the user to spawn their own dragons. If that's the case (and a user might want to create multiple fire dragons, for example), then I'll probably add a name for each dragon, so each can still b euniuely identified via CSS IDs.

### August 2, 2021
Making the app fit the MVC model was definitely the hardest part of this project so far. It felt like a lot of moving pieces. But in the end, I think the most difficult part was remembering to call `render()` when it needed to be called!

Since I was already generating my list of dragons, it was easy to move that part into the model. My `stable` of dragons was already being generated through the `dragonFactory`, and my nav buttons were already being generated from an array of `elements`, so I created `get` functions on the controller for the views to access them.

At first, I generated my `stable` in the `model.init()` function, but after I decided to let the user summon dragons via the nav buttons I made an `addDragonToStable()` function that pushes a dragon of a certain element into the `stable`. (And honestly, I had to make sme function names a little more specific, once I realised that I had `viewCards.addDragon()` and a `model.addDragon()`!)

In my views: my model is called 0 times, and my controller is called twice.

In my model: my views are called 0 times, and my controller is called 0 times.

In my controller: my views are called four times, and my model is called four times.