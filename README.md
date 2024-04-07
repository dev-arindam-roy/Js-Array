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
> **Find users who have age of greater than 25**
```js
/* Type 1 */
let findAgeArr = ageArr.filter((age) => (age > 25) ? age : null);
console.log(findAgeArr);

/* Type 2 */
let findAgeArr = ageArr.filter((age) => {
  return (age > 25) ? age : null;
});
console.log(findAgeArr);
```
> **Array Find - First, FirstIndex, Last, LastIndex**
```js
let ageArr = [12, 13, 14, 16, 22, 32, 61, 65, 70, 90];

let findFirstAge = ageArr.find((age) => (age > 25) ? age : null );
console.log(findFirstAge);

let findFirstAgeIndex = ageArr.findIndex((age) => (age > 25) ? age : null );
console.log(findFirstAgeIndex);

let findLastAge = ageArr.findLast((age) => (age > 25) ? age : null );
console.log(findLastAge);

let findLastAgeIndex = ageArr.findLastIndex((age) => (age > 25) ? age : null );
console.log(findLastAgeIndex);
```
> **Arrays within an array => single unique Array**
```js
let arrx = [[1,2],[2,3],[2,6]];
let oneArr = arrx.flat();
console.log(oneArr); //[1, 2, 2, 3, 2, 6]
let uniqueOneArr = [...new Set(oneArr)];
console.log(uniqueOneArr); //[1, 2, 3, 6]
```
> **Check IsArray**
```js
let arr = ["php", "asp", "jsp", "react", "node", "laravel", "firebase"];
let ageArr = [12, 13, 14, 16, 22, 32, 61, 65, 70, 90];

let obj = {
  name: "Arindam",
  skill: "Developer",
  exp: 14
}

console.log(Array.isArray(ageArr)); //true
console.log(Array.isArray(arr)); //true
console.log(Array.isArray(obj)); //false
```
> **Array Join into String**
```js
let arr = ["php", "asp", "jsp", "react", "node", "laravel", "firebase"];

let joinStringFormat1 = arr.join(',');
let joinStringFormat2 = arr.join('/');
let joinStringFormat3 = arr.join('-');

console.log(joinStringFormat1, joinStringFormat2, joinStringFormat3);
```
> **Array LastIndexOf**
```js
let arr = ["php", "asp", "jsp", "react", "node", "laravel", "firebase"];
let arr2 = ["android", "electron", "nest", "jsp", "react", "node", "mongodb"];
let arr3 = ["mysql", "postgresql", "firebase", "redis"]

let concatArrs = arr.concat(arr2,arr3);
console.log(concatArrs);
/*
["php", "asp", "jsp", "react", "node", "laravel", "firebase", "android", "electron", "nest", "jsp", "react", "node", "mongodb", "mysql", "postgresql", "firebase", "redis"]
*/
console.log(concatArrs.lastIndexOf('react')); //11
```
