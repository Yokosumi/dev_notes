
if you don't have an element saved in a variable you can use event.target to define which element will be affected by the eventlistener

```JavaScript

document.addEventListener('mousedown', (event) => {
 const element = event.target;
 //function
});
```

