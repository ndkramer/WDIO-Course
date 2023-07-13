# Comments
**Comment: Single line:**
//



**Block comment:**

/*

You can write multiple lines of comments here

*/


Note:
For VSCode you can also select the lines you want to comment and press
Ctrl + /

# ; (semi-colons)

The semicolon (;) in TypeScript and JavaScript is used to separate statements, but whether or not to use it is largely a matter of style and personal preference. 

Here are some best practices:
1. **Consistency**: Whether you choose to use semicolons or not, be consistent throughout your codebase. Mixing styles can lead to confusion and potential errors
2. **Automatic Semicolon Insertion (ASI)**: JavaScript has a feature called Automatic Semicolon Insertion that automatically inserts semicolons for you in most cases. However, there are some edge cases where ASI may not behave as expected, which could lead to bugs. If you choose not to use semicolons, make sure you understand these edge cases.
3. **When Using Tools**: Some JavaScript tools and libraries may require or recommend the use of semicolons. Always check the documentation of the tools you're using.
4. **Readability**: Some developers find that code is more readable with semicolons, especially when multiple statements are on the same line.
   
Here's an example of code with semicolons:
typescript
let name = 'John';
console.log(name);
And here's an example without semicolons:
typescript
let name = 'John'
console.log(name)

Both are valid, but the style you choose should be consistent throughout your codebase.

# Arrow Functions

Arrow functions provide a more concise syntax for defining functions. They also have the benefit of not having their own this context, which can be useful in certain scenarios.

   Example:
   
typescript
   const add = (a: number, b: number): number => a + b;
   
# Array Methods
JavaScript array methods like map, filter, reduce, etc., are very commonly used and are also available in TypeScript. These methods can be used to manipulate arrays in a functional programming style.
  
   Example:
   
typescript

   const numbers = [1, 2, 3, 4, 5];
   const doubled = numbers.map((num) => num * 2); // [2, 4, 6, 8, 10]
   
   
# Destructuring
Destructuring allows you to unpack values from arrays or properties from objects into distinct variables.

Note: "Unpack" in this context refers to the process of taking elements from complex data structures like arrays or objects and assigning them to individual variables.
   
   Example:
   
typescript

   const person = { name: 'John', age: 30 };
   
   const { name, age } = person; 
   
   // name = 'John', age = 30

   Here are a few reasons why you might want to use destructuring:
1. **Simplify Code**: Destructuring can make your code simpler and cleaner by reducing the need for repetitive access of properties in an object or elements in an array.
2. **Easily Handle Function Parameters**: If a function takes an object as a parameter, you can destructure the object right in the function parameters. This makes it clear what properties the function uses.
3. **Swap Variables**: Destructuring can be used to swap the values of two variables without needing a temporary variable.
   
# Template Strings
Template strings allow you to embed expressions within string literals using ${} syntax.
   
   Example:
   
typescript
   const name = 'John';
   const greeting = `Hello, ${name}!`; // 'Hello, John!'
   
   
# AWait
Await and Async/Await**: Await are used for asynchronous programming. async/await is a syntax sugar on top of Promises and makes asynchronous code look and behave a little more like synchronous code.
   
   Example:
   
typescript
   const getData = async () => {
     try {
       const response = await fetch('https://api.example.com/data');
       const data = await response.json();
       console.log(data);
     } catch (error) {
       console.error('Error:', error);
     }
   };
   

   
# Declaring Variables 
In TypeScript and JavaScript, there are three main ways to declare variables: **var, let, and const.**

**1. var:** This is the oldest way to declare variables. It's function-scoped, which means a variable declared with var is accessible within the function it's declared in.
   Reason to use: If you need a variable that's accessible throughout the entire function, regardless of block scope, you might use var. However, var is generally avoided in modern JavaScript and TypeScript due to its confusing scoping rules.
   
   Example:
   
typescript

   function testVar() {
   
     var x = 1;
     
     if (true) {
       var x = 2;  // Same variable!
       console.log(x);  // 2
       
     }
     console.log(x);  // 2
     
   }
   
**2. let:** This is a block-scoped variable declaration. A variable declared with let is only accessible within the block it's declared in, as well as any nested blocks.

   Reason to use: If you need a variable that can be reassigned and is only accessible within a certain block (like a loop or an if statement), you would use let.
   Example:
   
