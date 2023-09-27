## MAP

In Java, Map Interface is present in java.util package represents a mapping between a key and a value. Java Map interface is not a subtype of the Collection interface. Therefore it behaves a bit differently from the rest of the collection types. A map contains unique keys.

![java-map-hierarchy](https://github.com/connectaman/Java_Notes_and_Programs/assets/124034778/45dafd26-4512-4947-a63b-71ee0f1a7325)


**why and when to use Maps.**

---

Maps are perfect to use for key-value association mapping such as dictionaries. The maps are used to perform lookups by keys or when someone wants to retrieve and update elements by keys. Some common scenarios are as follows: 

- A map of error codes and their descriptions.
- A map of zip codes and cities.
- A map of managers and employees. Each manager (key) is associated with a list of employees (value) he manages.
- A map of classes and students. Each class (key) is associated with a list of students (value).


**Characteristics of a Map Interface**

---

- A Map cannot contain duplicate keys and each key can map to at most one value. Some implementations allow null key and null values like the HashMap and LinkedHashMap, but some do not like the TreeMap.
- The order of a map depends on the specific implementations. For example, TreeMap and LinkedHashMap have predictable orders, while HashMap does not.
- There are two interfaces for implementing Map in Java. They are Map and SortedMap, and three classes: HashMap, TreeMap, and LinkedHashMap.



**Method of Map:**

---

|Method|Action Performed |
| :- | :- |
|clear()|This method is used in Java Map Interface to clear and remove all of the elements or mappings from a specified Map collection.|
|containsKey(Object)|This method is used in Map Interface in Java to check whether a particular key is being mapped into the Map or not. It takes the key element as a parameter and returns True if that element is mapped in the map.|
|containsValue(Object)|This method is used in Map Interface to check whether a particular value is being mapped by a single or more than one key in the Map. It takes the value as a parameter and returns True if that value is mapped by any of the keys in the map.|
|entrySet()|This method is used in Map Interface in Java to create a set out of the same elements contained in the map. It basically returns a set view of the map or we can create a new set and store the map elements into them.|
|equals(Object)|This method is used in Java Map Interface to check for equality between two maps. It verifies whether the elements of one map passed as a parameter is equal to the elements of this map or not.|
|get(Object)| This method is used to retrieve or fetch the value mapped by a particular key mentioned in the parameter. It returns NULL when the map contains no such mapping for the key.|
|hashCode()|This method is used in Map Interface to generate a hashCode for the given map containing keys and values.|
|isEmpty()|This method is used to check if a map is having any entry for key and value pairs. If no mapping exists, then this returns true.|
|keySet()|This method is used in Map Interface to return a Set view of the keys contained in this map. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa.|
|put(Object, Object)|This method is used in Java Map Interface to associate the specified value with the specified key in this map.|
|putAll(Map)|This method is used in Map Interface in Java to copy all of the mappings from the specified map to this map.|
|remove(Object)|This method is used in Map Interface to remove the mapping for a key from this map if it is present in the map.|
|size()|This method is used to return the number of key/value pairs available in the map.|
|values()|This method is used in Java Map Interface to create a collection out of the values of the map. It basically returns a Collection view of the values in the HashMap.|
|getOrDefault(Object key, V defaultValue)|Returns the value to which the specified key is mapped, or defaultValue if this map contains no mapping for the key.|
|merge(K key, V value, BiFunction<? super V,? super V,? extends V> remappingFunction)|If the specified key is not already associated with a value or is associated with null, associate it with the given non-null value.|
|putIfAbsent(K key, V value)|If the specified key is not already associated with a value (or is mapped to null) associates it with the given value and returns null, else returns the current associate value.|


## Java HashMap class


**Points to remember**

---

- Java HashMap class contains values based on the key.
- Java HashMap class contains only unique keys.
- Java HashMap class may have one null key and multiple null values.
- Java HashMap class is non synchronized.
- Java HashMap class maintains no order.
- The initial default capacity of Java HashMap class is 16 with a load factor of 0.75.



---------

```java
import java.util.*;  
public class HashMap2 {  
   public static void main(String args[]) {  
    HashMap<Integer,String> map=new HashMap<Integer,String>();          
      map.put(100,"Amit");    
      map.put(101,"Vijay");    
      map.put(102,"Rahul");  
      map.put(103, "Gaurav");  
    System.out.println("Initial list of elements: "+map);  
    //key-based removal  
    map.remove(100);  
    System.out.println("Updated list of elements: "+map);  
    //value-based removal  
    map.remove(101);  
    System.out.println("Updated list of elements: "+map);  
    //key-value pair based removal  
    map.remove(102, "Rahul");  
    System.out.println("Updated list of elements: "+map);  
   }      
}  
```
Output
```
Initial list of elements: {100=Amit, 101=Vijay, 102=Rahul, 103=Gaurav}
Updated list of elements: {101=Vijay, 102=Rahul, 103=Gaurav}
Updated list of elements: {102=Rahul, 103=Gaurav}
Updated list of elements: {103=Gaurav}
```

---------

**Difference beween Hashtable and HashMap**

---

|**HashMap**|**HashTable**|
| :- | :- |
|HashMap is **non synchronized**. This means that if the hashmap is been used in a **multithread** (in two or more) environment, in that case, the hashmap can be accessed and processed in more than one thread simultaneously.|HashTable is **synchronized**, that is it makes sure that no more than one thread can access the hashtable simultaneously at a given moment of time. The thread which works on Hashtable acquires a lock on it to make the other threads wait till its work gets completed.|
|A HashMap can contain one null key and any number of null values.|A HashTable does not allow null keys and null values. If we try to store any null key or value in HashTable, it will throw a **null pointer exception** error.|
|Using the HashMap we can implement the LinkedHashMap which maintains the order of insertion, also we can implement the TreeMap which will sort the hashmap based on the ascending order of keys.|Using HashTable we cannot store the data in any kind of order. It also does not maintain the mapping in any particular order.|
|HashMap implements the Map interface, and also from the very beginning it is a part of the collection framework.|Initially HashTable was not the part of collection framework. Later on, after being reconstructed to implement the Map interface, it is been made a member of the collection framework.|
|The Iterator of HashMap is a fail-fast and it will throw an error **ConcurrentModificationException** if the map is structurally modified by adding or removing any element by any other thread. It will not throw any error if the map is modified by the iterator’s own remove() method. In simple terms, the word fail-fast |Enumerator for the Hashtable is not fail-fast. As the Hashtable is not multithread, and it can work with only one single thread at a time, so the map is not modified while running the enumerator, and it will not throw any error.|
|In the case of **HashMap** Threads are not required to wait, as multiple threads can work with **HashMap** simultaneously. So the relative performance of **HashMap** is high.|In the case of **HashTable**, it increases the waiting time of the thread as only a single thread can work with **HashTable** at a time. So the performance is low.|
|**HashMap** is introduced in the 1.2 version.|**HashTable** is introduced in the 1.0 version.|
|**HashMap** is non-legacy.|**HashTable** is a legacy.|

