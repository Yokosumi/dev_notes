
Der `useRef` Hook in React ermöglicht es dir, Referenzen auf DOM-Elemente oder andere Werte zu erstellen und diese über Rendervorgänge hinweg zu speichern. Im Gegensatz zu State-Variablen, die bei jedem Rendern aktualisiert werden und eine Re-Rendern auslösen können, behält `useRef` den Wert bei und löst kein Re-Rendern aus.

eine useRef Referenz erstellen:

```JavaScript
const myRef = useRef(initialValue);
```

  
Verwendung der Ref-Referenz in JSX: Du kannst die Ref-Referenz verwenden, um sie einem DOM-Element oder einem React-Komponentenattribut zuzuweisen. Zum Beispiel:

```JavaScript
  return <input ref={myRef} />;
```

  
Zugriff auf den Wert der Ref-Referenz: Du kannst auf den aktuellen Wert der Ref-Referenz über myRef.current zugreifen und verändern. Die werte sind Veränderbar.

```JavaScript
console.log(myRef.current);
```

Man kann Ref-Referenzen aktualisieren im Gegensatz zu State-Variable und sie lösen kein Re-render aus.

  
Der `useRef` Hook ist besonders nützlich, wenn du auf DOM-Elemente zugreifen oder bestimmte Werte über Rendervorgänge hinweg speichern möchtest, ohne ein Re-Rendern auszulösen.