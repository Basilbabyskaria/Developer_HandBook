# Lexical Structure

## Lexical grammar
 Javascript source text (Over code) is just a sequence of characters.In order for the interpreter to understand this it is parsed into a more structured representation  
 
 * The Text get's scanned from left to right and is converted into sequence of indivitual and automic elements 
 * Input element's like comments and spaces are insignificant and are stripped off
 * Elements like identifiers, keywords, literals, and punctuators (mostly operators) willbe
 * Line Terminators and multiline comments are allso insignificat but are used fir automic semicolon insertion

 ## Format-control characters (escape sequences)
 They have no visual representaion but are used to control the interpretation of texts 

 
 [//]: <> (Check web confused at the moment ,something to do with displaying arabic and similar words. )

 ## Comments

 line : `//`  
 MultiLine : `/* */`  
 Hashbang : `#!`  
 Just like Shebang in unix Hashbang is used in JS to specify the path to the interpreter in which the code should be executed. it is only taken i to account when the code is directly run in shell other wise it behaves like a normal line comment  
 eg: `#!/usr/bin/env node`  

 ## Identifiers
 Used to link a value to a name ,Variables and function Names for example

 ```
const decl = 1; // Variable declaration (may also be `let` or `var`)
function fn() {} // Function declaration
const obj = { key: "value" }; // Object keys
// Class declaration
class C {
  #priv = "value"; // Private field
}
lbl: console.log(1); // Label

 ```

* Identidiers are usually madeup of alphanumeric characters, `-` and `$`
* First letter should not be numeric
* Unicode code characters are allso allowed 
* Reserved words are not allowed

## Keyword 
* They look like identifiers but have a special meaning to them 
* some keywords are reserved
* eg  async ,await etc

## Reserved Words

[//]: <> (will get back to this)