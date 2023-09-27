## PageLoadTimeout: ##

pageLoadTimeout is used to set the amount of time to wait for a page to load completely before throwing an error.

**Example:**
~~~
driver.manage().timeouts().pageLoadTimeout(30, TimeUnit.SECONDS);

driver.get("https://example.com");
~~~
