
difference between <span style="color:#0070c0">axios</span> and <span style="color:#ffc000">fetch</span>:

- <span style="color:#0070c0">axios</span> waits only once
  
- <span style="color:#ffc000">fetch</span> waits twice
  
- <span style="color:#ffc000">fetch</span> is available in any modern browser since 2016
  
- <span style="color:#0070c0">axios</span> is not a <span style="color:#c00000">devDependency</span> 
  
- <span style="color:#0070c0">axios</span> must be imported like so:
	- `import axios from 'axios';`
  
  
- <span style="color:#0070c0">axios</span> must be installed with:
	- `npm -i axios`


1. **<span style="color:#c00000">Synchronous Data Fetching</span>:**
    
    - In <span style="color:#c00000">synchronous data fetching</span>, the program waits for the data to be retrieved **before** moving on to the next line of code.
      
    - During the data fetching process, the entire program execution is **blocked**, and it won't proceed to other tasks until the data is received.
      
    - <span style="color:#c00000">Synchronous operations</span> are straightforward but can lead to **performance issues**, especially in scenarios where there is a **delay** in data retrieval.
    

    this execution blocks until data is fetched
    
```JavaScript 
const data = fetchDataSynchronously();
```

    
2. **<span style="color:#00b050">Asynchronous Data Fetching</span>:**
    
    - In <span style="color:#00b050">asynchronous data fetching</span>, the program initiates the data retrieval process and **continues** with other tasks without waiting for the data to be available.
    - <span style="color:#92d050">Callbacks</span>, <span style="color:#ffff00">Promises</span>, or <span style="color:#00b050">async</span>/<span style="color:#7030a0">await</span> mechanisms are often used in <span style="color:#00b050">asynchronous </span><span style="color:#00b050">programming</span> to handle **the response** or **perform actions** after the data is retrieved.
    - <span style="color:#00b050">Asynchronous operations</span> are more common in web development, where waiting for network requests or file I/O could lead to **significant delays**.
    
    
```JavaScript
async function fetchData() {
  try {
    const data = await fetchDataAsynchronously();
    console.log(data); // This line is reached when data is available
  } catch (error) {
    console.error(error);
  }
}

fetchData();

```

<span style="color:#00b050">Asynchronous data</span> <span style="color:#00b050">fetching</span> is **preferred** in scenarios where you want to avoid *blocking* the execution of other tasks, especially in environments like **web browsers** where responsiveness is crucial. It allows the program to continue working on other tasks while waiting for the data to be retrieved, improving overall **efficiency** and **user experience**.
