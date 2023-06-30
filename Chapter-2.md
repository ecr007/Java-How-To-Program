# Introductions to Java Applications Input/Output and Operators.

Note: Syntax error also called compiler errors, compiler-time erros or compilation errors.

Note: It is important Write JavaDoc when begin the program, with the comments Author, Purpose of the program, date and time the program was last modified.

Note: The filename and the Class Name are same, to prevent compiler errors.

## Class Name and Indentifiers 
By convention, Class Names bigin with a capital letter and capitalize the first letter of each word they include.

A class name is an **identifier** a series of characters consisting of letter, digits, underscodes (_), and dollar $ signs,
that does not bigin with digit and does not contains spaces. 

## Class Body
**Important**
To make a group sets of expressions, together, they create what is known as a code block or code segment.

- Left brace: ```{```
- Right brace: ```}```

## Declaring a Method
The stating point of every Java Applications.

```java
// Set Javadoc
public class Welcome1{
  public static void main(String[] args){
    System.out.println("Welcome to Java World!!");
    
  } // end method main
}
```

Note: JVM (Java Virtual Machine) can translete the bytecode (.class) into instructions that are understood by the underlying operating system and hardware.

**Characters**

- Slash ```/```
- Backslash ```\``` (Some is a escape character)

### Escape Sequence

<table>
  <tr>
    <th>Character</th>
    <th>ASCII Code</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>\a</td>
    <td>07</td>
    <td>Alert (Beep, Bell) (added in C89)</td>
  </tr>
  <tr>
    <td>\b</td>
    <td>08</td>
    <td>Backspace</td>
  </tr>
  <tr>
    <td>\e</td>
    <td>1B</td>
    <td>Escape character</td>
  </tr>
  <tr>
    <td>\f</td>
    <td>0C</td>
    <td>Formfeed Page Break</td>
  </tr>
  <tr>
    <td>\n</td>
    <td>0A</td>
    <td>Newline (Line Feed); see notes below</td>
  </tr>
  <tr>
    <td>\r</td>
    <td>0D</td>
    <td>Carriage Return</td>
  </tr>
  <tr>
    <td>\t</td>
    <td>09</td>
    <td>Horizontal Tab</td>
  </tr>
  <tr>
    <td>\v</td>
    <td>0B</td>
    <td>Vertical Tab</td>
  </tr>
  <tr>
    <td>\\</td>
    <td>5C</td>
    <td>Backslash</td>
  </tr>
  <tr>
    <td>\'</td>
    <td>27</td>
    <td>Apostrophe or single quotation mark</td>
  </tr>
  <tr>
    <td>\"</td>
    <td>22</td>
    <td>Double quotation mark</td>
  </tr>
</table>

## Displaying with printf

