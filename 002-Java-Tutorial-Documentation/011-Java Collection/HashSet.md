## Set


The set interface is present in java.util package and extends the Collection interface. It is an unordered collection of objects in which duplicate values cannot be stored. It is an interface that implements the mathematical set. This interface contains the methods inherited from the Collection interface and adds a feature that restricts the insertion of the duplicate elements.

![Java-Set-Interface-hierarchy](https://github.com/connectaman/Java_Notes_and_Programs/assets/124034778/cc914244-759e-46a4-be46-de3bfa1e16a3)




**Creating Set Objects**

---

Since Set is an interface, objects cannot be created of the typeset. We always need a class that extends this list in order to create an object. And also, after the introduction of Generics in Java 1.5, it is possible to restrict the type of object that can be stored in the Set. This type-safe set can be defined as:

~~~java
// Obj is the type of the object to be stored in Set 

Set<Obj> set = new HashSet<Obj> ();
~~~

**Methods of Set**

---

|Method|`             Description|
| :- | :- |
|add(element)  |          This method is used to add a specific element to the set. The function adds the element only if the specified element is not already present in the set else the function returns False if the element is already present in the Set.|
|addAll(collection)   |This method is used to append all of the elements from the mentioned collection to the existing set. The elements are added randomly without following any specific order.|
|clear()|This method is used to remove all the elements from the set but not delete the set. The reference for the set still exists.|
|contains(element)|This method is used to check whether a specific element is present in the Set or not.|
|containsAll(collection)|This method is used to check whether the set contains all the elements present in the given collection or not. This method returns true if the set contains all the elements and returns false if any of the elements are missing.|
|hashCode()|This method is used to get the hashCode value for this instance of the Set. It returns an integer value which is the hashCode value for this instance of the Set.|
|isEmpty()|This method is used to check whether the set is empty or not.|
|iterator()|This method is used to return the iterator of the set. The elements from the set are returned in a random order.|
|remove(element)|This method is used to remove the given element from the set. This method returns True if the specified element is present in the Set otherwise it returns False.|
|removeAll(collection)|This method is used to remove all the elements from the collection which are present in the set. This method returns true if this set changed as a result of the call.|
|retainAll(collection)|This method is used to retain all the elements from the set which are mentioned in the given collection. This method returns true if this set changed as a result of the call.|
|size()|This method is used to get the size of the set. This returns an integer value which signifies the number of elements.|
|toArray()|This method is used to form an array of the same elements as that of the Set.|




**HashSet in Java**

---

Java HashSet class is used to create a collection that uses a hash table for storage. It inherits the AbstractSet class and implements Set interface.


**The important points about Java HashSet class are:**

---

- HashSet stores the elements by using a mechanism called hashing.
- HashSet contains unique elements only.
- HashSet allows null value.
- HashSet class is non synchronized.
- HashSet doesn't maintain the insertion order. Here, elements are inserted on the basis of their hashcode.
- HashSet is the best approach for search operations.
- The initial default capacity of HashSet is 16, and the load factor is 0.75.


**Constructors of HashSet class**

---

To create a HashSet, we need to create an object of the HashSet class. The HashSet class consists of various constructors that allow the possible creation of the HashSet. The following are the constructors available in this class.

1. HashSet()

This constructor is used to build an empty HashSet object in which the default initial capacity is 16 and the default load factor is 0.75. If we wish to create an empty HashSet with the name hs, then, it can be created as:
~~~java
HashSet<E> hs = new HashSet<E>();
~~~
2. HashSet(int initialCapacity)

This constructor is used to build an empty HashSet object in which the initialCapacity is specified at the time of object creation. Here, the default loadFactor remains 0.75.
~~~java
HashSet<E> hs = new HashSet<E>(int initialCapacity);
~~~
3. HashSet(int initialCapacity, float loadFactor)

This constructor is used to build an empty HashSet object in which the initialCapacity and loadFactor are specified at the time of object creation.
~~~java
HashSet<E> hs = new HashSet<E>(int initialCapacity, float loadFactor);
~~~
4. HashSet(Collection)

This constructor is used to build a HashSet object containing all the elements from the given collection. In short, this constructor is used when any conversion is needed from any Collection object to the HashSet object. If we wish to create a HashSet with the name hs, it can be created as:

~~~java
HashSet<E> hs = new HashSet<E>(Collection C);

~~~

**Methods in HashSet**

---

|add(E e)|Used to add the specified element if it is not present, if it is present then return false.|
| :- | :- |
|clear()|Used to remove all the elements from the set.|
|contains(Object o)|Used to return true if an element is present in a set.|
|remove(Object o)|Used to remove the element if it is present in set.|
|iterator()|Used to return an iterator over the element in the set.|
|isEmpty()|Used to check whether the set is empty or not. Returns true for empty and false for a non-empty condition for set.|
|size()|Used to return the size of the set.|
|clone()                       |Used to create a shallow copy of the set.|



**Java HashSet Example**

Let's see a simple example of HashSet. Notice, the elements iterate in an unordered collection.

~~~java
    import java.util.*;  
    class HashSet1{  
     public static void main(String args[]){  
      //Creating HashSet and adding elements  
        HashSet<String> set=new HashSet();  
               set.add("One");    
               set.add("Two");    
               set.add("Three");   
               set.add("Four");  
               set.add("Five");  
               Iterator<String> i=set.iterator();  
               while(i.hasNext())  
               {  
               System.out.println(i.next());  
               }  
     }  
    }  
~~~
Output:
~~~
Five
One
Four
Two
Three

~~~
