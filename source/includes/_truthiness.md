# Truthiness
A truthy value is a value that translates to true when evaluated in a Boolean context. All values are truthy unless they are defined as falsy (i.e., except for false, 0, "", null, undefined, and NaN).
 

```javascript
if (true) {
    console.log('we will get here');
}
if ({}) {
    console.log('we will get here');
}
 
 
if (-42) {
    console.log('we will get here');
}
 
 
if (-Infinity) {
    console.log('we will get here');
}

 
// undefined
```
## Falsiness
Using Boolean with the value of true or false, a falsyness will always be evaluated to false


```javascript
if (false) {
    console.log('we will not get here');
}

if (null){
    console.log('we will not get here');
}

if (undefined){
    console.log('we will not get here');
}

if (0){
    console.log('we will not get here');
}
 