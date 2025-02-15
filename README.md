# Spaced Repetition Project

## Welcome to the Space Repitition Language Learner

Space Repitition is a strategy for studying new material. It allows more frequently missed words to show up more often, and words that are translated correctly more often show up less and eventually not at all.

A user can make an account, and at which point can access their dashboard where they can see their progress as well as a word to translate. If the user gets it right they can move on to another word. A user can track their progress and see how close they are to completing the module. 

The Live website can be found here <site_after_deploy>

This project was created by Cristian & Kristof.

The frontend uses:
1. React
2.  Cypress for testing


## Install

1. Fork and clone the project to your machine
2. `npm install`. This will also install the application *Cypress.io* for running browser integration tests

The project expects you have the Spaced repetition API project setup and running on http://localhost:8000.

Find instructions to setup the API here https://github.com/jamster10/space-api-cristian-kristof.

## Running project

This is a `create-react-app` project so `npm start` will start the project in development mode with hot reloading by default.

## Running the tests

This project uses [Cypress IO](https://docs.cypress.io) for integration testing using the Chrome browser.

Cypress has the following expectations:

- You have cypress installed (this is a devDependency of the project)
- You have your application running at http://localhost:3000.
  - You can change the address of this expectation in the `./cypress.json` file.
- Your `./src/config.js` is using http://localhost:8000/api as the `API_ENDPOINT`

To start the tests run the command:

```bash
npm run cypress:open
```

On the first run of this command, the cypress application will verify its install. Any other runs after this, the verification will be skipped.

The command will open up the Cypress application which reads tests from the `./cypress/integration/` directory. You can then run individual tests by clicking on the file names or run all tests by clicking the "run all tests" button in the cypress GUI.

Tests will assert against your running localhost client application.

You can also start all of the tests in the command line only (not using the GUI) by running the command:

```bash
npm run cypress:run
```

This will save video recordings of the test runs in the directory `./cypress/videos/`.
