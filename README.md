Introduction:
Reusable Page Object Model framework for automating any web projects using Selenium Cucumber JVM.

Pre-requisites
•	Java
•	Maven
•	Eclipse
•	Eclipse Plugins
o	Maven
o	Cucumber
Setting up Project
•	Install JDK 1.8+ (make sure Java class path is set)
•	Install Maven  (make sure .m2 class path is set)
•	Clone respective repository or download zip.
o	https://github.com/selenium 
•	Clone the project from git
•	Launch Eclipse
•	click on File -> Import
•	Select Maven -> Existing Maven Projects and click on Next button
•	Click on Browse and navigate to git directory and select folder
o	Select pom.xml and click on finish button
Download chromedriver https://sites.google.com/a/chromium.org/chromedriver/downloads
Browser driver (make sure you have your desired browser driver and class path is set)
Maven
To run the tests on Google Chrome:

ChromeDriver
Set a system variable of "webdriver.chrome.driver" to point to the file downloaded above, either permanently or as part of running Maven: mvn test -Dwebdriver.chrome.driver=path/to/chromedrive
Building Project 
•	Goto project directory.
Use "mvn clean install" command to build the project.
Running features
Open command prompt and navigate to the project directory and type mvn clean test command to run features
Steps
•	Goto project directory.
•	Use "mvn test" command to run features.
To run specific feature if you have multiple feature files use, 
mvn test -Dcucumber.options="classpath:features/my_first.feature"
 
Framework Description:
Automation tests are designed in Page Object Model over the top of cucumber framework.
src/test/resources:
Resources folder contains cucumber feature files, configuration files and browser drivers
•	create your BDD scenarios in features folder and are organize them with tags                example. "@regression", "@smoke", ” @functional”
•	TestConfig.properties file consists environment and accounts details for running tests on dev1 server
src/main/java:
This folder contains 2 packages pagemodel and utils.
•	Pagemodel package, we create classes consists of reusable functions performing specific test logic like login, search, etc.,
•	utils package we have AppProperties.java and ObjectRepository.java classes.
i.	ElementProperties class reads web element properties files and sets up tests to run on that particular environment.
ii.	In ObjectRepository class create Strings for all identified web elements in web application
src/test/java:
This folder contains packages Runner and feature
•	Runner package contains junit classes for running specific test suites.
•	step definitions for all features added in features folder are added in stepdefs package.
Executing Tests:
Running the tests - from IDE
Run src/test/java/cucumber_runners/TestRunner.java as maven test

1.	select TestRunner.java from Runner package under folder src/test/resource
2.	Click on Run menu option and select run as JUnit Tests



