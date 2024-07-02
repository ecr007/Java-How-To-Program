# Working with variables

There are two major classes of variables or data types in java known primitives and objects.

Primitive data types are all lowercase.

String is not a primitive, is complex object. 

Java is a statically typed language.

All variables must have their types declared.

**Primitive number**
All primitive variable are starting by 0; default;

<img src="/img/primitive-data-types.png">

**Helper Classes**

Are part of Java Runtime Library, Each of these classes can be used for converting values from one primitive data type to another and to formart value 

<img src="/img/helper-classes.png">

Helper Classes Package: java.lang.HELPER CLASS NAME

```java

import java.lang.*;

public class Main{
    public static void main(String[] args){
        double doubleVal = 150.25;

        // Convert to another values
        Double obj = new Double(doubleVal);

        // To Float
        float fPrimitive = obj.floatValue();

        // To Int 
        int iPrimitive = obj.intValue();

        // To String
        String sObj = obj.toString();
    
    }
}

```

- Byte.MAX_VALUE: returns the maximum value of a byte variable.

Note: If you exceed the maximum value with a primitive data type, you'll always wrap around to the minimum value and that'll be true for all the primitive data types. 

## Representing currency values with BigDecimal.

Is a class in java that provides operations on arbitrary-precision decimal number. 

**Methods**

- .add(BigDecimal obj);
- .subtract(BigDecimal obj)
- .divide(BigDecimal divisor, int scale, RoundingMode roundingMode)

- .compareTo(BigDecimal val): Compares this BigDecimal with the specified BigDecimal 

// 1 if num1 > num2, -1 if num1 < num2, 0 if equal

- .setScale(int newScale, RoundingMode roundingMode)

- .negate() Returns a BigDecimal whose value is the negation of this BigDecimal.

- .abs() Returns a BigDecimal whose value is the absolute value of this BigDecimal.

- .pow(int n) Returns a BigDecimal whose value is (this<sup>n</sup>).

- .toString() Converts this BigDecimal to a String.


```java

import java.math.BigDecimal;

public static void main(String[] args) {
    try {
        BigDecimal object = new BigDecimal("58.50");

        System.out.println("Current value => "+ object.intValue());
    }
    catch (NumberFormatException e){
        System.out.println("Big Decimal value is wrong!!");
    }
    finally {
        System.out.println("Always for here papa");
    }
}

```