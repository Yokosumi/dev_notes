
you can write a function to use on different events when they do mostly the same with minor differences

```JavaScript
// querySelectors
const addOpacityButton =

            document.querySelector<HTMLButtonElement>(".opacity_up");

        const decreaseOpacityButton =

            document.querySelector<HTMLButtonElement>(".opacity_down");

        const paragraph =

            document.querySelector<HTMLParagraphElement>("div.solution p");

  
// currentValue
        let currentOpacity = 0.1;
// increment 
        const changeOpacity = (increment: number) => {

            currentOpacity += increment;

            if (paragraph !== null) {

                paragraph.style.opacity = String(currentOpacity);

            }

        };

  
// decrement
        addOpacityButton?.addEventListener("click", (event) => {

            event.preventDefault();

            changeOpacity(0.1);

        });

        decreaseOpacityButton?.addEventListener("click", (event) => {

            event.preventDefault();

            changeOpacity(-0.1);

        });

    });
```