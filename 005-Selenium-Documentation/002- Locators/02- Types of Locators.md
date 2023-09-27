**ID Locator :** Id is the fastest locator.
 
~~~
Syntax: driver.findElement(By.id(“id_value”));

Example:   WebElement usernameInput = driver.findElement(By.id("username"));
~~~
**Class Name Locator:**
~~~
Syntax:driver.findElement(By.className(“class\_name”));

Example: WebElement loginButton = driver.findElement(By.className("login-button"));
~~~
**Name Locator:**
~~~
Syntax: driver.findElement(By.name(“name\_value”));

Example: WebElement usernameInput = driver.findElement(By.name("username"));
~~~
**Xpath Locator:**
~~~
Syntax: driver.findElement(By.xpath(“xpath\_value”));

Example: WebElement submit= driver.findElement(By.xpath("//button[@id='submit']"));
~~~
**CSS Selector Locator:**
~~~
Syntax: driver.findElement(By.cssSelector”));

Example: WebElement submit = driver.findElement(By.cssSelector("button.login-button"));
~~~
**Tag Name Locator:**
~~~
Syntax: driver.findElement(By.tagName(“tag\_name”));

Example: WebElement inputField = driver.findElement(By.tagName("input"));
~~~
**Link Text locator:**
~~~
Syntax: driver.findElement(By.linkText(“link\_text”));

Example: WebElement forgotPasswordLink = driver.findElement(By.linkText("Forgot Password?"));
~~~
**Partial Link Text Locator:**
~~~
Syntax: driver.findElement(By.partialLinkText(“partial\_link\_text”)); 

Example: WebElement forgotPasswordLink = driver.findElement(By.partialLinkText("Forgot"));
~~~






