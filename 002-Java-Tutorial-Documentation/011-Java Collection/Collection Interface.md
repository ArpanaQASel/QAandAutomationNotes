## Collection Framework



**What is a Framework?**

---

A framework is a set of classes and interfaces which provide a ready-made architecture. In order to implement a new feature or a class, there is no need to define a framework. However, an optimal object-oriented design always includes a framework with a collection of classes such that all the classes perform the same kind of task.


**Need for a Separate Collection Framework**

---

Before Collection Framework(or before JDK 1.2) was introduced, the standard methods for grouping Java objects (or collections) were Arrays or Vectors, or Hashtables. All of these collections had no common interface. Therefore, though the main aim of all the collections is the same, the implementation of all these collections was defined independently and had no correlation among them. And also, it is very difficult for the users to remember all the different methods, syntax, and constructors present in every collection class.


**Collection Interface** 

---

The Collection interface is a member of the Java Collections Framework. It is a part of java.util package. It is one of the root interfaces of the Collection Hierarchy. The Collection interface is not directly implemented by any class. However, it is implemented indirectly via its subtypes or subinterfaces likeList, Queue, and Set.


**Syntax:** 

~~~java

Collection<E> objectName = new ArrayList<E>();
~~~

**The Hierarchy of Collection:**



![collection](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/d6b1a33d-7a58-4868-8af4-0b3e0d81122c)





**Iterable Interface**


---

The Iterable interface is the root interface for all the collection classes. The Collection interface extends the Iterable interface and therefore all the subclasses of Collection interface also implement the Iterable interface.

It contains only one abstract method. i.e.,

~~~java
Iterator<T> iterator()  

~~~

It returns the iterator over the elements of type T.




**Methods Of Collection**

---













|add​(E e)|Ensures that this collection contains the specified element (optional operation).|
| :- | :- |
|addAll​(Collection<? extends E> c)|Adds all the elements in the specified collection to this collection (optional operation).|
|clear()|Removes all the elements from this collection (optional operation).|
|contains​(Object o)|Returns true if this collection contains the specified element.|
|containsAll​(Collection<?> c)|Returns true if this collection contains all the elements in the specified collection.|
|equals​(Object o)|Compares the specified object with this collection for equality.|
|hashCode()|Returns the hash code value for this collection.|
|isEmpty()|Returns true if this collection contains no elements.|
|iterator()|Returns an iterator over the elements in this collection.|
|parallelStream()|Returns a possibly parallel Stream with this collection as its source.|
|remove​(Object o)|Removes a single instance of the specified element from this collection, if it is present (optional operation).|
|removeAll​(Collection<?> c)|Removes all of this collection’s elements that are also contained in the specified collection (optional operation).|
|removeIf​(Predicate<? super E> filter)|Removes all the elements of this collection that satisfy the given predicate.|
|retainAll​(Collection<?> c)|Retains only the elements in this collection that are contained in the specified collection (optional operation).|
|size()|Returns the number of elements in this collection.|
|spliterator()|Creates a Spliterator over the elements in this collection.|
|stream()|Returns a sequential Stream with this collection as its source.|
|toArray()|Returns an array containing all the elements in this collection.|
|toArray​(IntFunction<T[]> generator)|Returns an array containing all the elements in this collection, using the provided generator function to allocate the returned array.|
|toArray​(T[] a)|Returns an array containing all the elements in this collection; the runtime type of the returned array is that of the specified array.|



