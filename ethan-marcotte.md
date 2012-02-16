Ethan Marcotte ([@beep](http://twitter.com/beep))
===

1. Flexible grids
2. Flexible images and media
3. CSS media queries

e.g. Boston Globe

Maybe three ingredients is incomplete? They are about layout…
What about interaction?

##### Linear process currently: 
Discover -> Design -> Develop -> Deliver (Handoff on each step - work is complete)

How do we take image composites and wireframes of sites and envisage responsive versions of these pages.

When we design, we have a canvas. We have a width and a height. Not native to the web.

##### Solution?
Instead move to a cyclical agile approach for design-development
Designers introduce design for feature, layout, site etc.
Developers ask questions
Discuss: how sizes, layouts etc adapt, how things work on mobile, which requirements needed from developers.

**Question to ask for responsive:** "What value does this have for mobile users"
In line with [lukew.com/ff/entry.asp?933](lukew.com/ff/entry.asp?933) - design for mobile first

Mobile or Desktop = Less or More

Mobile devices offer us a choice - not tethered to a location to access the web, we can work completely mobile if we want.

> "Does this actually deserve to be here" - if content has no value for mobile users, how does it have value to any other users?

## Fluid Grid

Every grid has a context - e.g. 960px
Each column can have a relative context - e.g. 600 / 960  = x% - retain proportions

## Flexible images

Scale images easily: max-width: 100%;
Also consider actually different size images

## Media Queries

Create list of breakpoints for different types of devices
Base on device type, type of content, and site layout

e.g. min-width 320, 480, 768, 900 should cater to phone, smartphone, etc.

[Respond.js](https://github.com/scottjehl/Respond) can patch media query support into other browsers!

Could do @imports for more modular stylesheets? Is @import supported in places other than the top of the document?

Adaptive vs. Responsive design? Apparently responsive is a subset of adaptive

Boston Globe: use min-width only, and start with smallest, up to largest - means that default experience is for the most scalable, mobile version.

Test for @media query support or IE - store this somewhere, so you can provide better content and content layouts depending on how they are using the site (i.e. less image loading, etc.)


