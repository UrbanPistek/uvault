# Overview

## Embedded Design Guidelines 

Most relivent for developing safety critical code. 

1.  Avoid complex flow constructs (such as goto's & recursion)

        Justification: Makes for easier code analysis and debugging.

2.  All loops must have a fixed bound 
    
        Justification: Prevents infinite loops & runaway code. 

3. Avoid heap memory allocation
    
        Justification: Dynamic memory allocation to the heap is not deterministic.

4. Keep function length to a maximun of a single page
    
        Justification: Helps with code readability and clarity.

5. Implement an average of 2 input checks / runtime assertions per function
    
        Justification: Helps with error handling, code reliability and performance by helping with intercepting defects.  

6. Restrict the scope of data to be the smallest possible
    
        Justification: Adhears to data hiding principle - data is only visible within the required scope.

7. Check return value of all non-void functions or cast return value to void to indicate that the return is useless
    
        Justification: Help with code reliability and explicity validating return values.

8. Use preprocessor sparingly (macros)
    
        Justification: Helps with code readability and clarity while also limiting the variations of code that need to be tested when using conditional compilation.

9. Try to only use single pointers & do not use function pointers
    
        Justification: Function pointers are difficult to verify and this helps with code readability and clarity.

10. Compile with all warnings active and addressed
    
        Justification: There are simply no excuses for ignoring errors or warnings. 

## C Build Process 

1. Compile source files into object files 
2. Link object files into a single object file (relocatable file)
3. Physical memory is mapped to the relocatable file
4. The locator creates the executable file 

Sequnce of steps: .c (preprocessor)=> .i (compiler)=> .s (assembler)=> .o (linker)=> Relocatable File (locator)=> .exe  

## Terminology 

**Interperters:** Execute code line by line (Python)

**Compilers:** Compile code into object code before execution (C)

**Memory Leak**: Dynamic memory that has not been freed after being used
```c
void foo(){
        int *ptr = malloc(sizeof(int));
        return; // Memory has not been freed/dellocated before return
}
```

### Resources
- https://techinterviewhandbook.org/best-practice-questions/
- https://web.eecs.umich.edu/~imarkov/10rules.pdf
- https://www.guru99.com/c-programming-interview-questions.html
- https://www.edureka.co/blog/interview-questions/c-programming-interview-questions/
- https://www.w3resource.com/c-programming-exercises/
- https://journals.sagepub.com/doi/full/10.1016/j.jala.2006.10.016#:~:text=An%20RTOS%20is%20an%20OS,to%20support%20real%2Dtime%20applications.