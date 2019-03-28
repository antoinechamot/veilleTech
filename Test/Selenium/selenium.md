## Selenium

# What is selenium ?

Selenium is an automated testing suite for web based applications.It support multipe browsers (IE,chrome,firefox...)

# What are selenium components ?

 - Selenium Integrated Development Environment (IDE)
	-> Easy to use plugin for Firefox.
	-> Prototype tool only
	-> No advance test case
	
 - Selenium Remote Control (RC) = Selenium 1 :
    -> Rely on JavaScript for Automation
	-> Need a third party Server to run : slower than Webdriver and not very realistic
	-> automatically generates an HTML file of test results
	-> can readily support new browsers
	
 - WebDriver
    -> Better than Selenium IDE and Selenium RC (more modern and stable approach in automating the browser's actions).
	-> Controls the browser by directly communicating with it (controls the browser from the OS level)
	-> Support multiple language Java/C#/PHP/Python
	-> No  built-in command that automatically generates a Test Results File
	-> cannot readily support new browsers
 - Selenium Grid
    -> Tool used to run parallele tests across different machines
	-> Run a huge test suite, that needs to complete in the soonest time possible.
 
 
 => Selenium Remote Control (RC) and WebDriver are merged into Selenium 2

# Competitors ?

 - HP Quick Test Pro (QTP now UFT) : 
   -> More advance capabilities
   -> can also control desktop app
   -> automates faster than selenium
   -> native capability to export test data
   -> native test report generation
   But :
   -> More expensive (not free :))
   -> Support less browser, programming language and platform
   -> No parallele testing without Quality center



# limitation

 - Selenium is not very good for load tests (multiple users at same time) => loadrunner would be a better choice for it

#Resources

- https://www.guru99.com/selenium-tutorial.html
