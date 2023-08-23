# Java Clean Coding Convention
There is a line in the book **Clean Code: A Handbook of Agile Software Craftmanship** by Robert C. Martin:
> "Making it(code) easy to read, actually makes it easier to write."

We can't write code unless we can read the surrounding code. So, to make it readable, we should practice coding conventions. Coding convention in java is summarised below:

## 1. Source Files Structure
Each Java source files must contain a public class or interface. Java maintains an order in it's source file which is given below:
- Beginning comments
- Package and Import statements
- Class and interface declarations
### 1.1 Beginning Comments
In contains some information on authors, class, copyright notice and also brief description of the purpose of the program.
  Example:
  ```java
  /*
 * Class
 * Author
 * Version info
 * 
 * Copyright notice
 */
  ```
### 1.2 Package and Import Statements
Packages are group of classes, sub-packages and interfaces. The first thing we do after the beginning comment is importing necessary packages.
```java
import java.util.*
```
### 1.3 Class and Interface Declaraions
There is also an order which class/interface should follow. The order is shown in the following code section.
```java
/*
 * Class description
 */
public class SourceFile {
    /** class specific implementation comment */

    public static int variableStatic1;
    protected static int variableStatic2;
    private static int variableStatic3;

    public int variable1;
    protected int variable2;
    private int variable3;

    /*
     * constructor declaration
     */
    public SourceFile(){}

    /*
     * methods description
     */
    public void doSomething(){
        //Implementation goes here
    }
    
    /*
     * methods description
     * @Parameters description
     */
    public void doSomethingWithParams(int paramInt, String paramString){
        //Implementation goes here
    }
}
```

## 2. Comments, White Space and Indentation
### 2.1 Comments
| Good                      |            Bad                               |
| ------------------------- | -------------------------------------------- |
| Others can understand and beneficial     | Justification or excuses for mess     |
| Informative and explains the intent      | Uses for something which can be easily understood from the code itself   |
| Used for warning, TODO, highlighting the importance  |  Comment out codes  |

There are various types of comments:
```java
/*
* Block Comment
*/

/* Single Line comment */
sourceFile.isEven(num);  /*Trailing comment*/

// End-of-line comment
```
### 2.2 White Space
**Blank Lines:**
1. Two blank lines should always be used between sections in the source file and between classes and interfaces.
2. One blank line should always be used:
             - between methods.
             - between local variable and it's first statement.

**Blank Spaces:**
Blank spaces should be used when:
- A keyword followed by a parenthesis:
  ```java
  switch (value) {
      ....
  }
- But, not method name followed by parenthesis.
- Operators should be separated from their operands by spaces except unary operators, "++", "--" and ".".
  ```java
  sum = a + b;
  sum++;
  ```
- Arguments should be separated by space after comma in arguments list.
  ```java
  public void add(int a, int b, int c){}
  ```

### 2.3 Indentation
- 4 spaces for the indentation
- Avoid longer than 80 characters in a single line
- Break before an operator, after  a comma
   ```java
   function(longExpression1, longExpression2, longExpression3,
           longExpression4, longExpression5);
   longName1 = longName2 * (longName3 + longName4 - longName5)
             + 4 * longname6;
   ```
- For ternary operators with long expression:
  ```java
  word = (booleanExpression) ? apple : ball;
  word = (booleanExpression) ? apple
                             : ball;
  word = (booleanExpression)
        ? apple
        : ball;
## 3. Naming Convention
Naming is necessary for variables, functions, arguments, classes and packages. But, it is more important to have meaningful name.
- Name should be intention-revealing and searchable.
- **Classes and Interfaces name:** First letter of each internal word should be capatalized(**Upper camel case**). Example:
  ```java
  class BusTicket;
  interface Animal;
  ```
  But we should keep in mind that some noisy word like Data, Info, etc. must be avoided as a suffix. Example: ```StudentData``, ```AccountInfo``` should be avoided.
- To mention group of objects, we should avoid naming with suffix "List". Such as ```studentList``` ,```vehicleList```, etc. It is recommended to use just ```students```, ```vehicles```, ```studentGroup``` etc.
- Methods method should be action verb and follow **lower camel case**. Example: ```doSomething()``.
- **Variable Naming**: It should clearly state what the variable is all about. The variable should be understandable by seeing it's name. If comments are required, then the variable naming may not be appropiate.
  ```java
  int n; // Not clear
  int numberOfStudents;  // Perfectly Understood
  ```
  In case of local variable, we can use short form name. Such as:
  ```java
  for(int i=0; i<10; i++);
  ```
## 4. Function
  Each line should contain at most one statement.
## 5. Statements
  Each line should contain at most one statement.
   




