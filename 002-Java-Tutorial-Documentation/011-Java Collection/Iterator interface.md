


## Iterator interface

Iterator interface provides the facility of iterating the elements in a forward direction only.

**Methods of Iterator interface**

There are only three methods in the Iterator interface. 

|**No.**|**Method**|**Description**|
| :- | :- | :- |
|1|public boolean hasNext()|It returns true if the iterator has more elements otherwise it returns false.|
|2|public Object next()|It returns the element and moves the cursor pointer to the next element.|
|3|public void remove()|It removes the last elements returned by the iterator. It is less used.|


## ListIterator

It is only applicable for List collection implemented classes like ArrayList, LinkedList, etc. It provides bi-directional iteration. ListIterator must be used when we want to enumerate elements of List. This cursor has more functionality(methods) than iterator. ListIterator object can be created by calling listIterator() method present in the List interface.

**Syntax:**
~~~java
ListIterator ltr = l.listIterator();
~~~
`
Note: Here “l” is any List object, ltr is of type. ListIterator interface and refers to “l”. ListIterator interface extends the Iterator interface. So all three methods of Iterator interface are available for ListIterator. In addition, there are six more methods. 
`

**1. Forward direction**
~~~java
    1.1 hasNext(): Returns true if the iteration has more elements

    public boolean hasNext();

    1.2 next(): Same as next() method of Iterator. Returns the next element in the iteration. 

    public Object next(); 

    1.3 nextIndex(): Returns the next element index or list size if the list iterator is at the end of the list. 

    public int nextIndex();
~~~


**2. Backward direction**

~~~java
    2.1 hasPrevious(): Returns true if the iteration has more elements while traversing backward.

    public boolean hasPrevious();

    2.2 previous(): Returns the previous element in the iteration and can throw NoSuchElementException if no more element present.

    public Object previous(); 

    2.3 previousIndex(): Returns the previous element index or -1 if the list iterator is at the beginning of the list, 

    public int previousIndex();

~~~