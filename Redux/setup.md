# Redux Toolkit
```js
npm i @reduxjs/toolkit react-redux
```

### First Step

Create a Redux store in ./src folder ```./src/Redux/store.js```

./store.js
```js
import {configureStore} from '@reduxjs/toolkit'
export default configureStore({
    reducer: {}
})

```
./index.js
```js
import store from './Redux/store.js'
import {Provider} from 'react-redux'

<Provider store={store}>
<App /> 
</Provider>
```

### Create First State
Create a folder ```./color``` and create a file ```colorSlice.js```
```js
import {createSlice} from '@reduxjs/toolkit'

export const colorSlice = createSlice({
    name: "color",
    initialvalue: {
        value : "blue"
    },
    reducers: {
        change_color: (state,action) => {
            state.value = action.payload.color
        }
    }
})

export const {change_color} = colorSlice.actions
export default colorSlice.reducer
```

### Adding the color Reducer to Root Reducer in the Store

./Store.js
```js
import {configureStore} from '@reduxjs/toolkit'
import colorReducer from './color'
export default configureStore({
    reducer: {
        color:colorReducer
    }
})
```

### using the state in the component
```js
import {useSelector, useDispatch} from 'react-redux'
import {change_color} from 'filepath'
/////

const color = useSelector(state => state.color.value)
const dispatch = useDispatch()

const changecolor = () => {
    dispatch(change_color({
        color: "red"
    }))
}

```

