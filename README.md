## Website Performance Optimization portfolio project


These are things I did to optimize my page. Keep scrolling and Read below for specifics

1.  Watched a office hours with Mark over and over and over. Literally 10 times until I understood it.
2.  Took suggestions from office hours, read the Udacity forums.  Asked questions to many other students
3.  went to https://developers.google.com/speed/pagespeed/insights/ and put in my code from index.html and pizza.html and listened to all of their suggestions.
4.  Some things I did.  Inlined my css, asnyc'd my javascript compressed picture sizes, Moved Javascript to reduce render blocking.
	Minified my javascript.
5.  Google, Google, google, google, and when I was done googled some more.  Then I googled.
6.  I commented all my code where I made my changes so the instructor can review where I did what I did.

List of Main.js Changes.

1. moved a few things out of the for loop to make it run faster, didnt need to get the randomPizzaContainer, dx or the newwidth each time in the loop.

2. Moved the outside the loop also.  So it doesnt do it 100x only once. 
var pizzasDiv = document.getElementById("randomPizzas");

3.  faster way to access the DOM than querySelectorAll changing to getElementsByClassName. Suggestion per Office Hours.

4.  Instead of style.left changed it to style.transform = "translateX(".  Per office hours suggestion

5. Changed Columns in the below to 5 from 8.  Only shows 5 at a time at most anyways.  
  var cols = 5;
  var s = 256;

6. Changed it to 30 in the below loop from 200, per office hours suggestion.  Doesnt need to go all the way to 200
  for (var i = 0; i < 30; i++) {


Index.html Changes

1. Inlinded all of my css

2. Optimized images and made smaller versions
profilepic is now 11kb, pizzeria is 1kb

3. removed css/style.css 

4. moved .js files below to assist in renderblocking 
    <script src="http://www.google-analytics.com/analytics.js" async ></script>
    <script async src="js/perfmatters.js"></script>

5. added media=print in code
 <link href="css/print.css" rel="stylesheet" media="print">

6. Removed <link href="//fonts.googleapis.com/css?family=Open+Sans:400,700" rel="stylesheet">


Pizza.html Changes

1. minified my javascript to mainmin.js

2. compressed image pizza2 down to 9 kb

3. added Meta Vewport per PageSpeed Insights suggestion

4. inlining my CSS and the bootstrap CSS

5. Added Hardware acceleration to increse performance

6. remvong below CSS and bootstrap css--> 
<link rel="stylesheet" href="css/style.css">
<link rel="stylesheet" href="css/bootstrap-grid.css">




Other reading material.  Read some, not all of the the links below trying to get anything out of it that I could.  


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


