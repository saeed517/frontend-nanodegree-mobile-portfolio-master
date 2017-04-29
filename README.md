## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository and inspect the code.

### Getting started

1. You can take a look at index.html [here](http://juanmartin86.github.io/frontend-nanodegree-mobile-portfolio-master/).
2. You can take a look at pizza.html [here](http://juanmartin86.github.io/frontend-nanodegree-mobile-portfolio-master/views/pizza.html).


#### Part 1: Optimize PageSpeed Insights score for index.html

To identify and perform optimizations to achieve a PageSpeed score above 90 on index.html, I have done the following steps:

1. I prevented render blocking CSS by using (media = “print”) to print.css.
2. I prevented render blocking JS by making analytics.js async. 
3. I have changed pizzeria.jpg to pizzeria100w.jpg and I changed picture width to 100px.
4. I added style.css delivery through making it to inline CSS in index.html.
5. I optimized pizzeria 100w.jpg and profilepic.jpg using the online tool. (https://www.easy-resize.com/en/?gclid=CL-02Mqtx9MCFQML0wodYMAIOA)


#### Results:

Score of 95 Mobile / 97 Desktop on PageSpeed Insights --> (https://developers.google.com/speed/pagespeed/insights/)

#### References:

1. [Website Performance Optimization Course](https://www.udacity.com/course/website-performance-optimization--ud884-nd)
2. [Google Fonts using @fontface in your .css](https://coderwall.com/p/5vrdkg/google-fonts-using-fontface-in-your-css)
3. [How to get all font variations for font-face](http://stackoverflow.com/questions/25011533/google-font-api-uses-browser-detection-how-to-get-all-font-variations-for-font)


#### Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js. 

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>
