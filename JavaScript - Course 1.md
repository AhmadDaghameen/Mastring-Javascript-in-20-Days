# JavaScript: From First Steps to Professional
---

### `Course description`
---


> In this course, we’ll start from square one to take our first steps into the wide world of JavaScript, and we’ll walk away with the core skills we need to become productive JavaScript programmers. Through a series of hands-on projects, we’ll learn how to write our own JS code to manipulate and add interactivity to our websites, in cooperation with our friends HTML & CSS. We’ll wrap our heads around the building blocks of JS programs, including data types, objects, arrays, and functions, and how to work with them using core language features like operators, variables, loops, and branching logic. We’ll even encounter modern JS features & syntax such as arrow functions, destructuring, promises and async/await. After this course we’ll be ready to dive deeper into topics like advanced JS, functional programming, frontend frameworks like React, or backend programming with Node.


### `Course outline`
---
```markdown
- Part 1
    * Intro & course overview
    * JavaScript: What? Why? How?
    * Working with the DOM (HTML)
    * Data Types
    * Working with Strings
    * Operators & Expressions
    * Variables
    * Objects & Arrays
- Part 2
    * Part 2 project overview
    * Working with a code editor
    * Functions & Scope
    * Event Handlers
    * Conditionals
    * Loops
- Part 3
    * Part 3 project overview
    * Fetch
    * Promises
    * Async/Await
    * Map & Filter
    * Destructuring & spread syntax
    * Debugging & error handling
    * Modules, import & export
    * Course recap & next steps
```

## MATERIAL
---
---
### Part **1** : DOM - Data Types - Arrays & Objects
---

#### What Is JS?
 > Javascript is a programming language, it is a language of the web, JavaScript can modify and interact with HTML and CSS, JavaScript was created in 1995 by Brendan Eich. 
 
#### DOM <small>`Document Object Model`</small>
> It is an Object Representation of the HTML document, used to interact and modify Elements and Styles.

#### Reading the DOM with JS
* Access Document: `document`
* Title: `document.title`
* Body: `document.body`
* Body Childrens Elements: `document.body.children`
* Find Elements: 
    * By ID: `document.getElementById("board")`
    * Query Selector: `document.querySelector("#board")`
    * By Tag Name: `document.querySelector("#board")` Or `document.querySelectorAll("h1")`
    * By Class Name: `document.getElementsByClassName("player")` Or `document.querySelectorAll(".player")`
* Retrieve Element Attributes
    * Get Length attribute: `document.getElementsByClassName("player").length` Or `document.querySelectorAll(".player").length`
    * Get text inside an element using `textContent`: `document.getElementById("p1-name").textContent`
* Modify Element Attributes:
    * Change Title: `document.title = "My Page"`
    * Modify Inner Text of an element: `document.getElementById("p1-name").textContent = "Sofia"`
    * Append inner text of an element: `document.getElementById("p1-name").append(" & friends")`
    
