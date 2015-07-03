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
* Compressed images for index.html.
* Added code to generate pizzas to fill the screen within window height.
* Included case 3 with new width: 50 in changePizzaSizes function.
* Array length has been specified outside the for loop for optimization.
* Phase and elem variables have been declared outside the loops and phase has been modified to include'*100'.
* Strict mode has been enabled for some functions.


####Part 3: Instructions to run
To inspect the site on your phone, you can run a local server

$> cd /path/to/your-project-folder
$> python -m SimpleHTTPServer 8080

Open a browser and visit localhost:8080

Download and install ngrok to make your local server accessible remotely.

$> cd /path/to/your-project-folder
$> ngrok 8080

### References
1) http://cssminifier.com/ - Used in the project to minify CSS file


