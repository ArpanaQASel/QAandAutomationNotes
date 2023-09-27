## Context Click: ##

The contextClick() method simulates a right-click (context click) on a web element. This is often used to open a context menu.
~~~
Actions actions = new Actions(driver);

WebElement element = driver.findElement(By.id("myElement"));

actions.contextClick(element).build().perform();
~~~
