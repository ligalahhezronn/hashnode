---
title: "Master JavaScript Events & Event Delegation"
datePublished: Sat Apr 06 2024 11:54:21 GMT+0000 (Coordinated Universal Time)
cuid: cluo1eiju000208lb8nxo3z0a
slug: master-javascript-events-event-delegation
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1712402548680/81d66fed-997c-43d4-93ae-27189b0fb8b8.jpeg

---

### **Understanding JavaScript Events:**

### What are JavaScript Events?

Events are actions that happen in the system you are programming. Events can be user actions like clicks, mouse movements, key presses, or system occurrences like a webpage finishing loading.

### Listening for events

Introduce the `addEventListener()` method which we use to listen to events on elements.

Example:

```javascript
document.querySelector('button').addEventListener('click', function() {
  alert('Button clicked!');
});
```

### Event types

1. click
    
2. mouseover
    
3. mouseout
    
4. keydown
    
5. load
    

### Diving deeper: Event object

When event occurs, the event listener receives an event object as its first argument, which contains details about the event.

## Preventing default event behavior

Sometimes, you want to prevent the browser's default event action. Introduce `event.preventDefault()`. For example, if you want to prevent a form from submitting:

```javascript
document.querySelector('form').addEventListener('submit', function(event) {
  event.preventDefault();
  // Additional code to manually handle the form submission
});
```

# **Mastering Event Delegation:**

### The problem with direct event handlers

Inefficiency of adding an event listener to each element, especially with a large number of elements. Performance issues and the challenge of dynamically added elements.

### What is event delegation?

Event delegation is the technique that leverages event bubbling. Instead of adding event listener to each individual element, you add a single event listener to a parent element that will catch all events of a specified type from its children.

### Advantages of event delegation

1. Performance: reduces the number of event listeners needed.
    
2. Dynamically Added Elements: Automatically handles events from elements added in the future.
    

```javascript
document.querySelector('#parent').addEventListener('click', function(event) {
  if (event.target.matches('button.child')) {
    alert('Child button clicked!');
  }
});
```

# **Practical Example: A Todo List**

Clicking on a todo item toggles its completed state. Use event delegation to handle clicks on dynamically added todo items.

```javascript
document.querySelector('#todo-list').addEventListener('click', function(event) {
  if (event.target.matches('.todo-item')) {
    event.target.classList.toggle('completed');
  }
});
```