## How to create a simple selenium project to launch a browser: ##

1. Integrate Selenium with java Project.

2. In src folder create a package and create a class inside the package.

![Class](https://github.com/manoja13702/Manual-Testing-N/assets/142867318/5c796199-60ad-4209-bf9b-adf3a73f6299)

3. Inside a class create a Main Method.

![MM](https://github.com/manoja13702/Manual-Testing-N/assets/142867318/9a428e2e-168f-4bb2-b7da-1db736417f86)

4. Set the property of the browser and indicate the location of the browsers.

Syntax : System.*setProperty*(key, value);

Here System is a class & setProperty is a static method.

**Key** – “webdriver.chrome.driver” --> Chrome Browser

**Key** – “webdriver.gecko.driver”  --> Fire Fox Browser

**Key** – “webdriver.ie.driver”     --> Internet Explorer

**Value** – Within double quotes copy and paste the location of the WebDriver file for corresponding browser.

5. WebDriver is an interface.

Syntax : Interface ref = new classname();

WebDriver driver  = new ChromeDriver();

6. Use a method called “get” to launch the URL

WebDriver driver = new ChromeDriver();

driver.get(“URL”);

![BL](https://github.com/manoja13702/Manual-Testing-N/assets/142867318/4d4fdfd3-90ad-4c1a-9b07-dc068b321dfa)


