## Real-Time Examples: ##

**Example Using Excel:**

---
~~~
public class ExcelDataTest {

@DataProvider(name = "loginData")

public Object[][] loginData() throws IOException {

String filePath = "path/to/excel.xlsx";

String sheetName = "LoginData";

return ExcelDataReader.readDataFromExcel(filePath, sheetName);

}

@Test(dataProvider = "loginData")

public void testLogin(String username, String password) {

// Perform login with provided username and password

// Assertions and other test steps

}

}
~~~
