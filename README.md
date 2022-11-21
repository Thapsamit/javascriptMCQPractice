# javascriptMCQPractice

## Link of MCQs

https://github.com/lydiahallie/javascript-questions


## Day 1 (Total Attempted - 1-30 )

### Correct:-
1,2,4,5,6,7,9,10,15,16,19,21,22,23,24,25,26,27,30

```
let greeting;
greetign = {}; // Typo!
console.log(greetign);
```

- create window.greetign object (To avoid this use "use strict")


```
function bark() {
  console.log('Woof!');
}

bark.animal = 'dog';
```
- It is fine as function treated as objects

### Incorrect:-
3,8,11,12,13,14,17,18,29

```
function Person(firstName, lastName) {
  this.firstName = firstName;
  this.lastName = lastName;
}

const member = new Person('Lydia', 'Hallie');
Person.getFullName = function() {
  return `${this.firstName} ${this.lastName}`;
};

console.log(member.getFullName());
```

**In JavaScript, functions are objects, and therefore, the method getFullName gets added to the constructor function object itself. For that reason, we can call Person.getFullName(), but member.getFullName throws a TypeError.

If you want a method to be available to all object instances, you have to add it to the prototype property:**

```
Person.prototype.getFullName = function() {
  return `${this.firstName} ${this.lastName}`;
};
```

```
function getPersonInfo(one, two, three) {
  console.log(one);
  console.log(two);
  console.log(three);
}

const person = 'Lydia';
const age = 21;

getPersonInfo`${person} is ${age} years old`;
```
- If you use tagged template literals, the value of the first argument is always an array of the string values. The remaining arguments get the values of the passed expressions!

### Doubts

- Objects keys are always treat as strings
- Objects as reference 
- Static methods in class 
- Function in js are treated like an object
- Prototype is used to add a function that is available to all the instance objects
- If we do not use new keyword in object creation it will use globalobject
  ```
  const obj = Person("Amit","Thapliyal")
  ```
  - This will give obj as undefined but this.fname = "amit" and this.lname = "Thapliyal" will asssign to global object

- capturing then target and then bubbling event occurs
- All object has prototype but base object do not has prototype (created using new object)
- Objects always compared using reference doesn't matter whether using == or ===
- Use strict do not allow to use global variables
- Js creates global object and this keyword for us
- we can add properties to String using prototype



## Day 2 (Total Attempted - 31-50)

### Correct 
32,35,40,41,47,50

### Incorrect
31,33,34,36,37,38,39,42,43,44,45,46,49

```
function sayHi() {
  return (() => 0)();
}

console.log(typeof sayHi());

```
- "number" as it will invoked and return 0 (Immediately Invoked Function).


### Doubt
- The deepest element that caused the event is the target of event.
- bind returns a function but not executed immediately
- There are 8 falsy values:
    - undefined
    - null
    - NaN
    - false
    - '' (empty string) 
    - 0
    - -0
    - 0n (BigInt(0))
    
- typeof typeof 0. it returns string
- When you set a value to an element in an array that exceeds the length of the array, JavaScript creates something called "empty slots". These actually have the value of undefined, but you will see something like:
``` [1, 2, 3, empty x 7, 11] ```
- In catch block we received the argument which is not the same from any outside variable
- In Js everything is either primitive or object
- setInterval returns a uniqueId.
- generator function
- promise.race method returns the first promise that resolved/reject first
- 
``` 
 const num = parseInt('7*6', 10); returns 7 as it is first argument
```

## Day 3 (Total Attempted - 51-70 )

### Correct
51,52,53,54,55,56,59,60,66,67

### Incorrect
57,58,61,62,63,64,65,68,69,70

```
const value = { number: 10 };

const multiply = (x = { ...value }) => {
  console.log((x.number *= 2));
};

multiply(); #### 20 
multiply(); #### 20
multiply(value); #### 20
multiply(value); #### 40
```

- First two time default value is used hence new object created each time but in third or fourth time we passed value object to the function 

```
let num = 10;

const increaseNumber = () => num++;
const increasePassedNumber = number => number++;

const num1 = increaseNumber();
const num2 = increasePassedNumber(num1);

console.log(num1);
console.log(num2);
```
- 10 10 as unary operator returned and then increments 

```
const person = { name: 'Lydia' };

Object.defineProperty(person, 'age', { value: 21 });

console.log(person);
console.log(Object.keys(person));
```
- defineProperty method,we can add new properties or modify existing ones but they are by default not enumerable theresfore when using Object.keys it will only not give "age" key. Properties added using defineProperty method they are immutable by default.


