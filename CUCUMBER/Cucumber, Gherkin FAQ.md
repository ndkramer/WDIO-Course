<img width="665" alt="image" src="https://github.com/ndkramer/WDIO-Course/assets/7460198/9814d32c-0fd7-407a-b18d-eeb3e35621ce">




**5 Best Practices for Feature Files**
1. Use descriptive and concise feature names: Choose a clear and meaningful name for your feature that accurately represents the functionality being tested.
2. Write scenarios using Gherkin syntax: Use Given-When-Then format to define the steps of your scenarios. Start with a Given step to set up the initial state, followed by a When step to describe the action being performed, and finally, a Then step to define the expected outcome.
3. Keep scenarios independent and focused: Each scenario should test a specific behavior or functionality in isolation. Avoid creating scenarios that depend on the outcome of previous scenarios.
4. Use scenario outlines for data-driven testing: If you have multiple sets of test data to validate the same behavior, use scenario outlines to define a template scenario and provide different inputs using examples.
5. Use meaningful and readable step definitions: Write step definitions that are easy to understand and maintain. Use clear and descriptive names for your step definitions to improve readability.


**5 Best Practices for Step Definition Files**
1. **Keep It Simple**: Step definitions should be simple and clear. Avoid complex logic in your steps. If a step requires more complexity, consider breaking it down into multiple simpler steps.
2. **Reusability**: Write your step definitions so they can be reused across different scenarios. This reduces code duplication and makes your tests easier to maintain.
3. **Use Descriptive Names**: The names of your steps should clearly describe what they do. This makes your tests easier to read and understand.
4. **Parameterization**: Use parameters in step definitions whenever possible. This allows you to reuse the same step with different data.
5. **Organize Your Steps**: Group related steps into separate files or classes. This makes your step definitions easier to find and maintain.


**1) Can have multiple Scenario Outlines in the same feature file in WebDriverIO. :white_check_mark:
Here's a brief example to illustrate this:**

Feature: Multiple Scenario Outlines

  Background:
    Given I am on the homepage

  Scenario Outline: Scenario 1 - Check different elements
    When I check the element "<element>"
    Then the element should be visible

    Examples:
      | element   |
      | #header   |
      | #footer   |

  Scenario Outline: Scenario 2 - Search for different keywords
    When I enter the keyword "<keyword>" in the search box
    And I click the search button
    Then I should see the search results page

    Examples:
      | keyword   |
      | shoes     |
      | clothes   |
In this example:
- There are two Scenario Outlines (Scenario 1 and Scenario 2) within the same feature file.
- Each Scenario Outline has its own "Examples" table to define the data sets for that scenario.
This way, you can create and manage multiple Scenario Outlines in a single feature file while keeping your tests well-organized and easy to understand.


**2) You can use if-else statements in a step-definition file when working with WebdriverIO and TypeScript. Step definitions are just regular JavaScript/TypeScript functions, so you can use any control structures available in the language.
Here's an example of using an if-else statement in a step-definition file:**
typescript
import { Given, When, Then } from "@cucumber/cucumber";
import { expect } from "chai";

Given("I am on the home page", async function () {
  await browser.url("/");
});

When("I click on the {string} button", async function (buttonText: string) {
  const button = await $(`//*[text()='${buttonText}']`);
  await button.click();
});

Then("I should see the {string} message", async function (expectedMessage: string) {
  const actualMessage = await $("div.message").getText();

  if (expectedMessage === "Welcome") {
    expect(actualMessage).to.include(expectedMessage);
  } else {
    expect(actualMessage).not.to.include(expectedMessage);
  }
});
In this example, we're using an if-else statement inside the Then step definition to handle different expectations for the displayed message.

**3) Can you have more than one Scenario outline in a Feature File?**

   Yes, a feature file in Cucumber can contain more than one Scenario Outline. Each Scenario Outline provides a parametrized scenario script that is executed for provided examples.

**4) Can you have more than one feature file contain more than one 'Feature' section ?**

   5) Yes, a feature file in Cucumber can technically contain more than one feature. However, it's considered best practice to keep each feature in its own feature file for better organization and readability. Each feature file should ideally represent a single functionality or aspect of the application you're testing.

   
