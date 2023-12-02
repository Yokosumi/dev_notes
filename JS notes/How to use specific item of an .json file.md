

first import the .json file into the space where you want to use it

```JavaScript
import images from "../data/images.json";
```

then save  the wanted item in a variable with the fill() method

```JavaScript
 const imageFoodRoll = images.find((imageItem) => imageItem.name === "food rolls");
```

call the variable like this
```JavaScript
`<img src="${imageFoodRoll?.url}" alt="${imageFoodRoll?.alt}">`
```
