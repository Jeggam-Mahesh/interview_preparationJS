## Q1. Difference between “ == “ and “ === “ operators.
  ans:

  The == operator performs a loose equality comparison that performs type coercion if necessary to make the comparison possible. The === operator, on the other hand, performs a strict equality comparison that does not perform type coercion and requires the operands to have the same type (as well as the same value)

    let a = 5;
      let b = "5"; <br>
      console.log(a == b); // true <br>
      console.log(a === b); // false

## Q2.What are the differences between var, let and const?
  ans:

  var is a global scoped means variables created using var keyword will be accessible globally. It
can be redeclared and reinitialized.

    var a = 10;

let is a block scoped means variables created using let keyword will be accessible only in that
specific block where it has been declared. It cannot be redeclared but it can be reinitialized.

    let a = 20;

const is also block scoped means variables created using const keyword will be accessible only
in that specific block where it has been declared. It cannot be redeclared and cannot be
reinitialized.

     const a = 30

## Q3.What is hoisting?

ans:

Hoisting is a JavaScript mechanism where variables and function declarations are moved to the
top of their scope before code execution. Remember that JavaScript only hoists declarations,
not initialisation. Let's take a simple example of variable hoisting. Let and const keywords are
not hoisted so when you try to access them before initialization they start giving you Reference
error

    console.log(msg); //output : undefined
     var msg = 'The variable Has been hoisted';

## Q4.What is a Temporal Dead Zone?

 ans:

 The Temporal Dead Zone is a behavior in JavaScript that occurs when declaring a variable
with the let and const keywords, but not with var. In ECMAScript 6, accessing a let or const
variable before its declaration (within its scope) causes a ReferenceError. The time span when
that happens, between the creation of a variable’s binding and its declaration, is called the
temporal dead zone.

    Let's see this behavior with an example,
    function somemethod() {
     console.log(counter1); // undefined
     console.log(counter2); // ReferenceError
     var counter1 = 1;
     let counter2 = 2;
    }
## Q4.What is meant by first class functions?

ans:

A programming language is said to have First-class functions when functions in that language
are treated like any other variable. For example, in such a language, a function can be passed as
an argument to other functions, can be returned by another function and can be assigned as a
value to a variable.

    const temp = function() {
    console.log("Hello World !!");
    }
    temp();
    Output: Hello World !!
//another example:

    function sayHello() {
     return "Hello, ";
    }
    function greeting(helloMessage, name) {
     console.log(helloMessage() + name);
     }
    // Pass “sayHello” function as an argument to “greeting” function
    greeting(sayHello, "JavaScript!");
    Output: Hello, JavaScript!

## Q5.What are pure functions?
ans:

Pure Function is a function (a block of code ) that always returns the same result if the same
arguments are passed. It does not depend on any state, or data change during a program’s
execution rather it only depends on its input arguments.

Let’s see the below JavaScript Function

    function calculateGST( count ) {
    return count* 0.05;
    }

The above function will always return the same result, if we pass the same productPrice. In
other words, it’s output doesn’t get effected by any other values / state changes. So we can call
“calculateGST” function as a Pure function

   
  