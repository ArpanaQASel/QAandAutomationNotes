## Alerts: ##

Alerts are pop-up windows that appear in response to a user action or due to certain conditions. These alerts can be accepted, dismissed, or used to input text.

**Example:**

Consider a scenario where clicking a button triggers an alert.
~~~
// Click a button that triggers an alert

WebElement alertButton = driver.findElement(By.id("alertButton"));

alertButton.click();

// Switch to the alert and accept it

Alert alert = driver.switchTo().alert();

alert.accept();
~~~
