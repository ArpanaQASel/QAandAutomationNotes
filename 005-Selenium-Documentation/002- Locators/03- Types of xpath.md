1. ## Absolute XPath: ##

An Absolute XPath expression specifies the complete path from the root element to the desired element. It starts from the root node of the document (HTML) and provides the full path to the element being located.

**Example of an Absolute XPath:**
~~~
WebElement element = driver.findElement(By.xpath("/html/body/div[1]/form/input[2]"));
~~~
**Advantages of Absolute XPath:**

- Precise and accurate in locating elements.
- Works well for elements with fixed positions in the DOM.

**Disadvantages of Absolute XPath:**

- Prone to breaking if the HTML structure changes.
- Not suitable for dynamic web applications.
- Lengthy and hard to read, making maintenance difficult.

2. ## Relative XPath: ##

A Relative XPath expression starts selection from anywhere in the document using double forward slashes //. It allows for a more flexible and adaptable approach to element location by specifying a partial path.

**Example of a Relative XPath:**
~~~
WebElement element = driver.findElement(By.xpath("//form/input[@name='username']"));
~~~
**Advantages of Relative XPath:**

- More flexible and resistant to changes in the DOM structure.
- Suitable for dynamic web applications.

**Disadvantages of Relative XPath:**

- Can be slower than absolute XPath as it searches the entire DOM.
- Slightly less precise compared to absolute XPath.
