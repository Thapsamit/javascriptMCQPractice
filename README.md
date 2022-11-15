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



## Day 2 (Total Attempted - 30-50)

# Correct 
32,35,40,41,47,50

# Incorrect
31,33,34,36,37,38,39,42,43,44,45,46,49

```
function sayHi() {
  return (() => 0)();
}

console.log(typeof sayHi());

```
- "number" as it will invoked and return 0 (Immediately Invoked Function).


# Doubt
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



