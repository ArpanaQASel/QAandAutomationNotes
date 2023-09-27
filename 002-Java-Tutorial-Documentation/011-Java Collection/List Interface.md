

## List Interface 

The List interface in Java provides a way to store the ordered collection. It is a child interface of Collection. It is an ordered collection of objects in which duplicate values can be stored. Since List preserves the insertion order, it allows positional access and insertion of elements. 

The List interface is found in java.util package and inherits the Collection interface. It is a factory of the ListIterator interface. Through the ListIterator, we can iterate the list in forward and backward directions. The implementation classes of the List interface are ArrayList, LinkedList, Stack, and Vector. ArrayList and LinkedList are widely used in Java programming.


![Java-list-interface](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/9f7e8cfb-6edb-4eb9-b38b-bef27b8614ee)



**Methods of List**

---


|**Method**|**Description**||
| :-: | :-: | :- |
|void add(int index, E element)|It is used to insert the specified element at the specified position in a list.||
|boolean add(E e)|It is used to append the specified element at the end of a list.||
|boolean addAll(Collection<? extends E> c)|It is used to append all of the elements in the specified collection to the end of a list.||
|boolean addAll(int index, Collection<? extends E> c)|It is used to append all the elements in the specified collection, starting at the specified position of the list.||
|void clear()|It is used to remove all of the elements from this list.||
||||
|boolean equals(Object o)|It is used to compare the specified object with the elements of a list.||
|int hashcode()|It is used to return the hash code value for a list.||
|E get(int index)|It is used to fetch the element from the particular position of the list.||
|boolean isEmpty()|It returns true if the list is empty, otherwise false.||
|int lastIndexOf(Object o)|It is used to return the index in this list of the last occurrence of the specified element, or -1 if the list does not contain this element.||
|Object[] toArray()|It is used to return an array containing all of the elements in this list in the correct order.||
|<T> T[] toArray(T[] a)|It is used to return an array containing all of the elements in this list in the correct order.||
|boolean contains(Object o)|It returns true if the list contains the specified element||
|boolean containsAll(Collection<?> c)|It returns true if the list contains all the specified element||
|int indexOf(Object o)|It is used to return the index in this list of the first occurrence of the specified element, or -1 if the List does not contain this element.||
|E remove(int index)|It is used to remove the element present at the specified position in the list.||
|boolean remove(Object o)|It is used to remove the first occurrence of the specified element.||
|boolean removeAll(Collection<?> c)|It is used to remove all the elements from the list.||
|void replaceAll(UnaryOperator<E> operator)|It is used to replace all the elements from the list with the specified element.||
|void retainAll(Collection<?> c)|It is used to retain all the elements in the list that are present in the specified collection.||
|E set(int index, E element)|It is used to replace the specified element in the list, present at the specified position.||
|void sort(Comparator<? super E> c)|It is used to sort the elements of the list on the basis of specified comparator.||
|Spliterator<E> spliterator()|It is used to create spliterator over the elements in a list.||
|List<E> subList(int fromIndex, int toIndex)|It is used to fetch all the elements lies within the given range.||
|int size()|It is used to return the number of elements present in the list.||



**Java List Example**

---

Let's see a simple example of List where we are using the ArrayList class as the implementation.
~~~java
    import java.util.*;  
    public class ListExample1{  
    public static void main(String args[]){  
     //Creating a List  
     List<String> list=new ArrayList<String>();  
     //Adding elements in the List  
     list.add("Mango");  
     list.add("Apple");  
     list.add("Banana");  
     list.add("Grapes");  
     //Iterating the List element using for-each loop  
     for(String fruit:list)  
      System.out.println(fruit);  
      
    }  
    }  
~~~

