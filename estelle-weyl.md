Estelle Weyl
====

* Fast to load, render, response, understand
* YSlow, Page Speed extension

#### Four Points for Mobile Optimization

1. Eliminate reflows
2. Reduce number of DOM elements
3. Defer JS parsing
4. Make fewer requests

#### Battery

* Stuff like large images, CSS animations, intensive JS sucks battery
* CPU uses battery - avoid repaints, JS, JS animations (uses setTimeout), WebGL
* Allow the device to take breaks

#### Latency

* DNS request is still a request
* Remember the steps on mobile data - device -> tower -> telco switch -> internet
* Antipattern - m.bing.com - embed JS and CSS in head of document on first page. Then they extract CSS, JS and data URIs for images and saves in localStorage. They then do a 'diff' request using cookies - tell servers what they have, servers only sent files they need and do not have

> Wonder if there's Rack middleware for this?

> Is that actually different from using a cache manifest in HTML5?


#### Memory

* Keep in mind most phones have between 128mb-512b of RAM. That's really not much
* MBP has 4-8gb of RAM - it's not sufficient to test mobile sites on a laptop and assume it will work on mobile devices

#### Images
* Not enough to GZip
* Need to shrink image file size
* Use data URIs
* "Image Alpha" - http://pngmini.com/
* Use different background images with media queries
* Sencha.io - pass in URL to image and it will work out how large the image should be - saves having to create the images
* Investigate CSS3 masking to reduce the need for images with lots of solid blocks of background

#### Box Shadows

* Using inset and outset borders are repainted on each repaint or reflow (not rendered as bitmap)


#### Text Indent

* Normally left: 999em or whatever
* With mobile devices, it's a viewport - it's drawing everything and keeping that in memory
* Instead, use CSS clip and position text up


#### Gradients

* Images are often faster
* Keep them small (require CPU and memory)
* Viewport thing again - mobile browser will render the gradient that is offscreen, as well as onscreen

#### Out of viewport context

* Said this three times now, but everything is rendered
* meta viewport scale, width etc doesn't change what is rendered - just what is shown


### UI Responsiveness

* Touch events - on tap (normally we listen for click), it listens for 300ms for another tap so it can count it as a double tap
* Responsive UI - give feedback - i.e. if a tap is going to load a page, and it's going to take longer than 200ms, give them something to say that the event has been received.

### Testing
 
* Test on mobile data
* Make sure you have lots of apps open
* Simulator != Emulator






