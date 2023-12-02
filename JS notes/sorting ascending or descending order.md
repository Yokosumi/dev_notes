
sorts the array items in ascending order in the same array  
  
```JavaScript
array.sort( (a, b) => a > b ? -1 : 1)
```

sorts the array items in decending order in the same array  
  
```JavaScript
array.sort( (a, b) => a > b ? 1 : -1)
```

 what happens:
 
```JavaScript
-1 => a, b  
 1 => b, a  
```
