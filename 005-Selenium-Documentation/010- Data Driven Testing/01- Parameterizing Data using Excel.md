**Reading Data from Excel:**


~~~
import org.apache.poi.ss.usermodel.\*;

import org.apache.poi.xssf.usermodel.XSSFWorkbook;

import java.io.FileInputStream;

import java.io.IOException;

public class ExcelDataReader {

public static Object[][] readDataFromExcel(String filePath, String sheetName) throws IOException {

FileInputStream inputStream = new FileInputStream(filePath);

Workbook workbook = new XSSFWorkbook(inputStream);

Sheet sheet = workbook.getSheet(sheetName);

int rowCount = sheet.getPhysicalNumberOfRows();

int colCount = sheet.getRow(0).getPhysicalNumberOfCells();

Object[][] data = new Object[rowCount - 1][colCount];

for (int i = 1; i < rowCount; i++) {

Row row = sheet.getRow(i);

for (int j = 0; j < colCount; j++) {

data[i - 1][j] = row.getCell(j).toString();

}

}

workbook.close();

inputStream.close();

return data;

}

}
~~~

**Writing Data to Excel:**

---
~~~

import org.apache.poi.ss.usermodel.\*;

import org.apache.poi.xssf.usermodel.XSSFWorkbook;

import java.io.FileOutputStream;

import java.io.IOException;

public class ExcelDataWriter {

public static void writeDataToExcel(String filePath, String sheetName, Object[][] data) throws IOException {

Workbook workbook = new XSSFWorkbook();

Sheet sheet = workbook.createSheet(sheetName);

for (int i = 0; i < data.length; i++) {

Row row = sheet.createRow(i);

for (int j = 0; j < data[i].length; j++) {

Cell cell = row.createCell(j);

cell.setCellValue(data[i][j].toString());

}

}

FileOutputStream outputStream = new FileOutputStream(filePath);

workbook.write(outputStream);

workbook.close();

outputStream.close();

}

}
~~~
