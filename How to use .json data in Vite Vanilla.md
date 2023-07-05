

## Setting up .json file

- create `data` folder within the `src` folder
- create .json file `[name].json`
-  write structure
	- e.g ```
```
[

  {

    "dish": "Plantain Chips, Guacamole (V, VE)",

    "price": 9

  },

  {

    "dish": "Jalapeño Crisps (V, VE)",

    "price": 6

  }
]
```


## import .json file

like this:
 ```javascript
 import menuTable from "../data/[filename].json";

```
 

## usage

access the file through parameters of a function or callbackfunction

e.g
```JavaScript
 ${menuTable

     .map((menuItem) => {

       return /*html*/ `

        <tr>

        <td> ${menuItem.dish}</td>

        <td class="price"> ${menuItem.price}</td>

    </tr>

    `;
```

