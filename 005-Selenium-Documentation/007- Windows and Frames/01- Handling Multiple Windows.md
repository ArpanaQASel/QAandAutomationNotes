## Handling Multiple Windows: ##

When a web application opens multiple browser windows or tabs, Selenium allows you to switch between these windows and perform actions accordingly.

**Example:**

Let's consider a scenario where clicking a button opens a new window, and we need to interact with elements in both windows.

---

~~~
// Click a button that opens a new window

WebElement newWindowButton = driver.findElement(By.id("newWindowButton"));

newWindowButton.click();

// Get all window handles

Set<String> windowHandles = driver.getWindowHandles();

// Switch to the new window

for (String handle : windowHandles) {

if (!handle.equals(originalWindowHandle)) {

driver.switchTo().window(handle);

// Perform actions on the new window

// ...

break;

}

}

// Switch back to the original window if needed

driver.switchTo().window(originalWindowHandle);
~~~
