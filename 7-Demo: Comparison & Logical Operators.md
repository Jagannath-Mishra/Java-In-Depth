# Demo: Comparison & Logical Operators
```
package com.java.test.demo;

public class Student {
	int id;
	String name;
	String gender;
	
	Student(int id, String name){
		this.id = id;
		this.name=name;
		
	}
	
	public static void main(String[] args) {
		int[] studentId =  new int[] {1000,1001,1003,1002};
		
		//Creating first student object and setting its state.
		
		Student student1 =  new Student(studentId[0],"Jagan");
		student1.gender = "male";
		
		//Creating second student object and setting its state.
		
		Student student2 =  new Student(studentId[1],"Raj");
		student1.gender = "male";
				
		//Creating third student object and setting its state.
				
		Student student3 =  new Student(studentId[2],"Gari");
		student1.gender = "female";
		
		
		System.out.println("Name of Student1 "+student1.name);
		System.out.println("Name of Student2 "+student2.name);
		System.out.println("Name of Student3 "+student3.name);
		
		if(student1 == student2) {
			
			System.out.println("Student1 referancing to Student2");
		}
		
		if(student1 != student2) {
			System.out.println("Student1 not referancing to Student2");
		}
		
		
		Student student4 = null;
		
		//System.out.println(student4.gender); // NullPointerException
		
		student4 =  student1;
		
		if(student4 != null && student4 == student1 ) {
			
			System.out.println("Student 4  name : "+student4.name);
		}
		
		
		if(student4 != null && student4 == student2 || student4 == student1 ) {
			
			System.out.println("Student 4  name : "+student4.name);
		}

	}
	
	
	
}


```
