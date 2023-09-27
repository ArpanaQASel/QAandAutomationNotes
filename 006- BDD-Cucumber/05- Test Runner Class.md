## Test Runner class: ##

Test Runner class helps to execute the feature files and run the associated step definitions. 

**Here's a simple example:**

~~~

import io.cucumber.junit.Cucumber;

import io.cucumber.junit.CucumberOptions;

import org.junit.runner.RunWith;

@RunWith(Cucumber.class)

@CucumberOptions(features = "src/test/resources/features", glue = "package name of step\_definitions")

public class TestRunner {

}

~~~
