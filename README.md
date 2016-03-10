## Website Performance Optimization portfolio project

This is a website performance optimization project worked on 
a given sample site by the Udacity Team.

### Getting started

In the main directory you have two separate folders,
the original one and the one where the optimized work was
performed, named here as src and dist one respectivelly.

####Part 1: Open index.html file

Some useful tips to help you get started:

Check out the speed on google developers page [here](https://developers.google.com/speed/pagespeed/insights/). This was the initial measure phase where I received a few hints from the inspector on how to
proper start and adress the project

For optimizations and working on the critical rendering path, the following
steps were taken:
*  Inlining CSS;
*  Minify CSS and JS files (available on the css and js folders respectivelly)
*  Use of the tag async for certain script files
*  Use of the google script to replace the google font link tag 
*  The Gruntfile.js optimizes the images for the html file and
   place them on a new folder called images_production


####Part 2: Open the pizza.html file inside the views folder

Some useful tips to help you get started:

Most of the work done here was to reduce the frames per second rate. 
Check out the main.js file,inside the js folder, where some web performance 
tasks were created in order to reduce the 30fps to 60fps.

Using chrome dev tools to analize the pizza.html file, there were issues found initially with
the javascript file (main.js), the work was divided in two steps
*  reworking on the updatePositions function - related to the pizzas animation in the background
*  reworking on the changePizzasSize function - related to the slider that toggles the pizzas sizes

In order to attempt to optimize even further,in the style.css file, inside the css folder, I also used some CSS3 tricks for layout and style rendering optimization.
*  transform: translateX(), 
*  backface-visibility: hidden - for creating one layer per pizza when during the paint fase in rendering
*  will-change: transform - a hint for the browser about the kind of changes expected for a certain 
   element

I also minified the css and js files in this working directory


