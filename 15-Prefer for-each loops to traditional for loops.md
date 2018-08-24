# for-each loop
- Introduced in Java 5 Version.
- Iterate only array and other data structures.
- Iterate only in single forward direction. 

##### Examples:

```
int[] array = {0,1,2,3,4,5,6,7,8,9};
for(int i : array){ // variable i should be same type of array element. 
  System.out.println(i);
}
```

# Prefer for-each loops to traditional for loops
  -  Clear syntax, e.g. index variable is hidden
  -  Eliminates opportunities for error.
  -  Preferred for nested iterations.
     e.g.
     ```
     int[] iarray = {1,5,4,7,5,4};
     for(int i : iarray){
      for(int j : iarray){
        System.out.println(i + " -- " + j);
      }
     }
     ```
 ### When is Traditional for Preferable?
    1.  When we need access to index element.
    2.  To travers in both forwared and backword direction.
    3.  Transforming or replace elements.
    4.  Parallel iteration.
        e.g.
        ```
        int[] iArr = {1,2,3};
        int[] jArr = {4,5,6};
        for(int i = 0; j = 0; i<iArr.length && jArr.length; i++, j++){ // Parallel iteration of both array.
        //Do Someting with iArr[i] and jArr[j];
        }
        ```
