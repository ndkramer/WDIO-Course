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
