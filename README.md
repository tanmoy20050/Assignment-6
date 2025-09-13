
1. What is the difference between var, let, and const?

var

Function scoped
Redeclare , Reassign
Hoisted with undefined
পুরোনো JavaScript এ বেশি ব্যবহৃত

let

Block scoped
Redeclare , Reassign
Hoisted but Temporal Dead Zone (TDZ) এ থাকে

const

Block scoped
Redeclare , Reassign
Constant reference ধরে রাখে (object এর ভেতরের property change করা যায়)
var a = 10;
var a = 20; 

let b = 30;
b = 40; 

const c = 50;


2. What is the difference between map(), forEach(), and filter()?
forEach() → শুধু loop চালায়, return করে না
map() → প্রতিটা element transform করে নতুন array return করে
filter() → condition অনুযায়ী true value গুলো নিয়ে নতুন array return করে
const numbers = [1, 2, 3, 4, 5];

numbers.forEach((n) => console.log(n)); 

const squares = numbers.map((n) => n * n);
console.log(squares); 

const evens = numbers.filter((n) => n % 2 === 0);
console.log(evens); 


3. What are arrow functions in ES6?
Arrow functions → shorter & cleaner syntax, এবং this inherit করে surrounding scope থেকে।

function add(a, b) {
  return a + b;
}


const addArrow = (a, b) => a + b;
** Benefits:**

Shorter syntax
Lexical this binding
Useful for callbacks, array methods


4. How does destructuring assignment work in ES6?
Destructuring → array/object থেকে value বের করে variable এ রাখা যায়।

const numbers = [10, 20, 30];
const [x, y, z] = numbers;
console.log(x, y, z); 

const user = { name: "Riyaz", age: 21 };
const { name, age } = user;
console.log(name, age); 


5. Explain template literals in ES6. How are they different from string concatenation?
Template literals (backticks ` দিয়ে লেখা হয়):

Variable ও expression embed করা যায় → ${}
Multi-line string লেখা যায়
const name = "Md Riyaz Akondo";
const age = 21;

const text1 = "My name is " + name + " and I am " + age + " years old.";
const text2 = `My name is ${name} and I am ${age} years old.`;

console.log(text1);
console.log(text2);
