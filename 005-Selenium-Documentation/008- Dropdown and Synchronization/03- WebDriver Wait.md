## ﻿WebDriverWait: ##

WebDriverWait is an explicit wait in Selenium. It waits for a certain condition to be met before proceeding further in the code execution. It's more specific than implicit wait.

**Example:**
~~~
WebDriverWait wait = new WebDriverWait(driver, 10);  // Wait up to 10 seconds

WebElement element = wait.until(ExpectedConditions.elementToBeClickable(By.id("someId")));

element.click();
~~~