typescript

   function testLet() {
   
     let x = 1;
     if (true) {
       let x = 2;  // Different variable
       console.log(x);  // 2
     }
     console.log(x);  // 1
   }
   
**3. const:** This is also block-scoped, but it's used for constants, i.e., values that won't be reassigned.

   Reason to use: If you have a value that won't change, you should use const. This makes your code more predictable and easier to understand.
   Example:
   
typescript

   function testConst() {
   
     const x = 1;
     console.log(x);  // 1
     // x = 2;  // Error! You can't reassign a constant.
   }
   
Remember, it's generally recommended to always use const by default, and only use let when you know a variable needs to be reassigned. Avoid using var in modern JavaScript and TypeScript.

# Early Return
In TypeScript, as in JavaScript, it's often recommended to use the "early return" pattern instead of deeply nested if-else statements. This can make your code more readable and maintainable. Here's an example:

typescript

function processNumber(num: number): string {

  // Early return if the number is less than 10
  
  if (num < 10) {
  
    return 'Number is less than 10';
    
  }


  // If the number is between 10 and 20
  
  if (num >= 10 && num <= 20) {
  
    return 'Number is between 10 and 20';
    
  }

  // In all other cases
  
  
  return 'Number is greater than 20'
  
}


In this example, each condition returns early if it's met. This avoids the need for else or else if clauses. It's also clear what condition each return statement corresponds to, making the code easier to understand.
However, there are situations where traditional if-else statements or switch-case statements might be more appropriate, depending on the complexity of your conditions and what you find most readable.

# IF-Else:
An if-else statement is necessary when you have multiple conditions that need to be checked sequentially, and each condition corresponds to a different course of action. If-else statements are also useful when there's a default action that should be taken if none of the conditions are met.

Here's an example:

typescript

function getWeatherActivity(weather: string): string {

  if (weather === 'sunny') {
  
    return 'Go for a walk';
    
  } else if (weather === 'rainy') {
  
    return 'Read a book';
    
  } else if (weather === 'snowy') {
  
    return 'Build a snowman';
    
  } else {
  
    // Default case if none of the above conditions are met
    
    return 'Watch TV';
    
  }
  
}

In this example, the function checks the weather and suggests an activity based on it. If the weather is sunny, it suggests going for a walk. If it's rainy, it suggests reading a book. If it's snowy, it suggests building a snowman. If the weather is anything else, it defaults to suggesting watching TV. This is a case where an if-else statement is appropriate because there are multiple conditions with different actions associated with each one.


# Switch Case Statements:
A switch-case statement is useful when you have a single variable or expression, and you want to perform different actions based on its value. It's often used as a more readable alternative to if-else statements when there are many conditions.

Here's an example:

typescript

function getWeatherActivity(weather: string): string {

  switch (weather) {
  
    case 'sunny':
    
      return 'Go for a walk';
      
    case 'rainy':
    
      return 'Read a book';
      
    case 'snowy':
    
      return 'Build a snowman';

    default:
    
      // Default case if none of the above conditions are met
      
      return 'Watch TV';
      
  }
  
}


In this example, the function checks the weather and suggests an activity based on it. The switch-case statement is more concise and arguably more readable than the equivalent if-else statement, especially as the number of conditions increases.




# ? (Optional Parameters and Properties)
In TypeScript, function parameters and object properties can be marked as optional with the ? symbol. 
This means they may or may not be provided.

   Example:
   
typescript
   function greet(name?: string) {
     // ...
   }

# ' ' vs " " (Single vs Double Quotes)

In TypeScript, there is no difference between single quotes (') and double quotes ("). Both can be used interchangeably to define string values. The choice between the two often comes down to personal preference or coding style guidelines.

Here are examples of both:

typescript
let singleQuotedString = 'Hello, world!';
let doubleQuotedString = "Hello, world!";

Both singleQuotedString and doubleQuotedString are valid and equivalent.

However, it's important to be consistent in your usage of quotes. Mixing single and double quotes in the same project can lead to confusion and make your code harder to read. Some teams or projects may have a preferred style, so always check if there are any established guidelines you should follow.





