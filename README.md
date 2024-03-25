# Complete Javascript Bootcamp 😀💥💫
This is complete bootcamp to learn javascript from basic to intermediate level after doing this i am sure every one can solve medium question of DSA using these topics discussed. It is designed to revise all the important concepts of Javascript that is used frequently.If you think this repo helped you make sure to star the repo 🤗.
 ## Data Types
 1. Primitive: 
     --Number (+- 2^53-1)
     --BigInt 
     --Nan
     --Boolean (true,false)
     --Undefined
     --String
     --Symbol
 
  2. Non Primitive:
     --Object
     --Array
   
 
   ## String methods 
 1. length   ->  length of string
 2. indexOf() -> index of char
 3. lastIndexOf() -> last index of char
 4. slice(start,end) -> returns string with index from start to end
 5. splice() -> to remove/add element from segment of string
 6. split() -> returns string according to separator
 7. substring(start,end) -> replace substring from index start to end
 8. replace(target,replacement) -> replace target with replacement
 9. trim() -> removes extra spaces from start and end
 10. toLowerCase()/toUpperCase() -> converts uppercase/lowercase
 11. charAt() ->return char at index i
 12. at(index) -> return char at index i
 13. concat(operator,string) -> to merge to strings
 14. repeat(times) -> how many times to repeat string
---
Code:
```
const clothing = ['shoes', 'shirts', 'socks', 'sweaters'];

console.log(clothing.length);
// Expected output: 4
```
```
const beasts = ['ant', 'bison', 'camel', 'duck', 'bison'];

console.log(beasts.indexOf('bison'));
// Expected output: 1

// Start from index 2
console.log(beasts.indexOf('bison', 2));
// Expected output: 4

console.log(beasts.indexOf('giraffe'));
// Expected output: -1

```
```
const animals = ['Dodo', 'Tiger', 'Penguin', 'Dodo'];

console.log(animals.lastIndexOf('Dodo'));
// Expected output: 3

console.log(animals.lastIndexOf('Tiger'));
// Expected output: 1
```
```const animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];

console.log(animals.slice(2));
// Expected output: Array ["camel", "duck", "elephant"]

console.log(animals.slice(2, 4));
// Expected output: Array ["camel", "duck"]

console.log(animals.slice(1, 5));
// Expected output: Array ["bison", "camel", "duck", "elephant"]

console.log(animals.slice(-2));
// Expected output: Array ["duck", "elephant"]

console.log(animals.slice(2, -1));
// Expected output: Array ["camel", "duck"]

console.log(animals.slice());
// Expected output: Array ["ant", "bison", "camel", "duck", "elephant"]
```
```const months = ['Jan', 'March', 'April', 'June'];
months.splice(1, 0, 'Feb');
// Inserts at index 1
console.log(months);
// Expected output: Array ["Jan", "Feb", "March", "April", "June"]

months.splice(4, 1, 'May');
// Replaces 1 element at index 4
console.log(months);
// Expected output: Array ["Jan", "Feb", "March", "April", "May"]
```
```
const str = 'The quick brown fox jumps over the lazy dog.';

const words = str.split(' ');
console.log(words[3]);
// Expected output: "fox"

const chars = str.split('');
console.log(chars[8]);
// Expected output: "k"

const strCopy = str.split();
console.log(strCopy);
// Expected output: Array ["The quick brown fox jumps over the lazy dog."]
```
```
const str = 'Mozilla';

console.log(str.substring(1, 3));
// Expected output: "oz"

console.log(str.substring(2));
// Expected output: "zilla"
```
```
const paragraph = "I think Ruth's dog is cuter than your dog!";

console.log(paragraph.replace("Ruth's", 'my'));
// Expected output: "I think my dog is cuter than your dog!"

const regex = /Dog/i;
console.log(paragraph.replace(regex, 'ferret'));
// Expected output: "I think Ruth's ferret is cuter than your dog!"
```
```
function trimString(str) {
  console.log("Original String:", str);
  console.log("After trim:", str.trim());
}
// Original String: " Hello World "
// After trim: "Hello World"
trimString(" Hello World ");
```
```
const sentence = 'The quick brown fox jumps over the lazy dog.';

console.log(sentence.toLowerCase());
console.log(sentence.toUpperCase());

// Expected output: "the quick brown fox jumps over the lazy dog."
// Expected output: "THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG."
```
```
const sentence = 'The quick brown fox jumps over the lazy dog.';

const index = 4;

console.log(`The character at index ${index} is ${sentence.charAt(index)}`);
// Expected output: "The character at index 4 is q"
```
```
const str1 = 'Hello';
const str2 = 'World';

console.log(str1.concat(' ', str2));
// Expected output: "Hello World"

console.log(str2.concat(', ', str1));
// Expected output: "World, Hello"
```
```
const mood = 'Happy! ';

console.log(`I feel ${mood.repeat(3)}`);
// Expected output: "I feel Happy! Happy! Happy! "
```
---
## Array methods
1. indexOf()
2. push() -> to push element into array
3. pop() -> to remove element from last
4. shift() -> pop from starting of array
5. unshift() ->push from starting of array
6. sort() -> sort the array in increasing order
7. reverse() -> reverse element of array from end to begin
8. values() -> return all elements of array
9. includes(element) -> check if element exist or not 
10. forEach() -> iterate to every element of array 
11. join(operator) -> join array element with operator
12. find(),findIndex() -> find according to condition
13. fill(target,start,end) -> fill array with element equal to target from index start to end
14. map() -> maps each element of array as key and pair
15. filter() ->filters the array element according to condition  

