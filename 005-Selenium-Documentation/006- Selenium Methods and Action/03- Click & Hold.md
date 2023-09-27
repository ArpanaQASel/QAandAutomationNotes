## Click & Hold: ##

The clickAndHold() method is used to simulate clicking and holding the mouse button on a particular web element. This is often used when you want to drag an element.
~~~
Actions actions = new Actions(driver);

WebElement element = driver.findElement(By.id("myElement"));

actions.clickAndHold(element).build().pe rform();
~~~
