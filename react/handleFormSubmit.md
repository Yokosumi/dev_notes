

-this handle function gets the input over formData with event.target

-event.target is the form button that submits the values of the input fields

-because the standard submit is disabled due to `event.preventDefault()` the button saves the 
data to our formData variable instead in form of a formData-object

-after that we turn the formData object into json format, so we can send it to our backend


```JavaScript
    const handleFormSubmit = (event: FormEvent<HTMLFormElement>) => {

        event.preventDefault();

        const formData = new FormData(event.target as HTMLFormElement);

        const employee = JSON.stringify(Object.fromEntries(formData));


    };

```

