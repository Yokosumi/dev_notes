
this code iterates throuhgh an array to pass each value to the log of attributes of wanted values

```JavaScript

const array = ["href", "hreflang", "rel", "target", "type"];

      function getAttributes() {

        array.forEach((val) => {

          console.log(element.attributes[val]);

        });

      }

  

      btn.addEventListener("click", () => {

        getAttributes();

      });

```