**@Test:**

This annotation marks a method as a test method.

~~~

import org.testng.annotations.Test;

public class TestNGExample {

@Test

public void testMethod() {

System.out.println("This is a test method.");

}

}

~~~

**@BeforeSuite, @AfterSuite:**

These annotations run before and after all tests in a suite.

~~~

import org.testng.annotations.BeforeSuite;

import org.testng.annotations.AfterSuite;

public class TestNGSuiteExample {

@BeforeSuite

public void beforeSuite() {

System.out.println("Before Suite: Initialize resources.");

}

@AfterSuite

public void afterSuite() {

System.out.println("After Suite: Clean up resources.");

}

 }

~~~

**@BeforeTest, @AfterTest:**

These annotations run before and after all the test methods belonging to a <test> tag in XML.

~~~

import org.testng.annotations.BeforeTest;

import org.testng.annotations.AfterTest;

public class TestNGTestExample {

@BeforeTest

public void beforeTest() {

System.out.println("Before Test: Setup test environment.");

}

@AfterTest

public void afterTest() {

System.out.println("After Test: Clean up test environment.");

}

}

~~~

**@BeforeMethod, @AfterMethod:**

These annotations run before and after each test method.

~~~

import org.testng.annotations.BeforeMethod;

import org.testng.annotations.AfterMethod;

public class TestNGMethodExample {

@BeforeMethod

public void beforeMethod() {

System.out.println("Before Method: Setup method-level resources.");

}

@AfterMethod

public void afterMethod() {

System.out.println("After Method: Clean up method-level resources.");

}

@Test

public void testMethod1() {

System.out.println("Test Method 1");

}

@Test

public void testMethod2() {

System.out.println("Test Method 2");

}

}

~~~

**@Listeners:**

This annotation defines test listeners

~~~

import org.testng.ITestListener;

import org.testng.ITestResult;

public class TestNGListenerExample implements ITestListener {

@Override

public void onTestSuccess(ITestResult result) {

System.out.println("Test passed: " + result.getName());

}

@Override

public void onTestFailure(ITestResult result) {

System.out.println("Test failed: " + result.getName());

}

}

~~~
