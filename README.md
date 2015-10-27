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
4. In main1.js line 560. This one achieve the 60fps performance:
The basicLeft is showing repeat same 8 results. Probably it's causing by too large i, so that divide it into 8 which
becomes 25.