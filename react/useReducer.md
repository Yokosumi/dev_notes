
## useReducer boilerplate (counter)


```JavaScript
interface IState {

    count: number;

}

  

const initialState: IState = {

    count: 0,

};

  

interface IAction {

    type: "increment" | "decrement";

    payload: number;

}

  

const reducer = (state: IState, action: IAction) => {

    const _state = structuredClone(state);

    switch (action.type) {

        case "increment":

            _state.count += action.payload;

            break;

        case "decrement":

            _state.count -= action.payload;

            break;

    }

    return _state;

};
```
