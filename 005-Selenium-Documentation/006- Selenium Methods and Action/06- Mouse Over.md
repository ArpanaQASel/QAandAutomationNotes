## Mouse Over: ##

The moveToElement() method simulates moving the mouse pointer to the middle of the specified element. This is useful when dealing with submenus or dropdowns that are visible only on mouse hover.

~~~
Actions actions = new Actions(driver);

WebElement element = driver.findElement(By.id("myElement"));

actions.moveToElement(element).build().perform();
~~~
