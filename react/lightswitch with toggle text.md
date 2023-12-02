
```JavaScript
import { useState } from "react";

  

export const Room = () => {

  const [lighting, setLight] = useState("lit");

  const [isRoomLit, setIsRoomLit] = useState(true);

  const handleLightState = () => {

    setLight(lighting !== "lit" ? "lit" : "dark");

  };

  const handleRoomText = () => {

    setIsRoomLit(!isRoomLit);

  };

  return (

    <>

      <div className={lighting}>

        {isRoomLit ? "The room is lit" : "the room is dark"}

      </div>

      <button

        onClick={() => {

          handleLightState();

          handleRoomText();

        }}

      >

        Lichtschalter

      </button>

    </>

  );

};
```

Timos Version:

```JavaScript
import { useState } from "react";

export const Room = () => {
  const [isRoomLit, setIsRoomLit] = useState(true);

  const handleLightState = () => {
    setIsRoomLit(!isRoomLit);
  };

  const roomStatus = isRoomLit ? "The room is lit" : "The room is dark";

  return (
    <>
      <div className={isRoomLit ? "lit" : "dark"}>
        {roomStatus}
      </div>
      <button onClick={handleLightState}>
        Lichtschalter
      </button>
    </>
  );
};
```

with previous state:

```JavaScript
import { useState } from "react";

  

export const Room = () => {

  const [lighting, setLight] = useState("lit");

  const [isRoomLit, setIsRoomLit] = useState(true);

  const handleLightState = () => {

    setLight((prevLighting) => (prevLighting === "lit" ? "dark" : "lit"));

    setIsRoomLit((prevIsRoomLit) => !prevIsRoomLit);

    console.log(lighting, isRoomLit);

  };

  return (

    <>

      <div className={lighting}>

        {isRoomLit ? "The room is lit" : "the room is dark"}

      </div>

      <button

        onClick={() => {

          handleLightState();

        }}

      >

        Lichtschalter

      </button>

    </>

  );

};
```