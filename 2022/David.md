<h1>Reflections on Creating a Dragon Clicker App</h1>

<h3>Single Dragon (Initial steps)</h3>
<ul>
  <li>Set up the HTML to structure the page</li>
  <li>Added a JS event listener to the dragon button</li>
  <li>Created a CSS file to host some basic styling</li>
</ul>
<p>
I create an event listener to watch for user clicks, and chose to use a query selector to access the needed element (dragon button). When clicked,
it increments my value variable by one then updates the inner HTML of the output element (counter) so the end user sees the count increase. 

Originally, I had an alert set to respond to the user after each click. This was clunky and slow and had to be removed for rapid clicking.
</p>
<br>

<h2>Duo Dragons (Adding a 2nd dragon button</h2>
<ul>
  <li>Created a 2nd variable and 2nd eventlistener</li>
  <li>Applied hue-rotate to differentiate the two dragon buttons</li>
 </ul>
 
 <p>
Not overly happy with the current code. I had to duplicate code and know that if the client were to ask for more and more dragons, I would not be able to scale it easily. 

I played around with the hue for the two dragon buttons and came up with two colors I'm content with ("fire" and "ice" dragons). Previously, I was applying the style through ID identifier, but now each dragon has its own class to apply the styling.
</p>

<h2>Dragon Spawner (pre-MVC restructure)</h2>
<ul>
  <li>finalized styling on 5 dragon types</li>
  <li>added a navbar for each dragon type</li>
  <li>made a jumbled mess of my code</li>
</ul>

<p>In preparing to restructure the code into an MVC design, I moved pieces around into distinct sections that will develop into the model, controller and view components. I'm still struggling with the various functions needed, and a little confused how it all fits together. I procrastinated a bit playing around with styling. 

At this point, I still haven't been able to spawn a dragon object. I think there is something wrong with my "dragonFactory" function, or maybe the string template syntax. Hopefully refactoring into MVC design will help with debugging the issues. 
 </p>
