## Drag and Drop: ##

The dragAndDrop() method is used to simulate dragging an element and dropping it onto another element. This is commonly used for actions like rearranging items on a page.

~~~
Actions actions = new Actions(driver);

WebElement sourceElement = driver.findElement(By.id("source"));

WebElement targetElement = driver.findElement(By.id("target"));

actions.dragAndDrop(sourceElement, targetElement).build().perform();
~~~
