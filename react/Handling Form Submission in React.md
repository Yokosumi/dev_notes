
# Handling Form Submission in React

## Introduction

In this article, we will discuss how to handle form submission in React. We will explore a code example that demonstrates the process of capturing form data and logging it to the console.

## Key Concepts

Before diving into the code example, let's briefly cover some key concepts related to form submission in React:

1. **Form Submission**: When a user fills out a form and clicks the submit button, the form data needs to be processed. In React, we can handle form submission using event handlers.
    
2. **Event Handling**: React provides a synthetic event system that wraps native browser events. We can attach event handlers to specific elements in our React components to respond to user interactions.
    
3. **Preventing Default Behavior**: By default, when a form is submitted, the browser will refresh the page. In React, we can prevent this default behavior using the `preventDefault()` method.
    
4. **Form Data**: The data entered by the user in the form fields needs to be captured and processed. In React, we can access the form data using the `FormData` API.
    

## Code Structure

The code provided demonstrates a function called `handleFormSubmit` that handles the form submission event. Let's break down the code and understand each step:

language-javascript



```JavaScript
const handleFormSubmit = (event: FormEvent<HTMLFormElement>) => {

        event.preventDefault();

        const formData = new FormData(event.target as HTMLFormElement);

        const employee = JSON.stringify(Object.fromEntries(formData));

        console.log(employee);

    };
```

1. The `handleFormSubmit` function takes an event object as a parameter, which represents the form submission event.
    
2. The `event.preventDefault()` method is called to prevent the default behavior of form submission, which is to refresh the page.
    
3. The `FormData` API is used to create a new instance of the `FormData` object. This object captures the form data entered by the user.
    
4. The `Object.fromEntries()` method is used to convert the form data into a plain object. This step allows us to access the form data in a more convenient format.
    
5. The `JSON.stringify()` method is called to convert the form data object into a JSON string.
    
6. Finally, the `console.log()` function is used to log the JSON string representation of the form data to the console.
    

## Code Examples

Let's consider an example where we have a form with two input fields: `name` and `email`. When the user submits the form, the `handleFormSubmit` function will be triggered, capturing the form data and logging it to the console.

language-jsx

 Copy code

``` JavaScript
import React, { FormEvent } from 'react';

const MyForm = () => {
    const handleFormSubmit = (event: FormEvent<HTMLFormElement>) => {
        event.preventDefault();
        const formData = new FormData(event.target as HTMLFormElement);
        const employee = JSON.stringify(Object.fromEntries(formData));
        console.log(employee);
    };

    return (
        <form onSubmit={handleFormSubmit}>
            <label htmlFor="name">Name:</label>
            <input type="text" id="name" name="name" />

            <label htmlFor="email">Email:</label>
            <input type="email" id="email" name="email" />

            <button type="submit">Submit</button>
        </form>
    );
};

export default MyForm;

```

In the above example, we define a functional component called `MyForm`. Inside this component, we render a form with two input fields (`name` and `email`) and a submit button. The `onSubmit` event handler is set to the `handleFormSubmit` function.

## Conclusion

Handling form submission in React involves capturing the form data and performing any necessary processing. By using event handlers and the `FormData` API, we can easily handle form submissions in a React application. The provided code example demonstrates how to prevent the default behavior of form submission, capture the form data, and log it to the console. Feel free to modify and adapt this code to suit your specific needs. Happy coding!