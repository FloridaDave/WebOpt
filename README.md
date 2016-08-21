WEB OPTIMIZATION PROJECT NOTES

Github URL: https://floridadave.github.io/WebOpt

To view on local computer: Open index.html in your browser

PSI on index.com part (Obtained score of 97 on desktop and 95 on Mobile):

Optimized pizzeria.jpg by resizing to 100 px wide and lowering compression quality. 
Applied async to JS analytics code line (‘perfmatters’   already had async).
Moved CSS print call below footer and added media=”print” to limit when invoked.
In lined everything in CSS style as advised in training video. 
Applied Web Font Loader using JS as described on:
- https://www.lockedowndesign.com/load-google-fonts-asynchronously-for-page-speed/
- https://github.com/typekit/webfontloader/blob/master/README.md 
(Note: github referenced from Google Fonts web site)
Applied additional compression to pizzeria and profile images

Pizzeria FPS part (Obtained FPS ranging consistantly from .03 ms per page down down to .02 ms - sometimes less than that):

Optimized pizzeria_2 picture to 320 width (different from index.html which uses 100 width)
Modified total number of background pizzas from 200 to 24 (3 rows of 8 columns) 
Moved scrollTop calculation outside of for loop. (Strategy seen on https://engineering.gosquared.com/optimising-60fps-everywhere-in-javascript  with before and after work graphics to convey the reason for the dramatic improvement)
Changed var items = document.querySeletorAll to getElementsByClassName
Changed (at bottom of code) var items = document.querySelector to getElementsById
Changed var windowWidth = document.querySelector to getElementsById
Changed for (var i = 0; i < document.querySelectorAll to getElemantsByClassName
Changed var dx = determineDx(document.querySelectorAll to getElementsByClassName
Changed var newwidth = (document.querySelectorAll to getElementsByClassName
Changed querySelectorAll(".randomPizzaContainer")[i] to getElementsByClassName
Pulled randomPizzaContainer out of 4 lines of code and created var RPC to use in each of the for lines. 
Pulled the following lines of code out of the for loop an put them below the function because i is defined inside the loop. 
Changed var RPC to = document.getElementsByClassName("randomPizzaContainer");
Replaced previous lines (4) 'with getElementsByClassName("randomPizzaContainer")' with new var RPC
Removed 'document.' before each 'RPC'

