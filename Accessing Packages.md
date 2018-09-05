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

Example:

```

```

