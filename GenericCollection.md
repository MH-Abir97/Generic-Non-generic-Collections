https://dotnettutorials.net/lesson/object-oriented-programming-csharp/

> # C# Generic & Non-generic Collections
## What is Collections ?
* C# includes specialized classes that store series of values or objects are called collections.
##  Type Of Colllection : -
i. Generic  Namespace contains - System.Collections

ii. Non-generic  Namespace contains - System.Collections.Generic

> In most cases, it is recommended to use the generic collections because they perform faster than non-generic collections and also minimize exceptions by giving compile-time errors.

## Generic Collections

> List<T> :-	Generic List<T> contains elements of specified type. It grows automatically as you add elements in it.

> Dictionary<TKey,TValue> :	 Dictionary<TKey,TValue> contains key-value pairs.

> SortedList<TKey,TValue> : 	SortedList stores key and value pairs. It automatically adds the elements in ascending order of key by default.
> Queue<T> :	Queue<T> stores the values in FIFO style (First In First Out). It keeps the order in which the values were added. It provides an Enqueue() method to add values and a Dequeue() method to retrieve values from the collection.

> Stack<T>:	Stack<T> stores the values as LIFO (Last In First Out). It provides a Push() method to add a value and Pop() & Peek() methods to retrieve values.

> Hashset<T> :	Hashset<T> contains non-duplicate elements. It eliminates duplicate elements.

## Non-generic Collections

 ArrayList  : -
ArrayList stores objects of any type like an array. However, there is no need to specify the size of the ArrayList like with an array as it grows automatically.

SortedList  :- SortedList stores key and value pairs. It automatically arranges elements in ascending order of key by default. C# includes both, generic and non-generic SortedList collection.

Stack :- Stack stores the values in LIFO style (Last In First Out). It provides a Push() method to add a value and Pop() & Peek() methods to retrieve values. C# includes both, generic and non-generic Stack.

Queue :  - Queue stores the values in FIFO style (First In First Out). It keeps the order in which the values were added. It provides an Enqueue() method to add values and a Dequeue() method to retrieve values from the collection. C# includes generic and non-generic Queue.

Hashtable :- A Hashtable in C# is a collection class that represents a collection of key-value pairs that are organized based on the hash code of the keys. A hash table allows quick access to values based on their associated keys, making it an efficient data structure for storing and retrieving data.

BitArray : - BitArray manages a compact array of bit values, which are represented as Booleans, where true indicates that the bit is on (1) and false indicates the bit is off (0).


## Diffrence between Hastable and Hasset in C#

 * Hashtable is used to store key-value pairs
 *  HashSet is used to store a set of unique elements.

 *  Hashtable is useful when you need to associate some data with a unique key.
 
  *  HashSet is useful when you only need to store a set of unique elements without any associated values.
