# My Dragon Clicker Project Log

I'm making a javascript app and I'll be recording my thoughts as I go here!

### Dragon Clicker
- I don't think this is scaleable
- It was easy enough to manage for now
- I think its simple enough for anothe developer to understand

### Dragon Duo
- I just duplicated the dragons in my HTML
- I added the fireClicks & waterClicks variables to hold the clicks for the two dragons
- I'm listening to the click even for each dragon to update the clicks and then rerender the innerText with the new click count

### Dragon Gang
- Now loops are coming into play
- looping over an array of the types of dragons
- using a dragonStamper function to write a dragon for each type to the DOM
- looping over each of the dragon DOM elements to addEventListener to each one
- storing a separate click value for each dragon by it's type in a key
- in the click even handler, incrementing the click count for that particular dragon by one and updating the DOM