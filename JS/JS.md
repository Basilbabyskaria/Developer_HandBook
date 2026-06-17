# JAVA SCRIPT

- Programming Language made for the web
- light weight
- interpreted or just in time compiled

- Javascript is dynamic and weakly types
  - Dynamic - Variables in JavaScript are not directly associated with any particular data type, any variable can be assigned (and re-assigned) values of all types
  ```
  let foo = 42; // foo is now a number
  foo = "bar"; // foo is now a string
  foo = true; // foo is now a boolean
  ```
  - Weakly typed - it allows implicit type conversion when an operation involves mismatched types, instead of throwing errors it converts one to data type of the other .
  ```
  const foo = 42; // foo is a number
  const result = foo + "1"; // JavaScript coerces foo to a string, so it can be concatenated with the other operand
  console.log(result); // 421
  ```
- End every line of code with a `;`
- JS is Case Sensitive

## Comments

One line : `//`
Multi Line : `/**/`

## Data Types

- Undefined (Premitive DataType)
- Null (Premitive DataType)
- String (Premitive DataType)
- Number (Premitive DataType)
- Boolean (Premitive DataType)
- Bigint (Premitive DataType)
- Symbol (Premitive DataType)
- Object (Reference DataType)

All primitive datatypes except for null can be tested using `typeof` operator,`typeof(null)` returns object so `===` is used to check for null.`undefined` indicates the absence of a value, while `null` indicates the absence of an object (which could also make up an excuse for typeof null === "object")

Premitive data types are assigned by copy which means if we create a variable and assign it to an another variable both are stored in seperate memory spaces changes made to one does not affect other.
On the other hand Reference data types are assigned by reference changes made to one affects the other.

To Over Come this

```
Option 1 (assign)

declare new object as empty and use assign

let ={a,b,c}
let b={}
object.assign(b,a)

Option 2 (spread operator)
let b={...a}

```

## Variable

- A label to point to a data
- Name Storage for data
- When a variable is declared memory is allocated with the variable name
- Can be declared using `var`,`let`,`const`
- As JS is case sensitive camel case is generally used (properCamelCase)

### var

- Global Scoped
- Can be Declared multiple time's
- Can be reassigned
- `var a=1;`

### let

- Block Scopped
- Can't be Declared multiple time's
- Can be reassigned
- `let a=1;`

### const

- can't be reassigned
- `const a=1;`
- A const array can be reassigned by using bracket notation

```
const a=[1,2,3]
a=[3,4,5] >>error
a[0]=5
console.log(a)  >>[5,2,3]
```

## Assigning values

- While assigning string value to a variable `''`,`""` and a pair of ` can be used  
  let a="hi"  
  let a='hi'
- Simpley declaring a a variable without assigning a value set it as undefined

## Operators

- Addition `+` (All so used for concatination of strings)
- Substraction `-`
- Multiplication `*`
- Division `/`
- Modulas `%` (Gives Reminder)
- Increment `++`
- DEcrement `--`
- Assignment `=`
- Comparison `==`

```
let a=1
console.log(a++)  >> 1
console.log(++a)  >> 2

```

### Logical Operators

- `||` OR (console.log(false || a); >> a)
- `&&` AND
- `!` NOT (!true=false)

undefined,null,0,NaN,'' are considered as false

### Equality

```
let a=1,b='1';

loose equality (==) converts both to same datatype and then compare
console.log(a==b) >> true

Strict equality (===) Check's difference in datatype too
console.log(a===b) >> false

loose Inequality
console.log(a!==b) >> false

Strict Inequality
console.log(a!===b) >> True
```

### Escape Character `\`

`let str= "this is a double quotes: \" "    `  
will print the double quotes  
U can allso achive this my mixing other qoutes \
`'this is a double quotes: "'`

### Turnary Operator `? :`

Basically If Else  
`let freeTicket=age>10?true:false`  
if value of age is greater than 10 freeTicket will be set as true otherwise as false

### Nullish coalescing `??`

- returns right handside when left hand side is null or undefined
- Like isnull in SQL

```
let a=null,b='1';
console.log(a??b) >>1
```

### Length Of String

```
let a='car'
console.log(a.length)  >> 3
```

### []

Like accessing a array element a character at an index can be accessed using `[]`

```
let a='car'
console.log(a.[0])  >> c
console.log(a.[-1])  >> r (Returns last character)

