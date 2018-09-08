# Accessing Packages 
- It is very common for classes within the package to access other classes in the same package. 
- Different Packages (If we have to access a class from a different package then there are two ways to do it.)
  - First one is by using an **import** statement.
    - ``` e.g. import com.java.Date ```
  - Second is by using a fully qualified class name a fully qualified class name is nothing with the package name followed by a dot which is then followed by the class name.
    - ``` e.g. com.java.Date date =  new com.java.Date(); ```
# Import Statement

Example :-
```
import java.util.ArrayList

class FooClass{
void foo(){
ArrayList list = new ArrayList();
...
...
...
}
}


```
   
> `import java.util.ArrayList` This informs the compiler that we want to use the class ArrayList from the package.

>*NOTE:* This import statement must be at the top of the class and must be  outside the class definition.

# Importing Single vs Multiple Classes

- Import single class
  - Explicit Import (or Single - Type - Import)
    - `import java.util.ArrayList `
- Import multiple classes
  - Separate explicit import
  - \* import ( or Import-On-Demand) 
    - \* import
     - This Imports all the classes in a packages 
     - e.g. `import java.util.*;`
> \* import is a shortcut for importing multiple classes as you were having just a single import statement instead.

# Explicit import or \* import?
- To import multiple classes from the same package we need to use either start import or expensive imports.

> So one question would be Is there any recommendation among the two options one issue it's not important.
- \* import can break code
- Better clarity with explicit import.
- Explicit import seems to be preferred.

# Fully - Qualified Class Name

-  Alternative to import 
      - java.til.ArrayList list =  new java.util.ArrayList();
- Required if using both java.util.Date and java.sql.Date

For example let's say we want to use both java.util.Date or java.sql.Date in the same class.

This is a fairly uncommon scenario.But in this case you would have to use a fully qualified name for at least one of the classes.

There are two solutions for this case.

## Solution-1
- Use only one explicit import
```
import java.util.Date;
import java.sql.*;
...

Date date;// Using from import statement
java.sql.Date date2; // this is fully qualifyed name. 

```
> So basically using a simple name of the class will always reference the class from the explicit import. So explicit import takes president over start import in such a scenario.

> Note: Just note that in this example we have only two classes but even if there were say many classes and 10 different packages and we want to use all of them in the same class then we can only explicitly import one of them and for the rest mind you would  have to use them using their fully qualified names.


## Solution-2
Use Only Fully-Qualified names

```
import java.util.*;
import jav.sql.*;
...
...
java.util.Date date;
java.sql.Date date2;
```
 > In this senario always use fully qualified name. 
 
 > Note: Both import statement for date class gives a compiler error
 ```
 import java.util.Date;
 import java.sql.Date; // Gives Compilation error
 ```
 
 ## Any Side affects in using imports ?
 
 -  An answer is No.
 -  You can have as many important statements as you want and you may never even use those classes and it will not have any effect.
 -  Similarly an import statement does not affect that runtime performance too it simply saves you from typing the fully qulified name of the class.
 - However on you compile your code the compiler simplly replaces the simple class names with the corresponding fully qualified class name.
 
 > java.lang packed which is fundamental to java is imported by default, So you don't have to explicitly import any of the classes in this package.
 
 
