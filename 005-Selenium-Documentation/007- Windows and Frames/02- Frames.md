## Frame: ##

Frame allow dividing a browser window into multiple sections, each with its own HTML document. Selenium needs to switch to the frame in which the target element is present to interact with it.

**Example:**

Assume we have a webpage with a frame, and we need to interact with an element inside that frame.

---

~~~

// Switch to the frame by index

driver.switchTo().frame(0);

// Perform actions on elements inside the frame

WebElement frameElement = driver.findElement(By.id("frameElementId"));

frameElement.click();

// Switch back to the main content

driver.switchTo().defaultContent();
~~~
