# Java Clean Coding Convention
There is a line in the book **Clean Code: A Handbook of Agile Software Craftmanship** by Robert C. Martin:
> "Making it(code) easy to read, actually makes it easier to write."
We can't write code unless we can read the surrounding code. So, to make it readable, we should practice coding conventions. Coding convention in java is summarised below:

## 1. Source Files Structure
Each Java source files must contain a public class or interface. Java maintains an order in it's source file which is given below:
- Beginning comments
- Package and Import statements
- Class and interface declarations
### 1.1 Beginning comments
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
### 1.2 Package and Import statements
Packages are group of classes, sub-packages and interfaces. The first thing we do after the beginning comment is importing necessary packages.
```java
```
