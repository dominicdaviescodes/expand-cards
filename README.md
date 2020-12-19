# expand-cards


## What does the JavaScript do in this project?

We simply add the active class to the image we click on.
What happens then is the effect coded in CSS.  When we click on another image the class is removed from the current image.

When you click on the current image nothing happens.

First we need to bring in all the panels. This puts all the panels into a node list which is similar to an array, you can access items using bracket notation.


```js
// Grab the panels

const panels = document.querySelectorAll('.panel');

// can get the first panel 

console.log(panels[0])

```

### HTML DOM querySelectorAll() Method

Here we get all elements in the document with class="panel"

(from w3schools)
The querySelectorAll() method returns all elements in the document that matches a specified CSS selector(s), as a static NodeList object.

The NodeList object represents a collection of nodes. The nodes can be accessed by index numbers. The index starts at 0.

#### You can loop through a node list just like with an array. (2.25sec)