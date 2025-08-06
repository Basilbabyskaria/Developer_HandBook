# Data Types
* Primitive Data Types - Null,Undefined,Number,String,Bigint,Boolean,Symbol  
* Reference - Objects  
* All primitive datatypes except for null can be tested using `typeof` operator,`typeof(null)` returns object so `===` is used to check for null.

## Null,Undefined
`undefined` indicates the absence of a value, while `null` indicates the absence of an object (which could also make up an excuse for typeof null === "object")

## Boolean 
True or False

## Numbers 
It is capable of storing positive floating-point numbers between 2<sup>-1074</sup> (Number.MIN_VALUE) and 2<sup>1023</sup> × (2 - 2<sup>-52</sup>) (Number.MAX_VALUE) as well as negative floating-point numbers of the same magnitude, but it can only safely store integers in the range -(2<sup>53</sup> − 1) (Number.MIN_SAFE_INTEGER) to 2<sup>53</sup> − 1 (Number.MAX_SAFE_INTEGER). Outside this range, JavaScript can no longer safely represent integers; they will instead be represented by a double-precision floating point approximation. You can check if a number is within the range of safe integers using Number.isSafeInteger().  
* Positive values greater than Number.MAX_VALUE are converted to Infinity.
* Positive values smaller than Number.MIN_VALUE are converted to 0.
* Negative values smaller than -Number.MAX_VALUE are converted to -Infinity.
* Negative values greater than -Number.MIN_VALUE are converted to -0.

## NaN 
("Not a Number") is a special kind of number value that's typically encountered when the result of an arithmetic operation cannot be expressed as a number. It is also the only value in JavaScript that is not equal to itself.

## BigInt 
The BigInt type is a numeric primitive in JavaScript that can represent integers with arbitrary magnitude. With BigInts, you can safely store and operate on large integers even beyond the safe integer limit (Number.MAX_SAFE_INTEGER) for Numbers.

## 