# Testing Facebook Account Creation with Cypress.io
This repository demonstrates the ability to automate UI tests using Cypress.io. The intent is to show the ease of writing tests, debugging tests and running tests with Cypress.io.

More info about Cypress can be found at their website: https://www.cypress.io/

## Why Cypress?
The following are my top reasons for using Cypress over Selenium Webdriver:
* Has screenshots and video recording tests built into the framework. It will auto screenshot each step of the test as well as the failure point if there is one.
* Has automatic sleeps built into the framework. When attempting to grab a DOM object, it will auto sleep until the object is available or the test will timeout
* Since it is built around Mocha, you are able to immediately use Mocha features built in, such as pre built reporters or custom reporters.

Selenium WebDriver can provide the same capabilities as Cypress, but they are not built into WebDriver. You will need to recreate these features or integrate third party libraries. With each implementation you will need to overcome challenges of flakiness or changing DOM objects when having a dynamic UI. Cypress gives us all these features and more built into its framework.

https://docs.cypress.io/guides/overview/why-cypress.html#Our-mission

## Running Cypress
Another great feature that comes with Cypress is the test runner. When running tests locally it provides a runner that gives detailed information about the tests being run, allowing you better debugging into why your tests are failing and what Cypress is actually seeing when the tests run.

### Install and Run Cypress 
You can install Cypress with node: 

`npm install cypress --save-dev`
 
From the root of this project, run the following command:

`npx cypress run`

To run and have a report of the results generated (example is in junit format)

`npx --reporter junit --reporter-options "mochaFile=results/my-test-output.xml,toConsole=true"`

If you want to run from the test runner:

`npx cypress open`

This will open up the runner and the runner will rerun when you make any hot changes locally to the tests.
Another added feature with the runner is that it has an element select mode. In this mode you can click on any element and it will provide you with the best selector to use to access that element in the test.
 
## API Testing with Cypress
Cypress also has the ability to do API testing built into the framework. Examples coming soon
