# WDIO-Course
**Content for WebdriverIO course**

**What is WebdriverIO?**

WebdriverIO is an open-source e2e (End-to-End) test automation utility for nodejs. It lets you control a browser or a mobile application with just a few lines of code. It makes it possible to write super easy selenium tests with Javascript in your favorite BDD or TDD test framework.

It basically sends requests to a Selenium server via the WebDriver Protocol and handles its response. These requests are wrapped in useful commands and can be used to test several aspects of your site in an automated way.
https://www.w3.org/TR/webdriver/

Terminal Commands:

To run your tests: **npm run wdio**


**What are the pros and cons of WebdriverIO?**

**Pros:**

WebDriverIO is a custom implementation of W3C webdriver API. This gives it an edge to have full control over implementation rather than depending on WebDriverJS implementation.

*It is fully extensible and is written to be as flexible and framework agnostic as possible. It can be applied in any context and serves not only the purpose of testing.

*It has a command line interface wdio which makes test configuration as easy and simple as possible so that a non-programmer can configure the setup.

*It has support for most BDD and TDD test frameworks.

*It has good support and enthusiastic developer community and end users which gives it an edge over NightwatchJS.

*It can be used with webdriver css to compare css stylings of an element in the webpage.

**Cons:**

*It can be used for automating AngularJS apps but it is not as customized as Protractor.

*It doesn't have the full support of xPath like as NightwatchJS.

*Since it is a custom implementation, it is also a disadvantage as it deviates from generic syntax which may confuse selenium developers coming from other languages.

**Overview of WebDriver:**

WebDriver is a general-purpose library for automating web browsers. It was started as part of the Selenium project, which is a very popular and comprehensive set of tools for browser automation, initially written for Java but now with support for most programming languages.

**Architecture:**
All software runs on your local computer:

<img width="631" alt="image" src="https://github.com/ndkramer/WDIO-Course/assets/7460198/a1a259ff-eeb5-4db3-97cf-0ea635106d93">


*Node runs Cucumber or Mocha framework and runner of test script.

*Expect and\or Chai is the assertion library.

*Web Driver IO communicates with Selenium Server using JSON Wire Protocol.

*Selenium Server invokes a local browser using a driver to test the web application.






