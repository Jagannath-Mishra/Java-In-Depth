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

## if-else statement

It executes the if block if condition is true otherwise else block is executed.

e.g.
```
if(condition){  
//code if condition is true  
}else{  
//code if condition is false  
}  
```

> Find out even and odd number?

```
public class IfElseExample {  
public static void main(String[] args) {  
    int number=13;  
    if(number%2==0){  
        System.out.println("even number");  
    }else{  
        System.out.println("odd number");  
    }  
}  
}  
```

## if-else-if ladder

The if-else-if ladder statement executes one condition from multiple statements.

```
if(condition1){  
//code to be executed if condition1 is true  
}else if(condition2){  
//code to be executed if condition2 is true  
}  
else if(condition3){  
//code to be executed if condition3 is true  
}  
...  
else{  
//code to be executed if all the conditions are false  
}  
```
> Here else block is optional block and if we mention else block then it should be last block.


> Demo Program for if-else-if ladder

```
public class IfElseIfExample {  
public static void main(String[] args) {  
    int marks=65;  
      
    if(marks<50){  
        System.out.println("fail");  
    }  
    else if(marks>=50 && marks<60){  
        System.out.println("D grade");  
    }  
    else if(marks>=60 && marks<70){  
        System.out.println("C grade");  
    }  
    else if(marks>=70 && marks<80){  
        System.out.println("B grade");  
    }  
    else if(marks>=80 && marks<90){  
        System.out.println("A grade");  
    }else if(marks>=90 && marks<100){  
        System.out.println("A+ grade");  
    }else{  
        System.out.println("Invalid!");  
    }  
}  
}  
```
## nested if statement

It's possible to have if..else statements inside a if..else statement in Java. It's called nested if...else statement.

Here's a program to find largest of 3 numbers:
```
class Number {
    public static void main(String[] args) {

        Double n1 = -1.0, n2 = 4.5, n3 = -5.3, largestNumber;

        if (n1 >= n2) {
            if (n1 >= n3) {
                largestNumber = n1;
            } else {
                largestNumber = n3;
            }
        } else {
            if (n2 >= n3) {
                largestNumber = n2;
            } else {
                largestNumber = n3;
            }
        }

        System.out.println("Largest number is " + largestNumber);
    }
}
```
