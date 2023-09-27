## ImplicitWait: ##

Implicit wait is a type of wait in Selenium that sets a timeout for the WebDriver to wait for an element to be present in the DOM before throwing a NoSuchElementException. It's set once and affects all subsequent element search calls.

**Example:**
~~~
// Set implicit wait

driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);

// Use the wait while searching for an element

WebElement element = driver.findElement(By.id("someId"));
~~~
