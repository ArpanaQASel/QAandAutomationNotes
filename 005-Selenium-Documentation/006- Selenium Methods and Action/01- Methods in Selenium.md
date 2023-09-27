1. **click():**

The click() method is used to simulate a mouse click on a web element, such as a button, link, or checkbox. This action emulates a left-click performed by a user.
~~~
WebElement button = driver.findElement(By.id("myButton"));

button.click();
~~~
2. **sendKeys():**

The sendKeys() method allows you to simulate typing into an input field or any other editable element on a webpage.
~~~
WebElement inputField = driver.findElement(By.id("username"));

inputField.sendKeys("myusername");
~~~
3. **clear():**

The clear() method is used to clear the text present in an input field or textarea.
~~~
WebElement inputField = driver.findElement(By.id("username"));

inputField.clear();
~~~
4. **submit():**

The submit() method is used to submit a form. It works on form elements such as buttons or input fields.
~~~
WebElement form = driver.findElement(By.id("loginForm"));

form.submit();
~~~



5. **getText():**

The getText() method retrieves the visible (rendered) text of a web element.
~~~
WebElement heading = driver.findElement(By.tagName("h1"));

String headingText = heading.getText();

System.out.println("Heading: " + headingText);
~~~
6. **getAttribute():**

The getAttribute() method retrieves the value of a specified attribute of a web element.
~~~
WebElement link = driver.findElement(By.tagName("a"));

String hrefValue = link.getAttribute("href");

System.out.println("Link URL: " + hrefValue);
~~~
7. **isDisplayed(), isEnabled(), isSelected():**

These methods are used to check the state of an element.

isDisplayed() - checks if the element is currently visible on the page.

isEnabled()  - checks if the element is enabled or not.

isSelected() - checks if the element is selected (applicable for checkboxes, radio buttons, etc.).
~~~
WebElement element = driver.findElement(By.id("myElement"));

boolean isVisible = element.isDisplayed();

boolean isEnabled = element.isEnabled();

boolean isSelected = element.isSelected();
~~~
