RenderFarm
==============================

Completely re-done.

Simple to use interface.

    $('.className').piggy({
 		focus: function(){
        },
		blur: function(offBottom){
		},
		scroll: function(offset){
		},
		render: function(offset){
		}
    }, true);

That's it. Nothing hard. Just target an element, and give it instructions for the cases that fit your needs.

#### focus ####
`focus` is triggered when the element appears on the screen

#### blur ####
`blur` is triggered when the element is scrolled off the screen. A boolean is passed to indicate if the element has been scrolled off the bottom.

#### scroll ####
`scroll` is triggered when the element is on the screen and the user scrolls. A value between -1 and 1 is passed to indicate how much of the element is on the screen.

When the element is exactly centered on the screen, offset is 0.

When the element is completely below the screen, offset is -1

When the element is completely above the screen, offset is 1.

#### render ####
`render` is triggered when the element is on the screen using requestAnimationFrame. A value between -1 and 1 is passed to indicate how much of the element is on the screen.

When the element is exactly centered on the screen, offset is 0

When the element is completely below the screen, offset is -1

When the element is completely above the screen, offset is 1.

There is a demo included showing how to control a Greensock TimelineLite animation with this new implementation. Everything else should be easy to figure out for yourself.

Enjoy animating everything!

http://codepen.io/cmndo/pen/PwoRyx

UPDATE
#### inside or outside ####
You can pass a boolean as a second parameter to the piggy function to tell RenderFarm if you want to track the element ONLY when it is fully inside the window.

TODO
need to recalculate some stuff when you resize, but that shouldn't be too hard. 
