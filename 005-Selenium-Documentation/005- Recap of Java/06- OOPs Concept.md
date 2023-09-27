## OOPs Concepts: ##

**Classes and Objects:** 

Classes are blueprints for objects, defining their properties and behaviour.

**Inheritance:** 

Allows a class to use properties and behaviour of another class. Encourages reusability and extensibility.

**Polymorphism:** 

Allows methods to do different things based on the object they are acting upon, achieved through method overloading and method overriding.

**Encapsulation:** 

Wrapping the data (fields) and code acting on the data (methods) together as a single unit.

**Abstraction:** 

Representing the essential features without including the background details.

**Example (class definition, inheritance, polymorphism):**
~~~
class Vehicle {

void drive() {

System.out.println("Driving...");

}

}
~~~
~~~
class Car extends Vehicle {

@Override

void drive() {

System.out.println("Driving a car...");

}

void accelerate() {

System.out.println("Accelerating...");

}

}

public class Main {

public static void main(String[] args) {

Car myCar = new Car();

myCar.drive(); // Polymorphism

myCar.accelerate(); // Accessing subclass method

}

}
~~~