**Code**
```
// push()
function pushExample(arr, element) {
  console.log("Original Array:", arr);

  arr.push(element);
  console.log("After push:", arr);
}
pushExample([1, 2, 3], 4);
// Expected Output : 1,2,3,4


// pop()
function popExample(arr) {
  console.log("Original Array:", arr);

  arr.pop();
  console.log("After pop:", arr);
}
popExample([1, 2, 3]);
// Expected Output : 1,2

// shift()
function shiftExample(arr) {
  console.log("Original Array:", arr);

  arr.shift();
  console.log("After shift:", arr);
}
shiftExample([1, 2, 3]);
// Expected Output : 2,3

// unshift()
function unshiftExample(arr, element) {
  console.log("Original Array:", arr);

  arr.unshift(element);
  console.log("After unshift:", arr);
}
unshiftExample([1, 2, 3], 0);
// Expected Output : 0,1,2,3

// forEach()
function forEachExample(arr) {
  console.log("Original Array:", arr);

  arr.forEach(function(item, index) {
    console.log(item, index);
  });
}
forEachExample([1, 2, 3]);
// Expected Output : {1,0},{2,1},{3,2}

// map()
function mapExample(arr) {
  console.log("Original Array:", arr);

  let newArr = arr.map(function(item) {
    return item * 2;
  });
  console.log("After map:", newArr);
}
mapExample([1, 2, 3]);
// Expected Output : 2,4,6

// filter()
function filterExample(arr) {
  console.log("Original Array:", arr);

  let newArr = arr.filter(function(item) {
    return item > 3;
  });
  console.log("After filter:", newArr);
}
filterExample([1, 2, 3, 4, 5]);
// Expected Output : 4

// find()
function findExample(arr) {
  console.log("Original Array:", arr);

  let found = arr.find(function(item) {
    return item > 3;
  });
  console.log("After find:", found);
}
findExample([1, 2, 3, 4, 5]);
// Expected Output : 4

// sort()
const months = ['March', 'Jan', 'Feb', 'Dec'];
months.sort();
console.log(months);
// Expected output: Array ["Dec", "Feb", "Jan", "March"]

const array1 = [1, 30, 4, 21, 100000];
array1.sort();
console.log(array1);
// Expected output: Array [1, 100000, 21, 30, 4]

//reverse
const array1 = ['one', 'two', 'three'];
console.log('array1:', array1);
// Expected output: "array1:" Array ["one", "two", "three"]

const reversed = array1.reverse();
console.log('reversed:', reversed);
// Expected output: "reversed:" Array ["three", "two", "one"]

// Careful: reverse is destructive -- it changes the original array.
console.log('array1:', array1);
// Expected output: "array1:" Array ["three", "two", "one"]

//forEach
const array1 = ['a', 'b', 'c'];

array1.forEach((element) => console.log(element));

// Expected output: "a"
// Expected output: "b"
// Expected output: "c"

//includes
const array1 = [1, 2, 3];

console.log(array1.includes(2));
// Expected output: true

const pets = ['cat', 'dog', 'bat'];

console.log(pets.includes('cat'));
// Expected output: true

console.log(pets.includes('at'));
// Expected output: false


//fill 
const array1 = [1, 2, 3, 4];

// Fill with 0 from position 2 until position 4
console.log(array1.fill(0, 2, 4));
// Expected output: Array [1, 2, 0, 0]

// Fill with 5 from position 1
console.log(array1.fill(5, 1));
// Expected output: Array [1, 5, 5, 5]

console.log(array1.fill(6));
// Expected output: Array [6, 6, 6, 6]

```
## Filter,Map,Reduce
Filter let's you filter element based on condition you provide, it creates a new array.
Map hold key-pair object and remembers original insertion order of keys. It has some methods as below -
 **Map methods:** 
          -- clear()
          -- delete()
          -- set()
          -- get()
          -- has()
          -- forEach()
 Reduce iterates on array and filter element by condition.
```
const words = ['spray', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter((word) => word.length > 6);

console.log(result);
// Expected output: Array ["exuberant", "destruction", "present"]

```
```
const map1 = new Map();
map1.set('bar', 'foo');

console.log(map1.get('bar'));
// Expected output: "foo"

console.log(map1.get('baz'));
// Expected output: undefined

console.log(map1.has('bar'));
// Expected output: true

console.log(map1.delete('bar'));
// Expected result: true
// True indicates successful removal
map1.clear();
```
