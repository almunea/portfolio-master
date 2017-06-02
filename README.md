## Website Performance Optimization portfolio project

Live version

A live version of the website can be found on 
#####https://almunea.github.io/portfolio-master/index.html



####i changed 
index.html, project-2048.html, project-mobile.html, project-webperf.html, Inlined all style sheets, Created local copies of images and thumbnails, resized images too large Made script calls async Closed off


###index.html


1. Optimised pizzeria.jpg from 1 very large 2Mb to 2 images: one 293px w and one 720px w (based on their used in pizza.html)
2. used pizza_293.jpg in index.html
3. Inlined all style sheets.
4. Removed Google font line as it seems to take way to long to load and is blocking rendering.
5. Optimized (ImagOptim) /img/profilepic.jpg. Also downloaded thumbnails and serving from /img to be sure they are fully optimised.



###Pizza.html Resized pizzeria.jpg

###Main.js

1. Added pizzaImage size in pizzaElementGenerator
2. Optimized changePizzaSizes Moved new width claculation outside of loop, needs to be calculated only once since all pizzas are the same size Replaced document.querySelectorAll(".randomPizzaContainer") with variable reference to all generated pizzas
3. Optimized randompizza appending loop Moved randomPizza reference outside of loop so it is not recalculated Added variable to store reference to all random pizzas so change pizza size does not have to recalculate
4. Optimized function updatePositions() Storing all moving pizzas in var items outside of function
5. Optimized document.addEventListener('DOMContentLoaded', function() {} Optimized algorithm to generate scrolling pizzas to produce only 32 elements instead of 200 Changed elem.src to prescaled image Floored the value of width