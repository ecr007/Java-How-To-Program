# Using Data Collection

Arrays in java are a data structure used to store multiple values of the same type in a single variable.

`java.util.Arrays` class provides various methods for manipulating arrays (such as sorting and searching).

## Simple Arrays

The array is not re-sizable. Once it's been set, it's size can be changed.

Note: Use `Arrays` to manipulate an array. 

**Copying an array**

```java

// Sorting arrays
int[] someArray = {6,4,2,8};
Arrays.sort(someArray);

// sout(someArray) ->  2,4,6,8

int[] original = {1,2,3,4,5,6,7,8,9,10};

// Setting a initial size
int[] part = new int[5];

System.arrayCopy(
    The original Array,
    Original array starts index position,
    Destination Array,
    Destination starts index postion,
    Destination Length,
);
```

## Using Two-Dimensional Arrays

To create a two dimensional Arrays two part of brackets is needed. 

```java
String[][] topDr = new String[3][2];

// Set
topDr[0][0] = "Santiago";
topDr[0][1] = "Santiago de los Caballeros";
topDr[1][0] = "Santo Domingo";
topDr[1][1] = "Distrito Nacional";
topDr[2][0] = "Higuey";
topDr[2][1] = "Bavaro";

StringBuilder res = new StringBuilder("Dr has three big cities, there are: ");

// Response
for (String[] row : topDr) {
    res.append("\n").append(row[0]).append(" and its capital are ").append(row[1]).append(".");
}

System.out.println(res);

/*
Dr has three big cities: 
Santiago and its capital are Santiago de los Caballeros.
Santo Domingo and its capital are Distrito Nacional.
Higuey and its capital are Bavaro.
*/
```

<img src="img/java-2d-array.jpg">

## Common properties and methods of arrays.

- array.lenght:int
- Sorting Arrays: `Arrays.sort(ary)`

- Binary Search:

```java
int index = Arrays.binarySearch(numbers, 3); // Returns the index of the element 3
```

- Filling arrays:
```java
int[] numbers = new int[5];
Arrays.fill(numbers, 7); // Filling the five position with seven.
```
- Copying arrays: 
```java
int[] copiedArray = Arrays.copyOf(numbers, numbers.length);
```

- Comparing arrays: 
```java
int[] array1 = {1, 2, 3};
int[] array2 = {1, 2, 3};
boolean isEqual = Arrays.equals(array1, array2); // Returns true
```

- Converting array to string: `[].toString`


