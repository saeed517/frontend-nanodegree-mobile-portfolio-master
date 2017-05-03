## Website Performance Optimization portfolio project

1. You can take a look at index.html [here](http://juanmartin86.github.io/frontend-nanodegree-mobile-portfolio-master/).
2. You can take a look at pizza.html [here](http://juanmartin86.github.io/frontend-nanodegree-mobile-portfolio-master/views/pizza.html).

## My Solutions

###Part 1: Optimize PageSpeed Insights score for index.html

#### What needs to be done?

1. Identify and perform optimizations to achieve a PageSpeed score above 90 on index.html.

#### What did I do?

1. Prevented render blocking JS by making analytics.js async. 
2. Prevented render blocking CSS by using media type "print" to print.css.
3. Set Google Fonts to load directly using @font-face. ????
4. Used grunt-uncss plugin to remove unused css from style.css. ??? 
5. Minifed style.css using grunt-contrib-cssmin plugin.????
6. Optimized style.css delivery by making it to inline CSS in index.html.???
7. Copied pizzeria.jpg to pizzeria100w.jpg and changed its width to 100px.   
8. Optimized pizzeria 100w.jpg and profilepic1.jpg using the online tool [Optimizilla](http://optimizilla.com/).(https://www.easy-resize.com/en/?gclid=CL-02Mqtx9MCFQML0wodYMAIOA)
9. Minified perfmatters.js using grunt-contrib-uglify plugin. ???
10. Minified index.html using grunt-contrib-htmlmin plugin. ??

#### Results?

Score of 95 Mobile / 97 Desktop on PageSpeed Insights --> [Here](https://developers.google.com/speed/pagespeed/insights/?url=http%3A%2F%2Fjuanmartin86.github.io%2Ffrontend-nanodegree-mobile-portfolio-master%2F)

#### References:

1. [Website Performance Optimization Course](https://www.udacity.com/course/website-performance-optimization--ud884-nd)
2. [Google Fonts using @fontface in your .css](https://coderwall.com/p/5vrdkg/google-fonts-using-fontface-in-your-css)
3. [How to get all font variations for font-face](http://stackoverflow.com/questions/25011533/google-font-api-uses-browser-detection-how-to-get-all-font-variations-for-font)

### Part 2: Optimize Frames per Second in pizza.html

#### What needs to be done?

1. Time to resize pizzas is less than 5ms in pizza.html shown in the browser console.
2. Identify and perform optimizations ensuring a consistent frame rate at 60fps when scrolling in pizza.html.

#### What did I do?

1. Optimized pizza.png and pizzeria.jpg using the online tool [Optimizilla](http://optimizilla.com/).
2. Used grunt-uncss plugin to remove unused css from style.css and bootstrap-grid.css (after this I realized that .mover was removed so I had to add it manually) and moved everything to style.css.

#### For the Pizza Resize Part:

1. Found that determineDx, changePizzaSizes and resizePizzas functions in main.js were making FSL.
2. Removed determineDx function, moved sizeSwitcher logic inside changePizzaSizes and used percentages instead of pixels.
3. Created variables to accomplish DRY.
4. Moved variables outside loops to prevent constant calling or creation.

#### For the 60 FPS on Scroll:

1. Found that updatePositions functions was making FSL.
2. Created a new variable named scrolledTop that handles document.body.scrollTop outside the "for" loop for preventing to be called each time.
3. Set var phase outside the "for" loop to prevent variable creation each time.
4. FSL was gone :) but still having FPS below 60.
5. Realized there was a lot of Painting so, decided to put will-change: transform on the .mover class (because it handles the pizza.png images on the background), job done.
6. Copied pizza.png to pizza100h.png and changed its height to 100px.
7. Optimized pizza100h.png using the online tool  [Optimizilla](http://optimizilla.com/).
8. Created variables to hold the length outside "for" loops.
9. Reduced the number of pizzas to be shown based on the browser's height.
10. Moved var elem outside the loop, to prevent constant creation.
11. Minifed style.css using grunt-contrib-cssmin plugin. 
12. Optimized style.css delivery by making it to inline CSS in pizza.html.
13. Minified main.js to main.min.js using grunt-contrib-uglify plugin.
14. Minified pizza.html using grunt-contrib-htmlmin plugin.

#### Other main.js tasks:

1. Changed querySelectorAll to getElementsByClassName due to its speed.
2. Changed querySelector to getElementById due to its speed.

### Other notes:

1. Inside the main.js file you can find more details of what I did.

### Results?

1. For Pizza Resize Part: Time to resize pizza 0.49ms in pizza.html (less than 5ms).
![Resize Pizza](results/resize-pizza.png)
2. For the 60 FPS on Scroll: Consistent frame rate at 60fps (or above) when scrolling in pizza.html.
![60 FPS](results/60fps.png)

#### References:

1. [Browser Rendering Optimization Course](https://www.udacity.com/course/browser-rendering-optimization--ud860-nd)
2. [getElementsByClassName VS querySelectorAll](https://jsperf.com/getelementsbyclassname-vs-queryselectorall/18)
3. [getElementById vs. querySelector](https://jsperf.com/getelementbyid-vs-queryselector/11)
4. [Abstract Away the Performance Faults of querySelectorAll](http://ryanmorr.com/abstract-away-the-performance-faults-of-queryselectorall/)

#### Other References in General:

1. [Grunt Tutorial](https://www.youtube.com/watch?v=zfzUH9Keu1s&list=PLpP9FLMkNf55_LqrPuSUxcs84bMvQiPD8)

### General notes:

1. I used a separate Developer Environment to install grunt to make the minify and uncss tasks to all the files here.


https://github.com/juanmartin86/frontend-nanodegree-mobile-portfolio-master
