# Immutability

### Mutation in Array
```js
let num = [1,2,3,4]
num.push(5)
console.log(num)

```
Here the output will be 1,2,3,4,5
Here the ***num.push*** method mutates the num variable

### Mutation in Object
```js
let fruit = { name: "apple", color: "green"}
fruit.color = "red"
console.log(fruit)

```
Here the output will be { name: "apple", color: "red"} 
Here the fruit.color mutates the value of color 

### Immutability in Array
```js
let num = [1,2,3,4]
let newNum = [...num,5]
console.log(num)
console.log(newNum)

```
Here ***num*** is immuttable
and the second array mutated the first array.

### Immutability in Objects
```js
let fruit = { name: "apple", color: "green"}
newFruit = {...,color:"red"}
console.log(fruit)
console.log(newFruit)
```
Here ***fruit*** is immuttable
and the second array mutated the first array.
