**Aggregation**

---

- It represents Has-A’s relationship.
- It is a unidirectional association i.e. a one-way relationship. For example, a department can have students but vice versa is not possible and thus unidirectional in nature.
- In Aggregation, both entries can survive individually which means ending one entity will not affect the other entity.

![Aggregation](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/6cf53ebb-efe8-42a9-aea2-b658be07e647)


**Understanding meaningful example of Aggregation**

In this example, Employee has an object of Address, address object contains its own informations such as city, state, country etc. In such case relationship is Employee HAS-A address.

Address.java
~~~java
public class Address {  
String city,state,country;  
  
public Address(String city, String state, String country) {  
    this.city = city;  
    this.state = state;  
    this.country = country;  
}  
  
}  
~~~
Emp.java
~~~java
public class Emp {  
int id;  
String name;  
Address address;  
  
public Emp(int id, String name,Address address) {  
    this.id = id;  
    this.name = name;  
    this.address=address;  
}  
  
void display(){  
System.out.println(id+" "+name);  
System.out.println(address.city+" "+address.state+" "+address.country);  
}  
  
public static void main(String[] args) {  
Address address1=new Address("gzb","UP","india");  
Address address2=new Address("gno","UP","india");  
  
Emp e=new Emp(111,"varun",address1);  
Emp e2=new Emp(112,"arun",address2);  
      
e.display();  
e2.display();  
      
}  
}  
~~~
Output:
~~~
111 varun
 gzb UP india
 112 arun
gno UP india   
~~~
**Composition**

---

- Composition is a restricted form of Aggregation in which two entities are highly dependent on each other.

- It represents part-of relationship.
- In composition, both entities are dependent on each other.
- When there is a composition between two entities, the composed object cannot exist without the other entity.

![composition](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/4c337884-efbc-43a5-9bbb-9982b0bd22b7)


**Let's take an example of a university and its colleges to understand the concept of Composition.**

We create a class College that contains variables, i.e., name and address. We also create a class University that has a reference to refer to the list of colleges. A University can have more than one collages. So, if a university is permanently closed, then all colleges within that particular university will be closed because colleges cannot exist without a university. The relationship between the university and colleges is Composition.

CompositionExample.java

~~~java
import java.io.*;
import java.util.*;

// class College  
class College {
	public String name;
	public String address;

	College(String name, String address) {
		this.name = name;
		this.address = address;
	}
}

// University has more than one college.   
class University {
	// reference to refer to list of college.
	private final List<College> colleges;

	University(List<College> colleges) {
		this.colleges = colleges;
	}

	// Getting total number of colleges
	public List<College> getTotalCollegesInUniversity() {
		return colleges;
	}
}

class CompositionExample {
	public static void main(String[] args) {
		// Creating the Objects of College class.
		College c1 = new College("ABES Engineering College", "Ghaziabad");
		College c2 = new College("AKG Engineering College", "Ghaziabad");
		College c3 = new College("ACN College of Engineering & Management Sudies", "Aligarh");
		// Creating list which contains the no. of colleges.
		List<College> college = new ArrayList<College>();
		college.add(c1);
		college.add(c2);
		college.add(c3);
		University university = new University(college);
		List<College> colleges = university.getTotalCollegesInUniversity();
		for (College cg : colleges) {
			System.out.println("Name : " + cg.name + " and " + " Address : " + cg.address);
		}
	}
}
~~~
Output:
~~~java
Gaziabad
gaziabad
~~~

