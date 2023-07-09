# WDIO-Course


To run your tests: **npm run wdio**


## **Content for WebdriverIO course**

### **What is WebdriverIO?**

WebdriverIO is an open-source e2e (End-to-End) test automation utility for nodejs. It lets you control a browser or a mobile application with just a few lines of code. It makes it possible to write super easy selenium tests with Javascript in your favorite BDD or TDD test framework.

It basically sends requests to a Selenium server via the WebDriver Protocol and handles its response. These requests are wrapped in useful commands and can be used to test several aspects of your site in an automated way.
https://www.w3.org/TR/webdriver/

Terminal Commands:




**What are the pros and cons of WebdriverIO?**

**Pros:**

WebDriverIO is a custom implementation of W3C webdriver API. This gives it an edge to have full control over implementation rather than depending on WebDriverJS implementation.

*It is fully extensible and is written to be as flexible and framework agnostic as possible. It can be applied in any context and serves not only the purpose of testing.

*Easy to use: The API is close to Selenium’s and has a simple way of constructing objects. The API was also designed so that you can write tests in a more readable way, which is better for most of the developers that don’t know JavaScript but need to build tests with JavaScript.
  
*It has a command line interface wdio which makes test configuration as easy and simple as possible so that a non-programmer can configure the setup.

*Allows multi-use: WebdriverIO has a Node package that makes it easy to use in all your JavaScript projects. You can use the framework on your web, mobile, desktop, or API endpoints.
Can test on multiple browsers and native apps at the same time

*It has good support, an enthusiastic developer community, and end users, giving it an edge over Selenium.

*It can be used with webdriver css to compare css stylings of an element in the webpage.\

*Faster


**Cons:**

*It doesn’t use features like classes or modules.

*Lack of infrastructure: The API is very simple and doesn’t have complex facilities like watchers, listeners, and so forth. 

*It’s hard to know what some of the more complicated functions and classes do. With WebdriverIO, you’re limited to writing tests using TypeScript or JavaScript, and because of that, as a developer and tester, you need to have at least a basic understanding of JavaScript.

**Overview of WebDriver:**

WebDriver is a general-purpose library for automating web browsers. It was started as part of the Selenium project, which is a very popular and comprehensive set of tools for browser automation, initially written for Java but now with support for most programming languages.

**Architecture:**
All software runs on your local computer:

<img width="631" alt="image" src="https://github.com/ndkramer/WDIO-Course/assets/7460198/a1a259ff-eeb5-4db3-97cf-0ea635106d93">


*node.js (see below) runs Cucumber or Mocha framework and runner of test script.

*Expect and\or Chai is the assertion library.

*Web Driver IO communicates with Selenium Server using JSON Wire Protocol.

*Selenium Server invokes a local browser using a driver to test the web application.

## **node.js:**
Node.js is an open-source, cross-platform, back-end JavaScript runtime environment that runs on the V8 engine and executes JavaScript code outside a web browser.

Here's a simpler way to understand it:

1. **Open-source**: This means that Node.js is free to use and its source code is accessible to everyone. Developers from around the world contribute to its development.
2. **Cross-platform**: Node.js can run on various platforms like Windows, Linux, Unix, Mac OS X, etc. This makes it versatile and widely used.
3. **Back-end JavaScript runtime environment**: Traditionally, JavaScript could only be run in the browser (front-end). But with Node.js, you can now write server-side code using JavaScript. This means you can create, read, update, and delete files on the server, connect to databases, and much more.
4. **Runs on the V8 engine**: The V8 engine is Google's open-source high-performance JavaScript and WebAssembly engine. It's what Chrome uses to run JavaScript, and Node.js uses it too.
5. **Executes JavaScript code outside a web browser**: This means you can write command line tools and for server scripting to produce dynamic web page content before the page is sent to the user's web browser.
In essence, Node.js allows you to use JavaScript for more than just making websites interactive. With it, you can build entire servers and do a lot of other powerful things!






