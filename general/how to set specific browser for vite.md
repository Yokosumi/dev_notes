
first install the following so you can use `process` 

write this line into your terminal:

```JS
 npm i --save-dev @types/node
```

---


after that set the environment variable in the <span style="color:#00b0f0">vite.config.ts</span> or <span style="color:#ffc000">vite.config.js</span> file:

```TypeScript
process.env.BROWSER = "your browser" // (e.g: firefox, chrome)
```

--- 

lastly create the `.env.developement` on the root directory of your project (where also your vite.config file lies)

and set the `VITE_BROWSER` variable:

```JS
VITE_BROWSER=firefox
```

you can change the value to the wanted server. (note: the browser needs to be installed on your system)


---

You can now add `--open` parameter in <span style="color:#ffff00">package.json</span> or set open in your vite.config file like this:

```JS
export default defineConfig({
    server: {
        open: true,
    }
})
```

