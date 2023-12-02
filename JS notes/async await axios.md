await axios: 

````JavaScript
const response = await axios.get(url);
````

I will need an IIFE when the axios is in a function block

````JavaScript
(async () => {

});
````

you can put your data fetching code into a function block to call it later

````JavaScript
const fetchingData = async () => {

};
````

you can't use await or async in template literals:

In JavaScript, the `await` keyword is used to pause the execution of an asynchronous function until a promise is resolved. Template literals, on the other hand, are a way to concatenate strings in a more flexible and readable manner using backticks (`).

The reason why you can't use `await` directly inside template literals is that template literals are evaluated at the time they are created, and `await` can only be used inside an asynchronous function or an async IIFE