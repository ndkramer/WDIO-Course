**Comment: Single line:**
//



**Block comment:**

/*

You can write multiple lines of comments here

*/


Note:
For VSCode you can also select the lines you want to comment and press
Ctrl + /

#Early Return
In TypeScript, as in JavaScript, it's often recommended to use the "early return" pattern instead of deeply nested if-else statements. This can make your code more readable and maintainable. Here's an example:

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
  return 'Number is greater than 20';
}
In this example, each condition returns early if it's met. This avoids the need for else or else if clauses. It's also clear what condition each return statement corresponds to, making the code easier to understand.
However, there are situations where traditional if-else statements or switch-case statements might be more appropriate, depending on the complexity of your conditions and what you find most readable.

#IF-Else:
