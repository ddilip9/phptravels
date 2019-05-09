# phptravels

Technology stack used: BDD cucumber, Junit/TestNG Runner, Java, Feature files, JSON, XML for raw results storage, extent reporting libs for rich HTML preview, Eclipse/Intelli J IDE, Selenium libs, Appium libs(In case of Mobile), browser drivers, Maven, Jenkins for Continuous execution, Other tools ( Galen libs for layout testing, Sikuli libs for Image based execution)

I will convert all the business requirements in to Feature files, Write couple of scenario’s for the feature which we are intended to automate, Write all the scenario steps, examples, gather test data and complete the creation of feature file.
Once the feature file is ready configure the Cucumber Runner class to execute the scenario’s and generate reports..etc.
Generate Gluecode for all the scenario steps and implement the logic(Selenium script with Internal framework) 
On very high level my Internal framework contains KeywordClass, PageObjectClass, ReportingClass, ConfigurationClass, DriverClass, ComponentClass.

KeywordClass – Contains all the keywords of Selenium functionality (For eg: click(), elementSendText(), waitForElementPresence(), dragAndDrop(), wait(), sleep() ..etc)
PageObjectClass – All the XPath and other elements are recorded in this classes, for better standard create separate class for separate pages in the application – this is equivalent to page object model.

ReportingClass – reporting class get logs for every test step execution, since every keyword is surrounded with try-catch exception handling, Pass/Fail log status will be recorded as XML tags vis reporting class.
ConfigurationClass – used to maintain and supply configuration for test executions, like number of test cases to be execute, which test data sheet to pickup, which browser, which machine(in case of Grid), name of project for reporting, number of devices to execute the script and others..
DriverClass – contains the configuration of drivers and the respective browsers, and mobile devices configurations
ComponentClass – is used to hold the components of sequence of test steps.