### Doubt
- With throw keyword we can create custom exception and can throw explicit exception.
- When we try to invoke something that is not a function, a TypeError is thrown. In this case TypeError: pet.bark is not a function, since pet.bark is undefined.
- An imported module is read-only: you cannot modify the imported module. Only the module that exports them can change its value.
- variables declared with the var, const or let keyword cannot be deleted using the delete operator.
- The delete operator returns a boolean value: true on a successful deletion, else it'll return false. 
- When we add a property to global object then we can delete it.
- 
```
const data = JSON.stringify(settings, ['level', 'health']);
```
  - Second argument is replacer which can be an array or function. If It is array then the property name in the array will be added to JSON.stringify.
  - If the replacer is a function, this function gets called on every property in the object you're stringifying. The value returned from this function will be the value of the property when it's added to the JSON string. If the value is undefined, this property is excluded from the JSON string.
- If we do not return a value from reducer then it will give undefined in accumulator. Accumulator is the first parameter and it will take first parameter if not specified.
- 
```
console.log(Symbol('foo') === Symbol('foo'));
``` 
- Symbol is always unique and it returns false as it gives description which is independent of whether they have same value or not
- With the padStart method, we can add padding to the beginning of a string.The value passed to this method is the total length of the string together with the padding.If the argument passed to the padStart method is smaller than the length of the array, no padding will be added.

## Day 4 (Total Attempted - 71-90)

### Correct
72,73,75,76,77,78,79,80,81,82,83,86,87,90

### Incorrect
71,74,84,85,89

### Doubt
- A promise always return a pending state at first.
- Push function Returns length of the list.
- Object.freeze(obj) - it restricts the object to add,delete or modify values.
- for-in we can iterate over enumerable properties that is keys.
- for-of we can iterate over iterable that is values.
- By default the arguments are always undefined
- You can set a default parameter's value equal to another parameter of the function, as long as they've been defined before the default parameter.



## Day 5 (Total Attempted - 91-100)

### Correct
91,92,93,94,96,99,100


### Incorrect
95,97,98


### Doubt
- Regular function have a prototype property, which is an object with constructor property but arrow function do not have prototype property.
- JS Does automatic semicolon insertion.
- Symbol not enumerable.
-


## Day 6 (Total attempted - 101-110)

### Correct 
103,105,106,109

### Incorrect
101,102,107,108

### Doubt

```
const one = false || {} || null;
const two = null || false || '';
const three = [] || 0 || true;

console.log(one, two, three);
```
- When it is truthy value it gives the first truthy value otherwise if all false it gives last value ([] or {} are truthy values)
- With the await keyword in secondFunction, we literally pause the execution of an async function until the value has been resolved before moving to the next line.
- We can pass any type of value we want to Promise.resolve, either a promise or a non-promise.
- Under the hood, emojis are unicodes.These are always the same for the same emojis, so we're comparing two equal strings to each other, which returns true.
- With splice method, we modify the original array by deleting, replacing or adding elements. 
- JSON.parse() - Parses JSON to a JavaScript value.


## Day 7 (Total Attempted - 111-122)

### Correct
111,114,118,120,121


### Incorrect
112,113,115,116,117,119,122

### Doubt
- Expressions within template literals are evaluated first. 
- As long as there is a reference, the object won't get garbage collected.Even if we set to null to start the garbage collector process.
- when use deafult parameters then if we pass an object explicitly then it refers to the same object but if we don't specify the object then it makes a copy of the object which not effect the original  copy of the object.
- func(...[1,2,3]) can spread like this
- With the optional chaining operator ?., we no longer have to explicitly check whether the deeper nested values are valid or not. If we're trying to access a property on an undefined or null value (nullish), the expression short-circuits and returns undefined



## Day 8 - (Total Attempted - 123-130 )

### Correct
126,130

### Incorrect
123,124,125,127,128

### Doubt
- Number.isNaN(x) - check whether passed value is number ?? and check whether it is nan
- isNan check whether given item is not a number

### Generator function in JS:-
- It Returns a generator object
Why Generators?
Let say storing array of numbers to store elements instead use on the fly to generate value
```
    
function* numberGen(){
let i = 0;
yield 1;
yield 2;
  
}
const gen = numberGen();
console.log(gen.next()) // gives next value
console.log(gen.next())// gives next value 
// It will go till it has values to yield if not then give undefined
    
```

```
function* numGen(){
let i  = 0;
while(true){
  yield i++;
}
}
const gen =  numGen();
console.log(gen.next().value)
console.log(gen.next().value)
console.log(gen.next().value)
console.log(gen.next().value)
```
Important points on Generator:-
- Generators are functions that can be exited and later re-entered and can use the previous context(variable bindings) will be saved re-entrances.
- Generator + promises = Tools for asynchronous programming and can reduce callback hell and inversion control.
- yield* delegates to another generator function
- the generator function's body is executed until the first yield expression, which specifies the value to be returned from the iterator.
- A return statement in a generator, when executed, will make the generator finish (i.e. the done property of the object returned by it will be set to true). 
- 
```
function* anotherGenerator(i) {
  yield i + 1;
  yield i + 2;
  yield i + 3;
}

function* generator(i) {
  yield i;
  yield* anotherGenerator(i);
  yield i + 10;
}

```
- generator are not constructable











