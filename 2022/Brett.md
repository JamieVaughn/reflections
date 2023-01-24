Dragon-clicker App Notes
Revision 1 
I have a basic emoji that can increment once the box with the innerText is clicked on.  To achieve the functionality that is expected, I am experimenting with other coding methods(naming different constructor functions or making use of addEventListener with a div variable declaration).  

Revision 2
I can update the clicks for two dragon emojis of the same type - two separate dragon emojis(containers) two separte counters.

Drawback:
I am having difficulty updating the clicks for two dragon emojis of a different type.  The first trial resulted in the second emoji type reverting back to the original or first emoji type.  With the code that I am currently writing I can update only one emoji between two separate or different emojis.  

Final update: I was able to get the second clicker function to work on the script.js file so that each dragon increments independently of one another.

Revision 3:  
The factory function was a lot more difficult than I expected but the scalability and UI/UX is much more advanced simply because I can add more 
dragons to the dragonTypes and then add a new CSS class for that dragon card - i.e. almost unlimited # of dragons with varied CSS options.  I think that the code is 
more flexible but more complicated than just one or two dragons with separate clicker functions.  I do not see any real issues with scalability 
other than making the code more manageable or reusable.

Revision 4:
View does not get called within Model and Model does not get called within View.  
Controller gets called 4 times within View and 0 times within Model. Model gets called 6 times within Controller and View gets called 2 times.