**Your Friend : [MDN](https://developer.mozilla.org/) :sparkles:**




#### Values : 
> :arrow_forward:Chunks of information with different Types
> :arrow_forward: you can find the Type of Data using `typeof "42"`.
> :arrow_forward:There is Two Types of Data: Primitive  & Objects.
>* Primitive:
>    * string: "Hello!", '`I ❤️ backticks`', '867-5309', "42"
>    * number: 45, 523.25, -3.45, 1.21e9, Infinity, ....
>    * boolean: true , false only
>    * undefined: undefined value means it is declared but unassigned yet.
>    * null: value assigned to empty or nothing.

#### Working with Strings :
String Methods: 
* length `"super".length`
* [` `] `"ALOHA"[0]` 
* indexOf `"ALOHA".indexOf("L")`, `"ALOHA".indexOf("HA")`, `"ALOHA".indexOf("LOL")`
* includes `"ALOHA".includes("HA")`, `"ALOHA".includes("LOL")`
* startsWith `"ALOHA".startsWith("AL")`
* toLowerCase `"ALOHA".toLowerCase()`

**Your Friend : [MDN - Strings](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) :sparkles:**


#### Operators :
* Arithmetic operators: Order of operations same as Math
    * `+` add
    * `-` subtract
    * `*` multiply
    * `/` divide
* Comparison operators: Returns boolean
    * `>` greater than
    * `<` less than
    * `>=` greater than or equal to
    * `<=` less than or equal to
* Equality operators: <span style="color:blue"> You should almost always use the strict version </span>
    * strict equal `===`
    * loosey `==`
    * strict not equal `!==`
    * loosey not equal `!=`

**Your Friend : [MDN - Expressions & Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators) :sparkles:**

#### Expressions
> an expression evaluates (aka resolves) to a value
* 4 / 2 * 10
* "Frontend" + "Masters"
* 5 > 4 !== 3 > 4

#### Variables
> to Remember and Refers (Points) to Values.
* Use the following to declare variables
    * let `let bankruptcy;`
    * var
    * const `const myUnchangeableVariable = "Never gonna give you up";`


#### Statements vs. Expressions
> An **expression** "asks" JS for a value 
<span style="color:blue">while </span>
> A **statement** "tells" JS to do something

#### Objects
* Arrays : 
    * keep multiple values together in a single collection, can store values with diferent types at the sametime
    * Array methods:
        * length
        * [` `]
        * indexOf()
        * includes()
        * pop()
        * push()
        * sort()
        * join()
        * concat()
 
 **Your Friend : [MDN - Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) :sparkles:**
 
 #### Mutable vs. Immutable
 > Using immutable data & variables is usually best
 > Arrays actions might mutate the array, while other action not.
 
 * Objects : 
 > Objects collect multiple values together to describe more complex data
 > objects let us point at related values using properties in the object.
 > we can access properties using <mark> . </mark> operator like `js.name` , `js.isAwesome`
 > we can use property values or we can set them.
 
 * Methods
 > Properties can point to functions too, 
We call function-properties "methods" on objects
 ```javascript
const dog = {
    name: "Ein",
    breed: "Corgi",
    speak: function () {
        console.log("woof woof");
    }
}
dog.speak();
```
> speak is a prperty that points to a function which is called a Method, we can call that Method using <mark>.</mark> operater and `()` like  `dog.speak();`
 
> we can use `this` in a method to reference other properties of the object. but Its behavior is complicated & can be tricky.
 
 **Your Friend : [MDN - this](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this) :sparkles:**
 
 * Nested objects
 > objects can be contained in other objects
 ```javascript
const menu = {
    lunch: {
        appetizer: "salad",
        main: "spaghetti",
        dessert: "tiramisu"
    },
    dinner: {
        appetizer: "samosa",
        main: "saag paneer",
        dessert: "gulab jamun"
    }
};

const tiramisu = menu.lunch.dessert;
```
> or can be collected in arrays
```javascript
const spices = [
    {name: "Emma", nickname: "Baby"},
    {name: "Geri", nickname: "Ginger"},
    {name: "Mel B", nickname: "Scary"},
    {name: "Mel C", nickname: "Sporty"},
    {name: "Victoria", nickname: "Posh"}
];
```

* Built in objects
    - document
    - console
    - Math
    - Strings: Strings are primitive values (not objects) but JS automatically wraps them in String objects
 
  **Your Friend : [MDN - Standard built-in objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects) :sparkles:**


<div style='page-break-after: always'></div>



---
### Part **2** : Functions - Events - Branches & Loops
---

#### Functions
> functions do things

- declaring (creating) a function: 
```javascript
function myFunction(x) {
    return x;
}
```
- using functions 
```javascript
myFunction("1");
```
- Parameters & Arguments
 parameters are the inputs a function expects like `x` in `myFunction` function, they named as variable and used as variables. arguments are the actual values the function is called with like `"1"` in calling of `myFunction("1");`
- JS is pretty "loosey-goosey" about missing/extra arguments when calling a function. What happens depends on your particular code. 
- functions return `undefined` when there is no return in the function
##### Arrow functions `=>`

```javascript
(x, y) => x + y
```
- can be assigned to variables
- For one-parameter functions, parentheses are optional  `x => x*x`. while for multiple parameters, parentheses are required `(firstName, lastName) => firstName + " " + lastName`
- we can use curly braces for a "normal" function body. In that case, we need a return.
    ```javascript
    const addAndLog = (x, y) => {
        let sum = x + y; 
        console.log('The sum is', sum);
        return sum;
    }
    ```

#### Scope

> In JS it doesn't just matter what variables we declare, it also matters where we declare them. Scope determines where variables are "in play"
> Scopes are nested within the program. The widest scope is the global scope and each function gets its own new scope within the scope where it was declared
> Within each scope, you can access variables declared in a wider scope (e.g. global scope), but not the way around.

#### Events & Handlers 
> `Events` Fired when things happen on the page. Events can be detected using `event listeners`. The .addEventListener(event, handler) method lets us listen for events on a DOM element. `event.target` is the element the event fired on
```javascript
document.addEventListener("click", (event) => {
    console.log(event.target); 
});
```

#### Loops
> Loops let us run the same chunk of code multiple times (iterations)
 * Loop Syntacs:
    * for:  `for (let i = 0; i < numbers.length; i++)`
    * for of:  `for (let n of numbers)`
    ```javascript
    for (let rep = 0; rep < 10; rep += 1) {
        console.log("now doing rep", rep);
    }
    console.log("do you even lift bro");
    ```
> map & filter: functions that iterate an array
    ```javascript
    const spices = [
        {name: "Emma", nickname: "Baby"},
        {name: "Geri", nickname: "Ginger"},
    ];
    const nicknames = spices.map(s => s.nickname + " Spice");
    const mels = spices.filter(s => s.name.includes("Mel"));
    ```
> Spread (...) : iterating over arrays 
    ```javascript
    const oldBurns = ["square", "wack"];
    const newBurns = ["basic", "dusty", "sus"];
    const burnBook = [...oldBurns, ...newBurns];
    ```
    
#### Conditionals

* if : if statements let us execute code if a condition is true
    ```javascript
    const you = {wannaBeMyLover: true};
    if (you.wannaBeMyLover) {
        you.gottaGetWithMyFriends = true;
    }
    ```
* else : 
    ```javascript
    if (you.reallyBugMe) {
        console.log("Goodbye");
    } else {
        console.log("Hello");
    }
    ```
* if and else can be chained.
> a condition is an boolean expression, if it is another values then JS evaluate its truthiness

* Logical Operators : `&&` `||` `!`
* Conditional ternary operator: shortcut operator for writing quick conditionals
    ```javascript
    condition ? valueIfTrue : valueIfFalse;
    ```

---
### Part **3** :   (A)Sync - Pro Syntax - Bugs & Errors
---

#### Loops ...continued
* while loops: run a chunk of code over & over if a (condition) is true.
> JS can only do one task at a time ("single-threaded")

#### (A)synchronous code
 JS can usually run straight through  programS "synchronously"

```javascript
console.log("This will print first");
setTimeout(() => console.log("This will print third"), 1000);
console.log("This will print second");
```


  **Your Friend : [MDN - Introducing Asynchronous JS](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Introducing) :sparkles:**
  
:arrow_forward:[Philip Roberts: What the heck is the event loop anyway?](https://www.youtube.com/watch?v=8aGhZQkoFbQ)


#### Fetching data
> `fetch()` lets us use JS to load data from APIs
    ```javascript
    fetch("https://dog.ceo/api/breed/hound/list")
    ```
#### Promises
> JS writes us an "IOU" for the data value it doesn't have yet

Promises States:
*  pending
*  fulfilled
*  rejected

> Promises are "asynchronous".

> The Promise we get from `fetch()` resolves to a `Response` object

#### await 
> await lets us tell JS to stop and wait for an asynchronous operation to finish
> Calling the .json() method on the response parses its body as a JSON object

```javascript
let response = await fetch("https://dog.ceo/api/breed/hound/list");
let body = await response.json();
```

#### Destructuring
> Destructuring is a fancy way of declaring multiple variables at once
By "extracting" values from an object with their property names

```javascript
let {name, nickname} = spices[0];
```
* we can omit values that we don't need `let {nickname} = spices[2];`
* We can ignore the values in the array `const [,,melB] = spices;`
* We can use `...` to collect remaining values `const [babySpice, ...adultSpices] = spices;`


#### async functions
> we can't await something in a regular function, We need to make it an async function

```javascript
async function fetchResponse(url) {
    const response = await fetch(url);
    return response;
}
```



#### Modules
> Modules let us split big codebases across multiple files

> JS modules work differently from JS scripts

> One difference is that we can't use await outside of a function in a script

> One difference is that we can't use await outside of a function in a script

> import && export : `export` lets us expose variables from our module's scope to the outside world. `import` lets us use an exposed variable from another module

    ```javascript
    // myModule.js
    const veryUsefulFunction = () => "I came from a module";
    export { veryUsefulFunction };
    ```

  **Your Friend : [MDN - JS Modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules) :sparkles:**


#### Debugging
> we can use `console.log()`  `console.warn()` `console.error()`
> we can use `debugger;` to create breakpoints


#### Error handling
> Usually errors will cause JS to stop running our code
> try lets us "watch out" for potential errors while catch lets us manage errors when they occur

```javascript
try {
    thisMightThrowAnError();
} catch (error) {
    console.error("As if! Error:", error); 
    console.log("Whatever, let's press on anyway");
}
console.log("still rollin' with the homies");
```
  **Your Friend : [MDN - try...catch](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch) :sparkles:**

## PROJECTS
---
---
### Part `1`: Tic Tac Toe	
 GitHub Tic Tac Toe

### Part `2`: Quiz Game


### Part `3`: Doggos


## CHALLENGES
---
---

- Compound Assignment With Augmented Multiplication
```javascript
let a = 5;
let b = 12;
let c = 4.6;
// a should equal 25
// b should equal 36.
// c should equal 46.

// *Solution*
a *= 5;
b *= 3;
c *= 10;
```

---
- Concatenating Strings with the Plus Equals Operator
```javascript
// myStr should have a single space character between the two strings
// myStr should have a value of the string This is the first sentence. This is the second sentence.
// You should use the += operator to build myStr.

// *Solution*
let myStr;
myStr = "This is the first sentence.";
myStr += " This is the second sentence."
```
---
- Use Dot Notation to Access the Properties of an Object

```javascript
// Your code should use console.log to print the value for the name property of the dog object.
// Your code should use console.log to print the value for the numLegs property of the dog object

// *Solution*
let dog = {
  name: "Spot",
  numLegs: 4
};
// Only change code below this line

console.log(dog.name);
console.log(dog.numLegs);
```
---

- QUESTION #1 : What will be the output of each console.log statement?

```javascript
let a = 0;
let b = "0";
let c = false;
let d = "false";
                        //// *Solution*
console.log(a == b);    //true  : loosey equal, same value 
console.log(b === c);   //false : strict equal, deferent types
console.log(!!d);       //true  : empty string is true, !true => false ==> !(false) true
```

---
- QUESTION #2: Consider the following JavaScript expression, What will be the output of this expression?

```javascript
console.log(4 + 5 * "7");
// *Solution* 
// result : 39
// steps: convert to int: "7" -> 7 => multiply: (5*7) => add: 4 + (35)
```
---
- QUESTION #3: Evaluate the following expression: What will be the output of this expression?
```javascript
let result = 5 + 2 * 3 - 1;
// *Solution* 
// result : 39
// steps: multiply: 2 *3 => add: 5 + (6) => subtract: (11) - 1
```

- QUESTION #4: Consider the following code: What will be the output of each console.log statement? 

```javascript
let x = 10;
let y = '10';
                        // *Solution* 
console.log(x == y);    // true: loosey equal, same value diferent types.
console.log(x === y);   // false: strict equal, deferent types.
```
---
- QUESTION #5: Given the code below: What is the value of result?
```javascript
let num = "15";
let isPositive = true;
let result = (num > 10 && isPositive) || num < 0;
                        //*Solution* 
console.log(result);    // true
                        //convert "15" to int ==> 15  
                        //evalute first condition (num > 10) -> (15 > 10) ==> true
                        //evalute second condition (true && true) ==> true
```

---
- Copy Array Items Using slice()

```javascript
function forecast(arr) {
  // Only change code below this line
   //*Solution*
   arr = arr.slice(2,4);
  return arr;
}

// Only change code above this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```

---
- Combine Arrays with the Spread Operator
```javascript
function spreadOut() {
  let fragment = ['to', 'code'];
  //*Solution*
  let sentence = ['learning', ...fragment, 'is', 'fun']; // Change this line
  return sentence;
}

console.log(spreadOut());
```

---
- Profile Lookup
```javascript
// Setup
const contacts = [
  {
    firstName: "Akira",
    lastName: "Laine",
    number: "0543236543",
    likes: ["Pizza", "Coding", "Brownie Points"],
  },
  {
    firstName: "Harry",
    lastName: "Potter",
    number: "0994372684",
    likes: ["Hogwarts", "Magic", "Hagrid"],
  },
  {
    firstName: "Sherlock",
    lastName: "Holmes",
    number: "0487345643",
    likes: ["Intriguing Cases", "Violin"],
  },
  {
    firstName: "Kristian",
    lastName: "Vos",
    number: "unknown",
    likes: ["JavaScript", "Gaming", "Foxes"],
  },
];

function lookUpProfile(name, prop) {
  // Only change code below this line
for (let x = 0; x < contacts.length; x++) 
    {
      if (contacts[x].firstName === name) 
      {
        if (contacts[x].hasOwnProperty(prop)) 
        {
          return contacts[x][prop];
        } 
        else 
        {
          return "No such property";
        }
      }
    }
    return "No such contact";
  // Only change code above this line
}

lookUpProfile("Akira", "likes");
```

---
- Write Reusable JavaScript with Functions
```javascript
function reusableFunction (){
  console.log("Hi World");
}

reusableFunction ();
```
```javascript
// Setup
let sum = 0;

function addThree() {
  sum = sum + 3;
}

// Only change code below this line

function addFive() {
  sum += 5
}
// Only change code above this line

addThree();
addFive();
```
---
- Return a Value from a Function with Return
```javascript
function timesFive (num) {
 return num * 5
}
```
---
- Global Scope and Functions

```javascript
// Declare the myGlobal variable below this line
let myGlobal = 10;
let oopsGlobal = 5;
function fun1() {
  // Assign 5 to oopsGlobal here
  let myGlobal = 5;
}

// Only change code above this line

function fun2() {
  let output = "";
  if (typeof myGlobal != "undefined") {
    output += "myGlobal: " + myGlobal;
  }
  if (typeof oopsGlobal != "undefined") {
    output += " oopsGlobal: " + oopsGlobal;
  }
  console.log(output);
}
```


---

- Local Scope and Functions
```javascript
function myLocalScope() {
  // Only change code below this line
  let myVar = "";
  console.log('inside myLocalScope', myVar);
}
myLocalScope();

// Run and check the console
// myVar is not defined outside of myLocalScope
console.log('outside myLocalScope', myVar);
```
---

- Global vs. Local Scope in Functions
```javascript
// Setup
const outerWear = "T-Shirt";

function myOutfit() {
  // Only change code below this line
  const outerWear = "sweater";
  // Only change code above this line
  return outerWear;
}

myOutfit();
```

---

- Stand in Line
```javascript
function nextInLine(arr, item) {
  // Only change code below this line
  arr.push(item);
  let removed = arr.shift();
  return removed;
  // Only change code above this line
}

// Setup
let testArr = [1, 2, 3, 4, 5];

// Display code
console.log("Before: " + JSON.stringify(testArr));
console.log(nextInLine(testArr, 6));
console.log("After: " + JSON.stringify(testArr));
```


---


