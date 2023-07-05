
### index.css

```CSS
@tailwind base;

@tailwind components;

@tailwind utilities;
```

tailwind.config.js

```JavaScript
/** @type {import('tailwindcss').Config} */

export default {

  content: ["./index.html", "./**.{js,*}"],

  theme: {

    extend: {},

  },

  plugins: [],

};
```

