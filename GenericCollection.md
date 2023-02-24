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

  # C# - ArrayList

 →
   ArrayList is a non-generic collection of objects whose size increases dynamically. It is the same as Array except that its size increases dynamically.

> Create an ArrayList


using System.Collections;


ArrayList arlist = new ArrayList(); 

var arlist = new ArrayList(); 


## Adding Elements in ArrayList

var arlist1 = new ArrayList();

arlist1.Add(1);

arlist1.Add("Bill");

arlist1.Add(" ");

arlist1.Add(true);

arlist1.Add(4.5);

arlist1.Add(null);


var arlist2 = new ArrayList()

                {
                    2, "Steve", " ", true, 4.5, null

                };




![Benjamin Bannekat](https://www.tutorialsteacher.com/Content/images/csharp/arraylist.png).

## ArrayList Properties

Capacity :	Gets or sets the number of elements that the ArrayList can contain.

Count :	Gets the number of elements actually contained in the ArrayList.

IsFixedSize :	Gets a value indicating whether the ArrayList has a fixed size.

IsReadOnly :	Gets a value indicating whether the ArrayList is read-only.

Item :	Gets or sets the element at the specified index.

## ArrayList Methods

* Add()/AddRange() :	Add() method adds single elements at the end of ArrayList.
AddRange() method adds all the elements from the specified collection into ArrayList.

* Insert()/InsertRange() :	Insert() method insert a single elements at the specified index in ArrayList.

* InsertRange() : method insert all the elements of the specified collection starting from specified index in ArrayList.

* Remove()/RemoveRange() :	Remove() method removes the specified element from the ArrayList.
RemoveRange() method removes a range of elements from the ArrayList.
RemoveAt()	Removes the element at the specified index from the ArrayList.

* Sort()	: Sorts entire elements of the ArrayList.
Reverse()	Reverses the order of the elements in the entire ArrayList.

* Contains :	Checks whether specified element exists in the ArrayList or not. Returns true if exists otherwise false.

* Clear :	Removes all the elements in ArrayList.
CopyTo	Copies all the elements or range of elements to compitible Array.

* GetRange :	Returns specified number of elements from specified index from ArrayList.

* IndexOf :	Search specified element and returns zero based index if found. Returns -1 if element not found.

* ToArray :	Returns compitible array from an ArrayList.

# C# - List< T >

->   List< T > is a collection of strongly typed objects that can be accessed by index and having methods for sorting, searching, and modifying list. It is the generic version of the ArrayList that comes under System.Collections.Generic namespace.

# List< T > Characteristics

* List<T> equivalent of the ArrayList, which implements IList<T>.
* It comes under System.Collections.Generic namespace.
* List<T> can contain elements of the specified type. It provides compile-time type checking and doesn't perform boxing-unboxing because it is generic.
* Elements can be added using the Add(), AddRange() methods or collection-initializer syntax.

* Elements can be accessed by passing an index e.g. myList[0]. Indexes start from zero.

* List<T> performs faster and less error-prone than the ArrayList.

* It can be used to store any type of objects or primitives.
* It can dynamically resize itself as elements are added or removed.
* It supports a wide range of operations such as adding, removing, and searching for elements.
* It maintains the order of elements as they are added.

# Creating a List

List<int> primeNumbers = new List<int>();

primeNumbers.Add(1); // adding elements using add() method

primeNumbers.Add(3);

primeNumbers.Add(5);

primeNumbers.Add(7);

var cities = new List<string>();

cities.Add("New York");

cities.Add("London");

cities.Add("Mumbai");

cities.Add("Chicago");

cities.Add(null);// nulls are allowed for 
reference type list

//adding elements using collection-initializer syntax

var bigCities = new List<string>()

                    {
                        "New York",
                        "London",
                        "Mumbai",
                        "Chicago"                    
                    };


 > ## Add Custom Class Objects in List


 var students = new List<Student>() 

 { 

                new Student(){ Id = 1, 
                Name="Bill"},
                new Student(){ Id = 2, 
                Name="Steve"},
                new Student(){ Id = 3, 
                Name="Ram"},
                new Student()

                { 
                    Id = 4, Name="Abdul"
                }
            };

# Accessing a List

List<int> numbers = new List<int>()

 { 

    1, 2, 5, 7, 8, 10 

};

Console.WriteLine(numbers[0]); // prints 1

Console.WriteLine(numbers[1]); // prints 2

Console.WriteLine(numbers[2]); // prints 5

Console.WriteLine(numbers[3]); // prints 7

// using foreach LINQ method

numbers.ForEach(num => 

   Console.WriteLine(num + ", ")

);

//prints 1, 2, 5, 7, 8, 10,



// using for loop

    for(

    int i = 0; i < numbers.Count; i++

    )

    Console.WriteLine(numbers[i]);

#  Accessing a List using LINQ

var students = new List<Student>() 

{ 

                new Student(){ Id = 1, Name="Bill"},

                new Student(){ Id = 2, 
                Name="Steve"},

                new Student(){ Id = 3, Name="Ram"},

                new Student(){ Id = 4, Name="Abdul"}

            };

//get all students whose name is Bill

   var result =

        from s in students
	     where s.Name == "Bill"
	     select s;

		
foreach(var student in result)

    Console.WriteLine(student.Id + ", " + student.Name);


# List<T> Class Hierarchy

![Benjamin Bannekat](https://www.tutorialsteacher.com/Content/images/csharp/list.png).

