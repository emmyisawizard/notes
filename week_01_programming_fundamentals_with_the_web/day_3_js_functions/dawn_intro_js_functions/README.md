#Functions
## Objectives

| Objective |
| :--- |
| Students should be able to create simple Javascript functions with parameters|
| Students should be able to explain what returning a value means and how it differs with printing a value|
| Students should know what it means for a function to have scoped variables |



##Defining a function
```
var greeting = function() {
console.log("Hello World");
};

greeting();
```

##Defining a function with a parameter
```
var greeting = function (taco) {
  // anything inside of here will execute when called
  console.log("Good morning", taco);
};

var name = "Delmer";
var name2 = "Brett";
greeting(name);
greeting(name2);
```


##Why use functions?

###Let's greet some instructors

```
var instructor = "Brett";
console.log("Hello", instructor); // Hello Brett

instructor = "Delmer";
console.log("Hello", instructor); // Hello Delmer
```

###Or we could greet some students
```
var student = "Alexandra";
console.log("Hello", student);  // Hello Alexandra

student = "Emanuel";
console.log("Hello", student); // Hello Emanuel
```

###So what does this have to do with functions?

The question we should be asking is: Did we repeat ourselves in our code?
```
var greeter = function(person) {
  // We can avoid re-writing the same code by placing that code inside of our function
  console.log("Hello " + person + "!"); 
};

// Now let's greet some people.
greeter("Brett");
greeter("Alexandra");

```

Generalizing code inside of a procedure is called "abstraction"


##Defining a function with two parameter
```
var greeting = function (taco, stuff) {
  // anything inside of here will execute when called
  console.log("Good morning", stuff, taco);
  console.log("taco:", taco);
  console.log("stuff:", stuff);
};

var name = "Delmer";
var name2 = "Brett";
greeting(name, name2);
greeting(name2, name);
```

##Printing and returning are diffrent
```
var multiply = function(num1, num2) {
  console.log("inside the function");
  // return result = num1 * num2;
  return num1 * num2
};

var firstNum = 2;
var secNum = 3;
var taco = multiply(firstNum,secNum);

console.log(firstNum + " multiplied by " + secNum + " is " + taco );
```
```
// With a return value
var returnHello = function (name) {
  return("Hello, " + name);
};

console.log("with a return value:", returnHello("tim") );

// Without a return value
var returnHello2 = function(name) {
  console.log("inside returnHello2: Hello, " + name);
};
returnHello2("nachos");
console.log("without a return value:", returnHello2("taco") ); //will show as undefined
```

##A function with scoped variables
```
var scoped = function(name) {
	var greeting = "Hello " + name + "!";
	return greeting;
};

var hello = scoped("Michael");
console.log(hello);
```

###Exercise
Write a function that reverses a string.

Write a function to solve FizzBuzz

Rewrtie all the exercises from the previous days homework as functions instead of files.
