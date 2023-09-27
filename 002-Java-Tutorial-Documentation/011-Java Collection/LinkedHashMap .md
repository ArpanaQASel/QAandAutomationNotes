

## LinkedHashMap 

Java LinkedHashMap class is Hashtable and Linked list implementation of the Map interface, with predictable iteration order. It inherits HashMap class and implements the Map interface.

![linkedhashmap-hierarchy](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/13de64e7-6093-44c0-a478-fe9b9c7714d1)


**Points to remember**

---

- Java LinkedHashMap contains values based on the key.
- Java LinkedHashMap contains unique elements.
- Java LinkedHashMap may have one null key and multiple null values.
- Java LinkedHashMap is non synchronized.
- Java LinkedHashMap maintains insertion order.
- The initial default capacity of Java HashMap class is 16 with a load factor of 0.75.

**LinkedHashMap class Parameters**

---

Let's see the Parameters for java.util.LinkedHashMap class.

**K: It is the type of keys maintained by this map.**

**V: It is the type of mapped values.**

**Constructors of LinkedHashMap Class**

---

In order to create a LinkedHashMap, we need to create an object of the LinkedHashMap class. The LinkedHashMap class consists of various constructors that allow the possible creation of the ArrayList. The following are the constructors available in this class:

**1. LinkedHashMap():** 

This is used to construct a default LinkedHashMap constructor.

~~~java
LinkedHashMap<K, V> lhm = new LinkedHashMap<K, V>();
~~~
**2. LinkedHashMap(int capacity):** 

It is used to initialize a particular LinkedHashMap with a specified capacity.

~~~java
LinkedHashMap<K, V> lhm = new LinkedHashMap<K, V>(int capacity);
~~~

**3. LinkedHashMap(Map<? extends K,​? extends V> map):**

It is used to initialize a particular LinkedHashMap with the elements of the specified map.
~~~java
LinkedHashMap<K, V> lhm = new LinkedHashMap<K, V>(Map<? extends K,​? extends V> map);
~~~
**4. LinkedHashMap(int capacity, float fillRatio):** 
It is used to initialize both the capacity and fill ratio for a LinkedHashMap. A fillRatio also called as loadFactor is a metric that determines when to increase the size of the LinkedHashMap automatically. By default, this value is 0.75 which means that the size of the map is increased when the map is 75% full.
~~~java
LinkedHashMap<K, V> lhm = new LinkedHashMap<K, V>(int capacity, float fillRatio);
~~~
**5. LinkedHashMap(int capacity, float fillRatio, boolean Order):** 

This constructor is also used to initialize both the capacity and fill ratio for a LinkedHashMap along with whether to follow the insertion order or not.

~~~java
LinkedHashMap<K, V> lhm = new LinkedHashMap<K, V>(int capacity, float fillRatio, boolean Order);

~~~

**LinkedHashMap Example: Key-Value pair**
~~~java
    import java.util.*;  
    class LinkedHashMap2{  
     public static void main(String args[]){  
       LinkedHashMap<Integer, String> map = new LinkedHashMap<Integer, String>();           
          map.put(100,"Amit");    
         map.put(101,"Vijay");    
         map.put(102,"Rahul");    
           //Fetching key  
           System.out.println("Keys: "+map.keySet());  
           //Fetching value  
           System.out.println("Values: "+map.values());  
           //Fetching key-value pair  
           System.out.println("Key-Value pairs: "+map.entrySet());  
     }  
    }  
~~~
Output:
~~~
Keys: [100, 101, 102]
Values: [Amit, Vijay, Rahul]
Key-Value pairs: [100=Amit, 101=Vijay, 102=Rahul]

~~~

