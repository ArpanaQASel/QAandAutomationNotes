
# Encapsulation in Java


- Encapsulation in Java is a process of wrapping code and data together into a single unit, for example, a capsule which is mixed of several medicines.
- We can create a fully encapsulated class in Java by making all the data members of the class private. Now we can use setter and getter methods to set and get the data in it.

**Advantage of Encapsulation in Java**

---

- By providing only a setter or getter method, you can make the class read-only or write-only. In other words, you can skip the getter or setter methods.
- It provides you the control over the data. Suppose you want to set the value of id which should be greater than 100 only, you can write the logic inside the setter method. You can write the logic not to store the negative numbers in the setter methods.
- It is a way to achieve data hiding in Java because other class will not be able to access the data through the private data members.
- The encapsulate class is easy to test. So, it is better for unit testin



![Encapsulation](https://github.com/connectaman/Java_Notes_and_Programs/assets/124034778/ba60ad3f-be60-42e6-81c8-b55e5d6f1864)





**Example :**
~~~java
class Name {



    private int age; // Private is used to hide the data



   public int getAge() { return age; } // getter



    public void setAge(int age)

    {

       this.age = age;

    } // setter

}



class Guvi {

    public static void main(String[] args)

    {



        Name n1 = new Name();



        n1.setAge(19);


System.out.println("The age of the person is: "+ n1.getAge());

    }

}
~~~
Output:
~~~
19
~~~
**Advantages of Encapsulation in Java:**

---

- Improves security of an object’s internal state by hiding it from the outside world.
- Increases modularity and maintainability by making it easier to change the implementation without affecting other parts of the code.
- Enables data abstraction, allowing objects to be treated as a single unit.
- Allows for easy addition of new methods and fields without affecting the existing code.
- Supports the object-oriented principle of information hiding, making it easier to change the implementation without affecting the rest of the code.
