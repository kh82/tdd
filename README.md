# [AngularJS for Test-Driven Development][published url]
## Instructor: [Daniel Stern][instructor url]


Angular.js is one of the most widely-used web frameworks today. Part of what makes Angular so amazing is that it is a framework written from the ground up with testing in mind. In this course, we'll take a practical, hands-on approach to using Angular.js to its full testing capabilities.

You will how to build an app that's effectively tested, how to write effective tests, and we'll take a detailed look at running tests automatically. Automated tests allow us to write code that is more reliable, more effective and easier to maintain.

In order to test Angular properly, you need to be familiar with a variety of libraries, many from the Angular team. This course will familiarize you with all the testing frameworks you need to know about to test Angular - Mocha, Chai, Protractor, Karma and more.

## Source Files Description

This repository contains an example of an AngularJS app built with running tests in mind. Snapshots of the code as it exists before and after each lesson are also available in named repository branches.

You can clone this repository and use it as a basis for your app, or use it to learn about Test-Driven Development with Angular.

## Usage

1. Clone or unzip the Git repository to your workstation.
2. Install dependencies with `npm install; bower install`
3. Install Karma dependencies globally with `npm install -g karma karma-cli karma-protractor karma-coverage istanbul webdriver-manager mocha`
4. Run the application using the instructions in the Gulp section.

### Directory Structure

```
  /app/ 												// where our app is
	 --/scripts/  								// location of our app logic
	 --/index.html
 	/test/ 												// tests files
	 --/coverage/									// generated folder by istanbul
	 --/e2e/ 											// end to end tests
	 --/spec/ 										// unit tests for app
	 --/protractor.config.js/  		// set up for protractor
	 --/server.spec.js/   				// server unit tests
	/karma.conf.js								// karma setup
```

### Gup Tasks Helper
#### Run tests and serve
To run tests and then serve if the tests pass, run `gulp` (default task)

#### Generate and Serve Code Coverage Metrics
To generate and then view your code coverage report, run `gulp coverage`

#### To Serve and debug tests
Tests can be debugged in the browser by serving them with `gulp serve-test`

#### To run end-to-end tests with protractor
To automatically run Selenium and run your e2e tests, run `gulp protractor`

#### To run automated browser tests with Karma
To run all unit tests in every configured browser, run `gulp test-browser`

#### To run all tests one after the other
To run each tests suite without them conflicting, run `gulp test`

#### To test the Express server
To test the express server, run `gulp test-server`

#### To serve the app
To serve the app, run `gulp serve` (also runs tests)


## Glossary

### Jasmine
> DOM-less simple JavaScript testing framework

A test runner/assertion/mocking utility combination.

Use: Run tests, write assertions and mock functionality.
Compare To: Mocha+Chai

### Mocha
Just a test runner. Often used in combination with an assertion library (see Assert, Chai)
Compare to: Jasmine

### Karma
> The main goal for Karma is to bring a productive testing environment to developers. The environment being one where they don't have to set up loads of configurations, but rather a place where developers can just write the code and get instant feedback from their tests.

Karma is a browser test runner.

The idea is that browsers do not have natively a concept of loading tests files, running them, and reporting results. What Karma does is (roughly):

- Start a small web server to serve "client-side" JavaScript files to be tested (1)
- Also serve the "client-side" JavaScript files with the tests (or Specs, as they're often called) (2)
 -serve a custom web page that will run JavaScript code for the tests (3)
- Start a browser to load this page (4)
- Report the results of the test to the server (5)

Karma can then report the results to text files, the console or anything your CI server likes.

Use: Karma can be used to run your tests in browsers. If your tests are simple JavaScript that would run the same in Node as in Chrome, this is not necessary, but if you wish to support Firefox, Chrome, IE, et al, in your tests, Karma lets you do it, via a configuration file.

### Gulp
Use: Automate tasks.
Environment: Command Line / JavaScript
Compare to: Grunt, Broccoli

### gulp-karma
Use: Simplify automation of running Karma in Gulp
Environment: `require` this library in a gulpfile
Compare to: gulp-jasmine

### Supertest
A framework specifically for running tests on servers created by Express or similar APIs.
Use: Require supertest in your test script and have it run tests on your Server script
Compare to: Request.js

### Istanbul
A tool for measuring how much of your code has tests covering it.


### angular
MVC Framework.
Use: Build single-page apps or augment static apps
Compare to: Ember, React

### angular-mocks
A library necessary to run tests on your angular app. Has an e2e version that can only be run on the backend.
Use: Include the script on your page to gain access to `inject` and `module`

### protractor
A library for running end-to-end tests on angular apps. protractor uses selenium/webdriver, which are two big words.
Use: Test high level functionality like database interaction and navigation

### Chai
Assertion framework. Allows assertions to be written in `expect.to.be` form. Adds additional assertions to `assert` library.
Use: Write assertions in a descriptive way
Compare to: assert

### assert
A library built in to Node that can run certain assertions.
Use: Use to write tests that can throw errors if code returns unexpected results.
Compare to: Chai

------

These are source files for the Tuts+ course: [AngularJS for Test-Driven Development][published url]

Available on [Tuts+](https://tutsplus.com). Teaching skills to millions worldwide.

[published url]: https://code.tutsplus.com/courses/angularjs-for-test-driven-development
[instructor url]: https://tutsplus.com/authors/daniel-stern
