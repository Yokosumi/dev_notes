
  
Man brauch eine id um den Label mit dem input zu verbinden, in react muss die id auch im `htmlFor` attribute stehen

```JavaScript
<label htmlFor="exampleId">
</label>
<input id="exampleId"/>

```

form data beispiel:

``event.preventDefault();`` verhindert dass der Standard-Event ausgeführt wird damit wir unsere eigene Logik implementieren können

FormData packt die Geschickten Daten in ein FormData Object e.g:

FormData Vorteil: Wir müssen keine State Variablen verwalten.

![[Pasted image 20231113103259.png]]

event.target ist in diesem Form ein Button und von dem werden die Daten genommen und in ein FormData Object übergeben




```TypeScript

    const handleFormSubmit = (event: FormEvent<HTMLFormElement>) => {

        event.preventDefault();

        const data = new FormData(event.target as HTMLFormElement);

        console.log(data);

    };
```