```

### Strings Immutability

Once a string is created it can't be altered but we can reassign the variable

```
let a='car'
a.[0]='b'  >> error
```

## Array

- Array is a collection of same type of data
- `let array=['a','b']` an array of strings
- `let array=[['a','b'],[1,2]]` nested array

```
let array=['a','b']`
console.log(array.[0])  >> a
console.log(array.[-1])  >> b (Returns last character)


array.[0]='c'
console.log(array) >>['c','b']

let nestedarray=[['a','b'],[1,2]]
console.log(array.[1][0])  >> 1
```

- `array.push()` Push new items into end of an array
- `array.unshift()` Push new items into begining of an array
- `array.pop()` Pops last element from array
- `array.shift()` Pops first element from array

```
let array=['a','b']
array.push('c')
console.log(array) >> ['a','b','c']
array.pop()
console.log(array) >> ['a','b']
array.shift()
console.log(array) >> ['b']
array.shift('a')
console.log(array) >>['a','b']
```

### Array Destructuring

An another way to unpack values from an array or property from an object into variables

```
let array=['1','2','3','4']
let [a,b]=array
console.log(a)  >>1
console.log(b)  >>2

let [a,,,b]=array (Skips two values)
console.log(a)  >>1
console.log(b)  >>4
```

If `[ ]` is replced with `{ }` for objects

### Spread Operator `...` (Rest Operator)

To get rest of the elements when destructuring is used

```
let array=['1','2','3','4']
let [a,b, ...c]=array
console.log(c) >> ['3','4']
```

Spread Operator can allso be used for combining two arrays

```
let array1=['a','b']
let array2=['c','d']
let newArray=[...array1,...array2] >> ['a','b','c','d']
```

## Objects

- Key Value pair
- Groups together state and behaviour that are related

```
let a={
  "name":"bob",
  "salary":2000,
  "Tax":function(){
    console.log("tax")
  }
}

console.log(a.name);  >>bob
console.log(a[name]); >>bob

a.name="Ron"
console.log(a[name]); >>Ron

a.age=23
>> {
  "name":"bob",
  "salary":2000,
  "Tax":function(){
    console.log("tax")
  },
  "age":23
}

delete a.age
>> reurns to initial value

```

### Object Destructuring

Same like array

```
let {name,salary}=a
```

### Creating An Object

- Object Creation using class

```
class className{
constructor (name){
  this.name=name;
}
}
const a=className();
const b=new a('value');
```

## Functions

- Block of code which is designed to do a specific rask
- Can be reused multiple times
- JS has first class functions meaning functions are treated as any other variables,they can be passed as argument, returned by other function and can be assigned as a value to a variable
- Function that is passed as an argument to another function is called a callback function
- Functions which accepts other functions as values or returns a functions is called a higher order function

```
function declaretion :
function funcName(parameters){

}

function call :
funcName();
```

Destructuring can be used to perform multiple action on same set of data inside a function

```
function sumAndProduct(a,b){
  return[a+b,a*b]
}
let [sum,product]=sumAndProduct(1,2)
```

### Anonimus Function

- Function which does not have a name

```
var magic=function(){
  return new date();
};

```

- Even though it returns a value which is strored in a variable the function itself has no name
- These functions are exected immediately

### Arrow Function

- Anonimus functions can be converted to arrow funtions

```
var magic = (parameters) => {
  return new date();
};

if returning only one value

const magic = () => new date();

if there is only one parameter which is passed we can omit the paranthesis too
const a = x=>x*x
```

## IF ELSE

```
if(a==b){
  return "equal";
}
else {
retuen "not equal";
}
```

## SWITCH CASE

```
switch(true){
  case  a>b:
  console.log("greater");
  break;
  case  a<b:
  console.log("Less than");
  break;
  default:
  console.log("equal");
  break;
}
```

## Loops

### For

```
for(i=0;i<10,i==){

}
```

### While

```
while (i<0){

}
```

### Do While

```
do{

}
while i<10
```

do block executes once even if while block is not satisfied, only after first do execution condition on while is checked

### For In Loop

