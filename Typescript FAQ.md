**1) Here are some key differences between TypeScript and JavaScript:
TypeScript is a superset of JavaScript, which means that it extends the capabilities of JavaScript by adding optional static typing and other features. TypeScript was developed by Microsoft to improve the development experience for large-scale applications and to provide better tooling and error checking.**

1. **Static typing**: :memo:
   - TypeScript allows you to declare variable types, making it easier to catch type-related errors before they occur during runtime.
   - JavaScript is a dynamically typed language, meaning variable types are determined at runtime.
2. **Class-based Object-Oriented Programming (OOP)**: :books:
   - TypeScript supports class-based OOP with inheritance, interfaces, and visibility modifiers like public, private, and protected.
   - While JavaScript also supports OOP through prototypes, it doesn't have native support for these additional features.
3. **Interfaces**: :handshake:
   - TypeScript introduces interfaces, which help define the structure of an object and ensure that specific properties or methods are present.
   - JavaScript doesn't have built-in support for interfaces.
4. **Type inference and type annotations**: :mag_right:
   - TypeScript can automatically infer types from the code and allows you to explicitly specify types using type annotations.
   - JavaScript doesn't have built-in support for type inference or type annotations.
5. **Compiler**: :hammer_and_wrench:
   - TypeScript has a compiler that compiles TypeScript code into plain JavaScript code.
   - JavaScript doesn't require a compiler.
6. **Tooling and IDE support**: :computer:
   - TypeScript provides better tooling and IDE support with features like autocomplete, refactoring, and error checking.
   - JavaScript has limited tooling and IDE support in comparison.
In summary, TypeScript enhances JavaScript by introducing optional static typing, better OOP support, interfaces, and improved tooling. This makes TypeScript more suitable for large-scale applications that require better error checking and maintainability.


**2) When writing JavaScript code (Textframe supports JavaScript), there are two main keywords used to declare variables: let and const. Here is the difference between them:**
1. let:
   - It is used to declare a variable that can be reassigned.
   - It has block scope, which means it is only accessible within the block where it is defined.
   Example:
   
   let counter = 0;
   counter = 1; // This is valid, as 'let' allows reassignment
   
2. const:
   - It is used to declare a constant variable, whose value cannot be changed once assigned.
   - It also has block scope, like let.
   - It must be initialized with a value when declared.
   Example:
   
   const PI = 3.14159;
   PI = 3.14; // This will throw an error, as 'const' does not allow reassignment
   
In summary, use let for variables that need reassignment and const for variables that should remain constant throughout the code.

**3)  In TypeScript, {} and [] are used to represent different data structures:**
1. {} - Curly braces represent an object:
   * An object is a collection of key-value pairs (properties).
   * Keys are strings, and values can be any data type.
   * Example: { key1: 'value1', key2: 42 }
2. [] - Square brackets represent an array:
   * An array is an ordered list of elements.
   * Elements can be any data type.
   * Example: [1, 'string', { key: 'value' }]
Here's a summary:
:sparkles: Objects:
* Syntax: {}
* Structure: Key-value pairs
* Example: { firstName: 'John', lastName: 'Doe' }
:sparkles: Arrays:
* Syntax: []
* Structure: Ordered list of elements
* Example: [1, 2, 3, 4]
