### Team  
Saul Barrera García:[GitHub](https://github.com/saulbg/Summary_ThirdUnit  

Mario Solorzano Ventura: [GitHub](https://github.com/mariosolven/programming2)

# Subprograms  
A subprogram is a snippet of code that behaves independently within a program. They communicate by passing parameters.  
Each subprogram has its own namespace (local identifiers).  
It may have a section of declarations (variables, constants, etc ...) and also has some input and departure. This allows that the subprogram is completely independent of the main program.  
We can refeer us to the subprograms as parameters. Calling the procedure momentarily stops the program being
we would be operating and control passes to the called procedure. After the actions of the procedure are executed, it returns to the immediately following action to which was lost.  

## By Value  
It means that the function (or subprogram) receives only one copy of the value that the variable has, that is, it cannot modify it.  
When you print the value of the variables you can observe that the value is not affected so when you use this type of subprogram you only do a copy of the values.  
e.g.  
int CheckValue(int x);


## By Reference  
It means that the memory location where the variable is stored is passed, so the function can know how much it is worth, but it can also modify it in any way.  
This means that any modification we make to the function to the content of the reference will immediately affect the original variables.  
To pass values by reference to a function, you only have to put the & (ampersand) symbol in the name of the variable that will be the reference of the original variables.  
e.g.  
int FijateSiEsCincoRef(int &x);  



# Recursion 

Recursion is the process of repeating items in a self-similar way. If a program allows you to call a function inside the same function, then it is called a recursive call of the function.

In the recursive program, the solution to the base case is provided and the solution of the bigger problem is expressed in terms of smaller problems. Example: 

```c
int fact(int n)
{
    if (n < = 1) // base case
        return 1;
    else    
        return n*fact(n-1);    
}
```
In the above example, base case for `n <= 1` is defined and larger value of number can be solved by converting to smaller one till base case is reached.

There are two types:

1. Direct: When in the body of a method there is a call to the same method, we say that the method is directly recursive. That means Direct recursion occurs when a method invokes itself:

```c
int num()
{
	...
	...
	int num();

}
```

2. Indirect: If method A calls method B, method B calls method C, and method C calls method A we call the methods A, B and C indirectly recursive or mutually recursive:

```c
int num()
{
	...
	...
	int sum();

}
int sum()
{
	...
	...
	int num();

}
```

### References

+ https://www.atnyla.com/tutorial/direct-and-indirect-recursion/1/394
+ https://www.geeksforgeeks.org/recursion/
+ http://www.oma.org.ar/omanet/cym98/valorref.htm
+ https://julioecheverri.wordpress.com/2015/01/29/paso-de-variables-por-referencia-en-c/
