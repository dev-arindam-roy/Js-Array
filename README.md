# Javascript Array Functions with Examples
All require functions with example for your quick development

```js
let arr = ["php", "asp", "jsp", "react", "node", "laravel", "firebase"];

let arr2 = ["android", "electron", "nest", "jsp", "react", "node", "mongodb"];

let arr3 = ["mysql", "postgresql", "firebase", "redis"]

console.log(arr); //["php", "asp", "jsp", "react", "node", "laravel"]
console.log(arr.length); //6
console.log(typeof arr); //"object"
console.log((arr[2]) ? 'Yes have value' : null); //"Yes have value"
console.log(arr[10]); //undefined
console.log(typeof arr[10]); //"undefined"
console.log(typeof arr[10] == "undefined"); //true
console.log(typeof arr[10] === "undefined"); //true
console.log(typeof arr[10] == undefined); //false
console.log(typeof arr[10] === undefined); //false

console.log(arr[0]); //get first item => "php"
console.log(arr[arr.length - 1]); //get last item => "laravel"
 
console.log(arr.includes("nextjs")); //false
console.log(arr.includes("react")); //true

console.log(arr.indexOf("nextjs")); //-1 (-1 or <= 0 means not found into the array)
console.log(arr.indexOf("react")); //3

console.log(arr.at()); //get first item => "php"
console.log(arr.at(-1)); //get last item => "laravel"

let newArr1 = arr.concat(arr2); //merge arrays
console.log(newArr1); 

let newArr2 = arr.concat(arr2, arr3); //merge multiple arrays
console.log(newArr2);

let arr2Keys = newArr2.keys(); //get keys of the array into a new array
console.log(arr2Keys); //[object Array Iterator]
arr2Keys.forEach((v) => console.log(v));

let arr2Values = newArr2.values(); //get values of the array into a new array
console.log(newArr2.values());  //[object Array Iterator]
arr2Values.forEach((v) => console.log(v));

let arr2Entries = newArr2.entries(); //get key, values of the array into a new array
console.log(arr2Entries); //[object Array Iterator]
arr2Entries.forEach((v) => console.log(v));
arr2Entries.forEach((v) => {
 console.log(`Index:${v.at()} => ${v.at(-1)}`);
});
```
