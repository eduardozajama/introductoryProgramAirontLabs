# 30. Events. Event Bubbling
What are Events?
The Events in JavaScript are a change in the state of an object. There are a bunch of events where some activity is performed by the user or browser. When the JavaScript code is included in the HTML, JavaScript will react to the events. This process of reacting to events is known as Event handling.

## Event bubbling
The Event bubbling in JavaScript is a type of event propagation. The event triggers the innermost target element and consecutively triggers the parent element of the target element in the same hierarchy until it triggers the outermost element.

It is a procedure where it starts from the element that triggered the event and then bubbles up to the ancestor elements in the hierarchy.

Let’s get a clear understanding of the flow of event bubbling, where the flow goes from the target element to the outermost element.
## Example of Event Bubbling
Let's look at the below example to understand the working concept of Event Bubbling:
```html
<!DOCTYPE html>  
<html>  
<head>  
  <meta charset="utf-8">  
  <meta name="viewport" content="width=device-width">  
  <title>Event Bubbling</title>  
</head>  
<body>  
  <div id="p1">  
    <button id="c1">I am child button</button>  
  </div>  
    
  <script>  
    var parent = document.querySelector('#p1');  
      parent.addEventListener('click', function(){  
        console.log("Parent is invoked");  
      });  
  
   var child = document.querySelector('#c1');  
      child.addEventListener('click', function(){  
        console.log("Child is invoked");  
      });  
  </script>  
</body>  
</html> 
```
![](/studyMaterial/30-events/event-bubbling-and-capturing-in-javascript.png)
## Explanation of Code:

The above code is a HTML and JavaScript based code.
We have used a div tag having div id = p1 and within div we have nested a button having button id = c1.
Now, within the JavaScript section, we have assigned the html elements (p1 and c1) using the querySelector () function to the variable parent and child.
After that, we have created and included an event which is the click event to both div element and child button. Also created two functions that will help us to know the sequence order of the execution of the parent and child. It means if the child event is invoked first, "child is invoked" will be printed otherwise "parent is invoked" will get printed.
Thus, when the button is clicked, it will first print "child is invoked" which means that the function within the child event handler executes first. Then it moves to the invocation of the div parent function.
The sequence has taken place due to the concept of event bubbling. Thus, in this way event bubbling takes place.

We can also understand the flow of event with the help of the below flow chart:
![](/studyMaterial/30-events/event-bubbling-and-capturing-in-javascript2.png)


It means when the user clicks on the button, the click event flows in this order from bottom to top.

## How to Handle Events that Bubble
The "Event Bubbling" behavior makes it possible for you to handle an event in a parent element instead of the actual element that received the event.

The pattern of handling an event on an ancestor element is called Event Delegation.

## How to Stop Event Bubbling
Event Bubbling is a default behavior for events. But in some cases, you might want to prevent this.

Let's say, for example, from our HTML code, that you want the div to open a modal when it is clicked. For the button, on the other hand, you want it to make an API request when it is clicked.

In this case, you may not want the modal to open when you click the button. You might want the modal to only open when you actually click it (and not when you click any of its children). This is where preventing event propagation comes in.

To prevent event bubbling, you use the stopPropagation method of the event object.

When handling events, an event object is passed to the handling function:

button.addEventListener("click", (event) => {
  // do anything with the event object
}
The event object contains properties that have information about the event that was triggered and the element it was triggered on. This object also contains methods – one of which is stopPropagation().

The stopPropagation method of an event prevents the event from propagating to the parents and ancestors of the element the event was triggered on.

## Resources

https://www.freecodecamp.org/news/event-bubbling-in-javascript/#:~:text=What%20is%20Event%20Bubbling%3F,gets%20to%20the%20root%20element.
https://www.geeksforgeeks.org/event-bubbling-in-javascript/
https://www.javatpoint.com/event-bubbling-and-capturing-in-javascript
https://www.tutorialspoint.com/what-is-event-bubbling-in-javascript

