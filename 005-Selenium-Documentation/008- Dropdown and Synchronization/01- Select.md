## Select - Single, Multiple, File: ##


- The Select class in Selenium is used to handle dropdowns.
  
- There are three main dropdowns :
  
     a) Single Select
  
     b) Multiple Select

     c) File Upload

**Single Select:**

A single select dropdown allows selecting only one option at a time.

**Example:**
~~~
Select dropdown= new Select(driver.findElement(By.id("singleSelectDropdown")));

dropdown.selectByVisibleText("Option 2");  // Select by visible text
~~~

**Multiple Select:**

A multiple select dropdown allows selecting multiple options at a time.

**Example:**
~~~
Select dropdown = new Select(driver.findElement(By.id("multiSelectDropdown")));

dropdown.selectByVisibleText("Option 1");  // Select by visible text

dropdown.selectByValue("value2");  // Select by value
~~~

**File Upload:**

File upload input allows users to upload files to a web application.

**Example:**
~~~
WebElement fileInput = driver.findElement(By.id("fileInput"));

fileInput.sendKeys("/path/to/file.txt");  // Specify the file path
~~~
