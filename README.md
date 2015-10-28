## Website Performance Optimization portfolio project

### Optimization For index.html

1. Resize the image that used in the page to reduce the KB of CRP resource need to be sent.
2. Minify the css and JavaScript.
3. Async the JavaScript to make it non-blocking.
4. Create a non-blocking css link via media query.
5. Incline style.css

### Optimization For pizza.html

1. In main1.js line 427 This one achieve the change pizza size within 5 ms:
Deleting determinDx function and transfer the function into changePizzaSizes. The determinDx is been used in loops,
so it will be called every iteration, but since the the size of the every pizza img and text div should be same, so
that we don't need to calculate the width every iteration.
2. In main1.js use faster Web API rather than document.queryall.
3. In main1.js make the variable declaration and assignment outside of loop.
4. In main1.js line 560. reduce the pizzas amount on the screen. previously it's 200. Right now it's dynamically changing
based on current screen size. For example my current screen height is only 812, so it'll have 24 pizzas on screen.
5. Add will-change to mover class to prevent continuously repaint same images.


#Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the Critical Rendering Path course.

To get started, check out the repository, inspect the code,

Getting started

Part 1: Optimize PageSpeed Insights score for index.html

Some useful tips to help you get started:

Check out the repository
To inspect the site on your phone, you can run a local server

$> cd /path/to/your-project-folder
$> python -m SimpleHTTPServer 8080
Open a browser and visit localhost:8080

Download and install ngrok to make your local server accessible remotely.

$> cd /path/to/your-project-folder
$> ngrok 8080
Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: More on integrating ngrok, Grunt and PageSpeed.

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js.

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: Chrome Dev Tools tips-and-tricks.

Optimization Tips and Tricks

Optimizing Performance
Analyzing the Critical Rendering Path
Optimizing the Critical Rendering Path
Avoiding Rendering Blocking CSS
Optimizing JavaScript
Measuring with Navigation Timing. We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
The fewer the downloads, the better
Reduce the size of text
Optimize images
HTTP caching
Customization with Bootstrap

The portfolio was built on Twitter's Bootstrap framework. All custom styles are in dist/css/portfolio.css in the portfolio repo.

Bootstrap's CSS Classes
Bootstrap's Components
Sample Portfolios

Feeling uninspired by the portfolio? Here's a list of cool portfolios I found after a few minutes of Googling.

A great discussion about portfolios on reddit
http://ianlunn.co.uk/
http://www.adhamdannaway.com/portfolio
http://www.timboelaars.nl/
http://futoryan.prosite.com/
http://playonpixels.prosite.com/21591/projects
http://colintrenter.prosite.com/
http://calebmorris.prosite.com/
http://www.cullywright.com/
http://yourjustlucky.com/
http://nicoledominguez.com/portfolio/
http://www.roxannecook.com/
http://www.84colors.com/portfolio.html