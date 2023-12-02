## Info

If you want to give an flex item fixed space use `flex-1` on the flex item 

---
## Image


![[quote_card_tlw.jpg]]

---

## Code

```JavaScript
<div class="flex h-screen items-center justify-center">

  <div class="m-4 flex min-h-[15rem] min-w-[30rem] max-w-sm flex-col items-center rounded-lg border border-gray-200 bg-white p-6 shadow dark:border-gray-700 dark:bg-gray-800">

    <h2 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"></h2>

    <p class="max-h-[10rem] flex-1 overflow-hidden font-normal text-gray-700 dark:text-gray-400">

      Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto odio voluptatem dicta quasi cupiditate et earum voluptas quae, error cumque minus facilis repellat debitis ducimus ipsum quam veniam perferendis repudiandae.

      <span class="italic">Some name</span>

    </p>

    <button class="mx-4 my-4 h-12 max-w-xs rounded bg-blue-500 px-4 py-2 font-bold text-white hover:bg-blue-700">New Quote</button>

  </div>

</div>
```

---