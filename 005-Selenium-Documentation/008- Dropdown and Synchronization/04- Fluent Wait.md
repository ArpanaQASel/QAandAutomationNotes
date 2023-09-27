## FluentWait: ##

FluentWait is another type of explicit wait that allows you to define a custom polling interval and ignore specific types of exceptions while waiting for a condition.

**Example:**
~~~
Wait<WebDriver> wait = new FluentWait<>(driver)

.withTimeout(Duration.ofSeconds(10))

.pollingEvery(Duration.ofMillis(500))

.ignoring(NoSuchElementException.class);

WebElement element = wait.until(driver -> driver.findElement(By.id("someId")));
~~~
