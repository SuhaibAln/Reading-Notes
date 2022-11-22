# Redux Toolkit

- Redux Toolkit is the official, opinionated, batteries-included toolset for efficient Redux development. It is intended to be the standard way to write Redux logic, package that contains the most commonly used Redux packages, plus some utilities to make them work better together.

# What is createSlice in Redux Toolkit?

- createSlice is a function that accepts an initial state, an object full of reducer functions, and a "slice name", and automatically generates action creators and action types that correspond to the reducers and state.

# a small application to add a location name to the existing list dynamically using redux toolkit

- [Source](https://medium.com/geekculture/understanding-createslice-in-redux-toolkit-reactjs-eca8d20f45d7)

from the terminal run `npx create-react-app my-app --template redux`

- First, import the createSlice method from the redux-toolkit library.
  Make use of createSlice method to create your slice.
  The locationSlice created above contains all the values required to create a reducer. Now we need to export the actions and the reducer.

```
import { createSlice } from '@reduxjs/toolkit';
const locationSlice = createSlice({
    name: "location",
    initialState: {
        location: ['Bangalore', 'Hyderabad', 'Delhi'],
    },
    reducers: {
        save: (state, param) => {
            const { payload } = param;
            state.location = [...state.location, payload];
        },
    }
});
const { actions, reducer } = locationSlice
export const { save } = actions;
export default reducer;

```

## Step 2: Dispatch action by making use of react hooks in functional component.

- Now we need to make use of the react hooks useSelector to read the state and useDispatch to dispatch the action created in slice. Let’s implement and see how the app works.

```
import React, { useState } from "react";
import { save } from "./locationSlice";
import { useDispatch, useSelector } from "react-redux";
import { Box, TextField, Button } from "@material-ui/core";

export default function App() {
    const [locationName, setLocationName] = useState('');
    const dispatch = useDispatch();
    const { location } = useSelector(state=>state)
    const handleData = (e) => {
        setLocationName(e.target.value);
    }
    const handleSave = () => {
        const ifPrestent = location.includes(locationName);
        if(locationName !== undefined && !ifPrestent) {
            dispatch(save(locationName));
            setLocationName('')
        } else {
            setLocationName('')
        }
    }
    return (
        <Box>
            <Box>
                <TextField
                    onChange={handleData}
                    value={locationName}
                    label="Enter location name"
                />
                <Button
                    style={{margin: '10px'}}
                    variant="contained"
                    color="primary"
                    onClick={handleSave}
                >
                    add
                </Button>
            </Box>
            <Box>
                <h3> List of locations </h3>
            </Box>
            <Box>
                 {location.map((item) => <li>{item}</li>) }
            </Box>
        </Box>
    );
}
```

## Step 3: Configure the store

- Now we need to connect our store to the app. Here configureStore({}) wraps createStore() to simplify the configuration for us. createStore() is a redux store that holds the complete state tree of your app.

```

import React from "react";
import ReactDOM from "react-dom";
import App from "./App";
import { configureStore } from "@reduxjs/toolkit";
import { Provider } from "react-redux";
import rootReducer from "./locationSlice";
const store = configureStore({
    reducer: rootReducer
});
ReactDOM.render(
    <Provider store={store}>
        <App />
    </Provider>,
    document.getElementById('root')
);
```
