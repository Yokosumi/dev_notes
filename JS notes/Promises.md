

### Declaration

You can declare a promise like this:

```JS
const promise = new Promise(() => {})

```

---
### PromiseStatus


The value of the `PromiseStatus`, the **state**, can be one of three values:

- ✅ <span style="color:#00b050; font-weight: bold"> Fulfilled </span> : The promise has been `resolved`. Everything went fine, no errors occurred within the promise 🥳
- ❌ <span style="color:#ff0000 ; font-weight: bold">Rejected</span> : The promise has been `rejected`. Argh, something went wrong..
- ⏳ <span style="color:#ffc000 ; font-weight: bold">Pending</span> : The promise has neither resolved nor rejected (yet), the promise is still `pending`.