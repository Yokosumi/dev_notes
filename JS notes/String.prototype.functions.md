
split example:

the split method removes the given value (5) from each string in the array 

```JavaScript
const array = ["You5Tube", "Face5Book", "Net5Flix"];

const removedNumber = array.map((string) => string.split("5").join(""));
```