# Playwright Notes

## Playwright CLI

Run in headed mode:

* npx playwright test --headed

Run browser specific test

* npx playwright test --browser=firefox

Run browser specific test

* npx playwright test --headed --browser=firefox

Run all the browsers

* npx playwright test --browser=all

Run specific test

* npx playwright test path/to/test.spec.ts

Run in debugg mode

* npx playwright test --debugg

Run a test with a tag

* npx playwright test --grep @myTagName

Run a test using a specific config

* npx playwright test --config=playwright.config.ts

Run a specific project in config

* npx playwright test --config=playwright.config.ts --project=Webkit

Run tests with reporter

* npx playwright test --config=playwright.config.ts --project=Webkit --reporter=line
* npx playwright test --config=playwright.config.ts --project=Webkit --reporter=list
* npx playwright test --config=playwright.config.ts --project=Webkit --reporter=dot
* npx playwright test --config=playwright.config.ts --project=Webkit --reporter=junit
* npx playwright test --config=playwright.config.ts --project=Webkit --reporter=html

## Playwright Click

await page.click('selector-as-value')

## Playwright Selectors

Text

* await page.clcik('text=Sign in')

CSS Selectors

* await page.clcik('button')
* await page.clcik('#idName')
* await page.clcik('.className')

Only visible CSS Selector

* await page.click('.submit-button:visible')

Combinations

* await page.click('#idName .className')

XPath

* await page.click('//button')

## Run tests in parallel

To run tests in paralel add the tests inside 'describe' block.

* test.describe.parallel('name', () => {})