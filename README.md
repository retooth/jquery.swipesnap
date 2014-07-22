jquery.swipesnap
================

swipeSnap is a jquery plugin made for mobile applications. it allows users to move elements in one of the 4 directions (top, left, bottom, right) by swiping and snaps them back if the user lets go. it features a callback, which gets triggered when the user lets go after a certain threshold. usecases for this are e.g. navigation and list item management (think of the iphone app [clear](http://realmacsoftware.com/clear))

### Mandatory parameters:
* target - can either be "top", "left", "bottom" or "right"
* snapInfo - jQuery object that appears, when user swipes 

### Optional parameters:
* companions - a list of jquery objects which also get moved
* callback - a function that is called, if the user lets go and the snapInfo element is visible
* fadeDuration - the time it takes until snapInfo appears/disappears
* snapBackDuration - the time it takes until the element(s) are snapped back to their original position

### Example:
```javascript
$("#my-div").swipeSnap( { target: "top", snapInfo: $("#top-info"), 
                          companions: [$("#this-div"), $("#that-div")], callback: sayHello });
function sayHello () { alert("Hello"); }
```

### Dependencies

* [JQuery TouchSwipe](http://labs.rampinteractive.co.uk/touchSwipe/demos/)
