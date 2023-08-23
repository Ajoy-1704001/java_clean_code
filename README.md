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
### Comments
| Good Comments             | Bad Comments                                 |
| ------------------------- | -------------------------------------------- |
| Others can understand and beneficial     | Justification or excuses for mess     |
| Informative and explains the intent      | Uses for something which can be easily understood from the code itself   |
| Used for warning, TODO, highlighting the importance  |  Comment out codes  |
  


