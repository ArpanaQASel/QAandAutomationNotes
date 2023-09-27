## Java Database Connectivity (JDBC): ##

Java Database Connectivity (JDBC) allows Java applications to connect to a database, execute SQL queries, and retrieve results.

**For Example:**
~~~
import java.sql.\*;

public class JDBCExample {

public static void main(String[] args) {

String jdbcURL = "jdbc:mysql://localhost:3306/ExampleDB";

String username = "your\_username";

String password = "your\_password";

try {

Connection connection = DriverManager.getConnection(jdbcURL, username, password);

Statement statement = connection.createStatement();

// Execute a query

ResultSet resultSet = statement.executeQuery("SELECT \* FROM Users");

while (resultSet.next()) {

System.out.println("ID: " + resultSet.getInt("ID") + ", Name: " + resultSet.getString("Name") + ", Age: " + resultSet.getInt("Age"));

}

// Close connections

resultSet.close();

statement.close();

connection.close();

} catch (SQLException e) {

e.printStackTrace();

}

}

}
~~~
