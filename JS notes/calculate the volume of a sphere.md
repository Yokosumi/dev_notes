
```JavaScript
<body>

    <p>Input radius value and get the volume of a sphere.</p>

    <form id="MyForm">

      <label for="radius">Radius</label>

      <input type="text" name="radius" id="radius" required />

      <button>Calculate volume</button>

    </form>

  

    <script>

      const form = document.querySelector("#MyForm");

      const btn = document.querySelector("button");

      function calcVolume() {

        const userInput = document.querySelector("#radius").value;

        const volumne = (4 / 3) * Math.PI * Math.pow(Number(userInput), 3);

        alert("The volumne of the sphere equals: " + volumne.toFixed(2));

      }

  

      btn.addEventListener("click", (event) => {

        event.preventDefault();

        calcVolume();

      });

    </script>
```