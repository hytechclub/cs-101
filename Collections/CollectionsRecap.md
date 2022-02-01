# Collections
## Lists
A C# `List` stores multiple values of the same type. The list is sized dynamically (it grows and shrinks as you need it to automatically). List indexes also start at zero. 

```cs
List<long> numList;  // creates a variable that will store a list of longs

numList = new List<long>() {1,2,3,4}; // creates a new list of longs, with the numbers 0, 1, 2, 3, and 4 in it
numList.add(5); // adds the number 5 to the end of the list
```

The last element in an array or list is going to be the one less than the length. The first element in the collection is always at index zero. This is important to remember when calculating how many times to loop through a collection when using it in a loop.
 
If the programmer tries to loop through the array too many times, they will get an "index out of bounds" error, which means you tried to access part of the collection which doesn't exist.

## Arrays
An array holds a specific number of values of the same data type. The user must know how many values the array will hold when they create a new array. Array indexes start at zero. There is no real need to use arrays for the purposes of this course, but it can be beneficial to be aware of them.

```cs
long [] numArray;  // creates a variable that will store an array of longs
numArray = new long[10]{0,1,2,3,4,5}; // creates the new array of 10 longs, and fills in 0, 1, 2, 3, 4, and 5 in the first six spots 
numArray[6] = 6;  // sets the value of the Seventh value in the array to 6
```
 
 