- Used to iterate with javascript Objects

```
let employee={
  "name":"bob",
  "salary":2000,
  "Tax":function(){
    console.log("tax")
  }
}

for(let key in  employee){
console.log(key)
}
key can be any thig
```

### For Of Loop

- Used to iterate with javascript Arrays

```
for(let key of employee){
console.log(key)
}
```

## Template Literals

- When strings are displayed if ` baptick is used insted of ' or " we can include dynamic values with ${}

```
let name ='bob'
console.log(`hi ${name}`)

```

## Import Export

- import and export data between files

```
file 1
export const a=10
or
export {a}

file 2
import {a} from "./file_path"

To import every thing

import * as name from "./path"
everything will be
```

Default export import (fall back export)

```
export default a
import a from "./path" (no {})

```

## This

- Reference to an object where it is used
- Does not work with arrow functions

```
const p1={
  name:"bob",
  sayhello:function(){
    console.log(`hello i am ${name}`)
  },
   sayhi:function(){
    console.log(`hi i am ${this.name}`)
  },
   saygreating:() => {
    console.log(`greetings i am ${this.name}`)
  }

}

p1.sayhello()       >>hello i am
p1.sayhi()          >>hi i am bob
p1.saygreating()    >>greetings i am (in this case it will be refernceing the window object)

```
## JSON
- JavaScript Object Notation (JSON) is a standard text-based format for representing structured data based on JavaScript object syntax
- It is commonly used for transmitting data in web applications
- light weight and easy to read
- Supports strings,numbers,boolean,null,array,objects

```
[
  {

  }
]
is allso valid json
```
- `JSON.parse(variable)` is used to convert a json which is passed as a string in to an object
- `JSON.stringify()` to convert to string

## DOM Manipulation
### Accessing Element
```
document.getElementById("id")
document.getElementByClassName("class")
document.getElementByTagName("tagName")
document.querySelector(".id") OR ("#class") OR ("tagname")
-->> access first item
-->> can access with id,class or tag names

document.querySelectorALL(".id") OR ("#class") OR ("tagname")
-->> access all items
```

### Append Items
#### Text

```
const body=documet.body
const div =documnet,createElemet("div")
div.innerText="hello" OR div.textContent="hello"
body.append(div)
```
#### Html (not recomanded for sequerity reasons)

```
const body=documet.body
const div =documnet,createElemet("div")
div.innerHTML="<h1>hello</h1>"
body.append(div)
```
### Remove
```
const a=document.querySelector("#a")
a.remove()
```

### Modify Element Attributes
```
const a=document.querySelector("#a")
a.getAttribute("title")

a.setAttritute("title","new_title")

a.removeAttribute("title")

```
### Modify Data Attributes
- Just like id and class used to represent a element used for javascript manupulations
- these attributes allow you to store custom data without any visual representation
- Stated with HTML5 aimed to seperate accessing elements from css and JS
- Should Start with `data-` after that you can put anything
`<span id='a" data-id="hello">hello</span>`
- can add multiple for a single element
```
list datasets for that element as keyvalue pairs

const a=document.querySelector("#a")
console.log(a.datset)

Create new

a.dataset.newName="hi"  >> <span id='a" data-id="hello" data-new-name='hi'>hello</span>
```
### Modify Class Attributes
```
const a=document.querySelector("#a")

a.classList.add("classname") >> add's
a.classList.remove("classname") >>removes
a.classList.toggle("classname") >>removes if allready presents else add's
a.classList.toggle("classname",true) >> add's or remove based on passed boolean
```

### Modify Styles
```
const a=document.querySelector("#a")
a.style.property=value
```

## Class
- class is used to create one or more objects
- class definition contain's what an object have (Instance Propertys) and what an object does (Instance Methode)
- Every class has a constructor 
- A constructor is a methode which is run once when the object is created,which is used to setup your object
- constructor contains propertys  and any other functions are method's

```
class Rectangle{
constructor(_width,_height){
  // this refers to current object,'_' is not necessary
this.width=_width;
this.height=_height;
}
getArea(){
return this.width*this.height
}
}

//creating an object with class
let myRectangle =new Rectangle(4,5)
// executing the methodes
myRectangle.getArea()
```
### Getter and setter

