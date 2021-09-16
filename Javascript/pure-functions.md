# Pure Function

### Definition
- The function always return the same result if the same arguments are passed in. It does not depends on any state or data, change during the program execution. It must only depends on its input arguments.
- The function does not produce any observable side effects such as network requests, input and output devices,or data mutation.
  
```js
let num = Math.floor(Math.random()*100)

const f1 = () => {
    return x + num
}
console.log(f1(5))
```
Here the result will be change when refresh the screen each tim
```So this is not a pure function```

```js
const f2 = (x,y) => {
    return x + y
}
console.log(5,10)
```
When the code run many time the result will be same. so we say the its a ```Pure Function```