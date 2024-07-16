# Exception Handling and Debugging

**Syntax errors:** are code errors that you must deal with before you can compile and run your application. 

**Run time errors** are exceptions that occur while the application is running and will stop your application.

Note: If your code is successful, you'll execute all the code in the try block and then jump past the catch block. But if you run into one of the particular exceptions, your code path diverts to the catch block and you'll execute that code instead.

In Java `try` and `catch` blocks are used to handle exceptions, which are unexpected events that distrupt the normal flow of a program. 

- `try`: The code that might throw an exception is placed inside the `try` block. 

- `catch`: This block follows the `try` blocks and caches exception that occur in the `try` block, Each `catch` block can handle a specific type of exception.

```java
try {
    // Code that might throw an exception
} catch (ExceptionType1 e1) {
    // Handle ExceptionType1
} catch (ExceptionType2 e2) {
    // Handle ExceptionType2
} finally {
    // Optional block; executes regardless (in any case) of an exception
}
```

- `throw` is used to explicitly throw an exception from a method or a block of code. 

```java
// throw new ExceptionType("Error Messge");

public void checkAge(int age) {
    if (age < 18) {
        throw new IllegalArgumentException("Age must be 18 or older.");
    }
}

```

## Popular Exception in Java

These exceptions must be either caught or declared in the method signature using the throws keyword.

- IOException: Thrown when an I/O operation fails or is interrupted.

```java
try {
    FileReader file = new FileReader("somefile.txt");
} catch (IOException e) {
    e.printStackTrace();
}
```

- SQLException: Thrown when there is an error with the datatabe.

```java
try {
    Connection con = DriverManager.getConnection(url, user, password);
} catch (SQLException e) {
    e.printStackTrace();
}
```

### Unchecked Exceptions (Runtime Exceptions)
These exceptions are not checked at compile-time but occur at runtime.

- NullPointerException: Thrown when attempting to use null where an object is required.

```java
String str = null;
System.out.println(str.length()); // Throws NullPointerException
```

- ArrayIndexOutOfBoundsOfException: Thrown when accessing an array with an invalid index.

```java
int[] arr = new int[5];
System.out.println(arr[10]); // Throws ArrayIndexOutOfBoundsException
```

- Arithmetic Exception: Thrown when an arithmetic operation is invalid, such as division by zero.

```java
int result = 10 / 0; // Throws ArithmeticException
```

- IllegalArgumentException: Thrown when a method receives an argument that is not appropriate.

```java
public void setAge(int age) {
    if (age < 0) {
        throw new IllegalArgumentException("Age cannot be negative.");
    }
}
```

##

```java
try (BufferedReader br = new BufferedReader(new FileReader("file.txt"))) {
    String line;
    while ((line = br.readLine()) != null) {
        System.out.println(line);
    }
} catch (IOException e) {
    e.printStackTrace();
}
```