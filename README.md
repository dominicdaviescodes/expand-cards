# expand-cards

All notes note made by me are (from w3schools)

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
The panels with active class on first image: 
<!-- ![a photo of the project](/img/panels.JPG) -->
<!-- to control width of img used HTML
REF: https://stackoverflow.com/questions/14675913/changing-image-size-in-markdown
 -->
<img src="/img/panels.JPG" width="600" alt="a photo of the project" />

### HTML DOM querySelectorAll() Method

Here we get all elements in the document with class="panel"

The querySelectorAll() method returns all elements in the document that matches a specified CSS selector(s), as a static NodeList object.

The NodeList object represents a collection of nodes. The nodes can be accessed by index numbers. The index starts at 0.

#### You can loop through a node list just like with an array. 
You can target specific panels, we will loop through nodelist using forEach()

we now have access to all the panels by passing in a panel for each iteration.

The forEach() method calls a function once for each element in an array, in order.
```js
// loops through and shows each panel
panels.forEach(panel) => {
  console.log(panel)
})
```
## what do we want to do with these panels?

### The addEventListener() method
Common Example: Add an event listener that fires when a user clicks a button:  
```js
// add an event listener on each panel and listen for a click, when clicked we'll run a function
panels.forEach(panel) => {
  panel.addEventListener('click', () => {

  })
})
```
This property is useful to add, remove and toggle CSS classes on an element.

The classList property is read-only, however, you can modify it by using the add() and remove() methods.

```js
// add class of active to panel clicked on
panels.forEach(panel) => {
  panel.addEventListener('click', () => {
    panel.classList.add('active')
  })
})
```
But then all clicked on will be active. 

```js
// add class of active to panel clicked on
panels.forEach(panel) => {
  panel.addEventListener('click', () => {
    removeActiveClasses();
    panel.classList.add('active')
  })
})
```
this isn't a built in feature we'll write the function.   We need to run another function to remove the active class on all other panels.

```js
function removeActiveClasses() {
  panels.forEach((panel) => {
    panel.classList.remove('active');
  });
}
```