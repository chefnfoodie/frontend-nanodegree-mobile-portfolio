## Website Performance Optimization portfolio project

####Part 1: Optimize PageSpeed Insights score for index.html

Changes made:
1. CSS inlined and web fonts included as inlined style in minified form.
2. Google analytics and perfmatters javascript files have been tagged with async.


####Part 2: Optimize Frames per Second in pizza.html

File: pizza.html
* css is minified and inlined.

File: mover.css
* Added will-change: transform, translate :transform to reduce layout time.

File: main.js
* Replaced querySelectorAll, querySelector method calls with getElementsById and getElementByClassName respectively
* Reduced pizza count from 200 to 20 since only lesser number is needed.
* Update for-loop where pizza are appended - moved getting randomPizzas element by id outside the loop
* Added pizzaelements array to hold pizza elements. This eliminates the need to search the DOM again
* Inside updatePositions method, moved the computation of (document.body.scrollTop / 1250); outside the loop to reduce repeated computation
* Updated updatePositions method loop iteration to use pizzaelements array'
* Inside updatePositions method, removed mod operation with counter logic
* Replaced window.addEventListener('scroll', updatePositions); with window.requestAnimationFrame(updatePositions); and added window.requestAnimationFrame(updatePositions); 
* Refined changePizzaSizes method to improve the performance

### References
1) http://cssminifier.com/ - Used in the project to minify CSS file


