<!-- TITLE: Testing -->
<!-- SUBTITLE: A quick summary of Testing -->


= What is Visual Regression Testing? =

* Visual Regression Testing (VRT) involves taking screenshots of ads or parts of ads, before and after a deployment. 
* A comparison is made between the before and after screenshots and any breaking changes are highlighted in an HTML report.
* Gemini code and an overview of the functionality is [https://github.com/gemini-testing/gemini here]([Category:QA]])
* Below are the main steps to set up your Mac for Automated Visual Regression Testing.


= Clone and install globally the Gemini Visual Regression Testing Framework project =

* clone https://github.com/gemini-testing/gemini
* npm install -g gemini


= Install drivers to run your browser(s) =

* Install local version of Selenium Server to be run for all browsers
    * npm install -g selenium-standalone
* Install Chromedriver in order to run tests with chrome
    * npm install -g chromedriver


= Run driver(s) before running Gemini tests =

* To test using Firefox you need to run the following before running the tests:
    * selenium-standalone start
* To test using Chrome or Chrome Headless you need to run 2 commands before running the tests:
    * selenium-standalone start
    * chromedriver --port=4444 --url-base=wd/hub


= Run the Gemini tests =

* To take "master" screenshots of the molecules or atoms in an ad run the following:
    * gemini update gemini/tests/              ('gemini/tests/' is the location of your tests)
* To take "comparison" screenshots of the molecules or atoms in an ad run the following:
    * gemini test --vreporter flat   ('vreporter' gives you verbose reporting)


= Gemini configuration =

* The .gemini.yml file should be in the root of your project
* In .gemini.yml you can set the following:
    * rootUrl (the URL of where the ads are built to)
    * tolerance (ie how much difference in the ad that Gemini will allow before flagging an issue)
    * browsers (including 'headless' option for Chrome)
* Further details of what is configurable [here](https://github.com/gemini-testing/gemini/blob/master/doc/config.md)


= package.json =
* Any extensions to gemini must be added to package.json in the 'gemini' folder
* e.g. 'html-reporter' extends Gemini


= Gemini tests =

* Gemini tests are written in Javascript
* The tests go in the gemini/tests folder
* They can be run using regular Chrome, Chrome Headless and Firefox


= Gemini HTML Reports =
* This is where you can see screenshot comparisons which highlight any changes between a "master" screenshot and the "latest" screenshot
* The location of the report is shown in the command line after the tests have run, e.g file:///Users/myuser/qa/my-project/test/gemini-tests/gemini-report/index.html
* install html-reporter
    * git clone https://github.com/gemini-testing/html-reporter
    * npm install html-reporter
