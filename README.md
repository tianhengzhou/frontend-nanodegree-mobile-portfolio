## Website Performance Optimization portfolio project

### Optimization For index.html

1. Resize the image that used in the page to reduce the KB of CRP resource need to be sent.
2. Minify the css and JavaScript.
3. Async the JavaScript to make it non-blocking.
4. Create a non-blocking css link via media query.
5. Incline style.css

### Optimization For pizza.html

1. In main.js line 427 This one achieve the change pizza size within 5 ms:
Deleting determinDx function and transfer the function into changePizzaSizes. The determinDx is been used in loops,
so it will be called every iteration, but since the the size of the every pizza img and text div should be same, so
that we don't need to calculate the width every iteration.
2. In main.js use faster Web API rather than document.queryall.
3. In main.js make the variable declaration and assignment outside of loop.
4. In main.js line 560. reduce the pizzas amount on the screen. previously it's 200. Right now it's dynamically changing
based on current screen size. For example my current screen height is only 1080, so it'll have 40 pizzas on screen.
5. Add will-change to mover class to prevent continuously repaint same images.

### How to setup and run this project
#### Method 1: Create a local server.
 1. Change directory to your project folder
 2. Make sure you have python install in your computer.
 3. In your project's root type python -m SimpleHTTPServer 8080
 4. Open a browser and type localhost:8080 to visit the index.html.
 5. There is a link for pizza.html in index.html. Click the link to visit pizza.html
#### Method 2: Github pages
 1. Create a gh-pages branch in your repo on github.com
 2. type yourusename.github.io/yourreponame to visit the page.
