# Control-flow: if-statement

The Java if statement is used to test the condition. It checks boolean condition: true or false. 

### There are various types of if statement in java.

1. if statement
2. if-else statement
3. if-else-if ladder
4. nested if statement

## if-statement

This statement execute some block of codes only if some condition is passes. 

```
if(5>2){
System.out.println("5 is a bigger number.");
}
```

> Parentheses is mandatory to execute block of statement.

> If we didn't provide any parentheses then only first line after the if condition will execute.
e.g.
```
if(5<2)
System.out.println("5 is a bigger number."); // This will be ignored as if condition fails.
System.out.println("Dummy"); // this statement will execute evenif if condition pass or failed.
System.out.println("Dummy"); // this statement will execute evenif if condition pass or failed.
System.out.println("Dummy"); // this statement will execute evenif if condition pass or failed.

```
