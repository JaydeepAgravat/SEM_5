# Compiler Design

## UNIT-1

### 1.What is compiler? What is front-end and back-end of compiler?

- **Compiler:**
- A compiler is a program that translates source code written in a high-level programming language into machine code or an intermediate code.
- The compilation process typically involves multiple stages, with the front-end and back-end being two primary components.

- **Front-end:**
  - The front-end of a compiler handles the analysis of the source code. It includes the following phases:
    - **Lexical Analysis:** This phase breaks the source code into tokens. Tokens are the smallest units of meaning, such as keywords, identifiers, and operators.
    - **Syntax Analysis (Parsing):** This phase checks the syntax of the source code, ensuring it conforms to the rules of the programming language. It generates a parse tree or an abstract syntax tree (AST).
    - **Semantic Analysis:** This phase checks for semantic errors and enforces the meaning of the code. It involves type checking, scope resolution, and other semantic validations.

- **Back-end:**
  - The back-end of a compiler generates the target code. It includes the following phases:
    - **Intermediate Code Generation:** The compiler generates an intermediate representation of the code, which is a low-level and machine-independent code.
    - **Code Optimization:** This phase improves the efficiency of the intermediate code by applying various optimizations without changing the program's functionality.
    - **Code Generation:** The compiler translates the optimized intermediate code into the target machine code or another intermediate code.

### 2.Explain input, output and action performed by each phases of compiler with example

- **Phases of a Compiler:**
  - **Lexical Analysis (Input):** Reads the source code and breaks it into tokens.
    - *Example:* For the C statement `int x = 5;`, the tokens are `int`, `x`, `=`, `5`, and `;`.
  - **Syntax Analysis (Input):** Checks the syntax of the code and generates a parse tree.
    - *Example:* The parse tree for the assignment statement is a structure that shows the relationship between the variables and the value being assigned.
  - **Semantic Analysis (Input):** Checks the semantics of the code, such as type checking and scope resolution.
    - *Example:* Ensures that a variable is declared before use and that the types of operands in an expression are compatible.
  - **Intermediate Code Generation (Action):** Translates the source code into an intermediate representation.
    - *Example:* Generates three-address code for expressions, like `t = a + b`.
  - **Code Optimization (Action):** Improves the efficiency of the intermediate code.
    - *Example:* Constant folding, loop optimization, and common subexpression elimination.
  - **Code Generation (Action):** Translates the optimized intermediate code into machine code or another intermediate code.
    - *Example:* Generates assembly or machine code instructions for the target architecture.
  - **Code Emission (Output):** Produces the final executable code or object code.
    - *Example:* The final binary file or executable generated for the program.

### 3.Explain the roles of linker, loader and preprocessor

- **Roles of Linker, Loader, and Preprocessor:**
  - **Linker:**
    - Links together multiple object files into a single executable or library.
    - Resolves references between different modules.
    - *Example:* Combining object files produced by separate compilation into a single executable.
  - **Loader:**
    - Loads the executable program into memory for execution.
    - Resolves addresses and assigns memory locations to program components.
    - *Example:* Loading a compiled program into RAM before running it.
  - **Preprocessor:**
    - Handles preprocessing directives in the source code before actual compilation.
    - Performs tasks like file inclusion, macro expansion, and conditional compilation.
    - *Example:* Replacing macro calls with their expansions using `#define` in C/C++.

### 4.Explain the language dependent and machine independent phases of compiler. Also List major functions done by compiler

- **Language Dependent and Machine Independent Phases:**
  - **Language Dependent Phases:**
    - These phases are specific to the programming language being compiled.
    - Includes lexical analysis, syntax analysis, and semantic analysis.
  - **Machine Independent Phases:**
    - These phases are not tied to the programming language and deal with generating intermediate code.
    - Includes intermediate code generation, code optimization, and code generation.
  - **Major Functions Done by Compiler:**
    - Lexical analysis (tokenizing).
    - Syntax analysis (parsing and tree generation).
    - Semantic analysis (type checking and scope resolution).
    - Intermediate code generation.
    - Code optimization.
    - Code generation.
    - Code emission (producing the final executable or object code).

### 5.Define following terms: Compiler, Interpreter, Token

- **Definitions:**
  - **Compiler:** A program that translates high-level source code into machine code or an intermediate code.
  - **Interpreter:** A program that directly executes source code without prior translation, interpreting and executing each statement sequentially.
  - **Token:** A basic unit of meaning in a programming language, identified by the lexical analysis phase. Tokens include keywords, identifiers, operators, and literals.

## UNIT-4

### 1. Explain error recovery strategies

Error recovery strategies in compilers are essential to handle mistakes or errors in the source code gracefully. These strategies help maintain the compilation process even when errors are encountered. Here are some common error recovery strategies:

- **Panic Mode Recovery:**
  - When an error is detected, the parser skips tokens until a synchronization point is reached (e.g., a semicolon or a keyword).
  - The parser then resumes processing from that point.
  - This strategy prevents the parser from producing a cascade of errors due to one mistake.

- **Phrase-Level Recovery:**
  - Identify specific patterns or phrases in the code and attempt to synchronize with them.
  - For example, if a missing semicolon is detected, the parser may look for the start of the next statement to resume parsing.

- **Global Correction:**
  - Attempt to make corrections to the entire source code, often based on heuristics.
  - Common corrections include adding or removing tokens to correct the syntax.
  - This method requires more sophisticated analysis but can lead to better error recovery.

- **Interactive Error Handling:**
  - Involve the user in the error recovery process by providing suggestions or alternatives.
  - Integrated development environments (IDEs) often use this approach to offer code suggestions or corrections.

- **Immediate or Deferred Error Detection:**
  - Decide whether to halt compilation immediately upon detecting an error or continue parsing to identify multiple errors.
  - Immediate detection may prevent a cascade of errors, but deferred detection can provide more comprehensive error messages.

- **Error Reporting:**
  - Provide clear and informative error messages to aid developers in identifying and fixing issues.
  - Include details such as the line number, error type, and a description of the problem.

### 2. Explain the following with example: (1) Lexical phase error (2) Syntactic phase error (3) Semantic  Phase Errors

1. Lexical Phase Error

    - A lexical phase error occurs during the lexical analysis of the source code. It involves issues related to tokenization and recognition of lexical elements. Examples include:

    - **Mismatched Quotes:**

      ```c
      printf("Hello, World!);
      ```

      - Lexical error due to an unclosed string.

    - **Invalid Characters:**

      ```c
      float pi = 3.14a;
      ```

      - Lexical error due to an invalid character in the floating-point constant.

2. Syntactic Phase Error:

    - A syntactic phase error occurs during the parsing of the source code, where the structure of the code violates the grammar rules of the programming language. Examples include:

    - **Missing Semicolon:**

      ```c
      int x
      ```

      - Syntactic error due to a missing semicolon at the end of the statement.

    - **Unmatched Parentheses:**

      ```c
      if (x > 0 {
          // code
      ```

      - Syntactic error due to an unmatched opening parenthesis.

3. Semantic  Phase Errors:

   - Definition: Semantic errors occur when the code is grammatically correct but does not behave as intended. These errors are often logical mistakes in the code.

   - Example:

    ```c
    int x = 5 / 0;
    ```

    - Division by zero is a semantic error as it leads to undefined behavior.

### 3.Explain error recovery strategies used by parser

- **Panic Mode Recovery:**
  - Parser skips tokens until a synchronization point is reached.
  - Example:

    ```c
    int x = 5 +
    int y = 10;
    ```

    - The parser can recover after the `+` by skipping tokens until it finds a semicolon.

- **Phrase-Level Recovery:**
  - Identify specific patterns or phrases to synchronize with.
  - Example:
  
    ```c
    for (int i = 0 i < 10; i++) {
        // code
    }
    ```

    - The parser can synchronize by looking for the opening brace and continue parsing.

- **Global Correction:**
  - Attempt to make corrections based on heuristics.
  - Example:

    ```c
    if (x > 0) {
        // code
    else {
        // code
    }
    ```

    - The parser might detect the missing closing brace for the if statement and insert it to correct the syntax.

- **Interactive Error Handling:**
  - Involve the user in the recovery process.
  - Example:

    ```c
    float pi = 3.14a;
    ```

    - The IDE could suggest correcting the invalid character in the floating-point constant.

## UNIT-6

### 1. Compare: Static v/s Dynamic Memory Allocation

| Feature                         | Static Memory Allocation           | Dynamic Memory Allocation           |
|---------------------------------|------------------------------------|--------------------------------------|
| **Memory Allocation Timing**    | Occurs at compile time             | Occurs at runtime                    |
| **Flexibility**                 | Less flexible                      | More flexible                       |
| **Memory Size**                 | Fixed, determined at compile time  | Variable, determined at runtime      |
| **Memory Management Overhead**  | Lower                              | Higher                             |
| **Usage**                       | Typically for simple programs     | Essential for complex applications  |
| **Example**                     | Static arrays, global variables   | Heap-based data structures, dynamic arrays |
| **Responsibility**              | Compiler determines memory layout | Programmer explicitly manages memory |
| **Lifetime**                    | Entire program execution          | Can be allocated and deallocated dynamically |
| **Allocation/Deallocation**     | Automatic                         | Manual (explicit allocation and deallocation) |
| **Errors**                      | Compile-time errors for size-related issues | Runtime errors possible (e.g., memory leaks, segmentation faults) |
| **Efficiency**                  | Generally more efficient in terms of access speed | Slightly less efficient due to runtime management |

### 2. Explain Activation Record

An activation record, also known as a stack frame or function call frame, is a data structure used to manage the information associated with a single invocation of a function or procedure. It plays a crucial role in supporting function calls and providing a mechanism for managing the local variables, parameters, return addresses, and other information for each function call in a program. Let's break down the components of an activation record in a detailed manner:

- Components of an Activation Record

1. **Return Address:**
   - The return address is a pointer or address indicating where the control should return after the function execution completes.
   - It is crucial for maintaining the flow of program execution.

2. **Control Link (or Frame Pointer):**
   - The control link, also known as the frame pointer, points to the activation record of the calling function.
   - It facilitates navigation through the stack frames, allowing access to the local variables and parameters of the calling function.

3. **Parameters:**
   - The parameters of the function are stored in the activation record.
   - For example, in C programming, parameters are often stored in fixed positions relative to the frame pointer.

4. **Local Variables:**
   - Local variables declared within the function are stored in the activation record.
   - The size of the space allocated for local variables is determined by the compiler.

5. **Temporary (or Scratch) Space:**
   - Some space may be reserved for temporary variables or intermediate values during the execution of the function.
   - It is used for storing values that are not required to persist beyond the function call.

6. **Saved Registers:**
   - Registers that need to be preserved across function calls are saved in the activation record.
   - This ensures that the calling function's register values are not unintentionally modified by the called function.

7. **Dynamic Link (or Heap Pointer):**
   - If a function dynamically allocates memory from the heap during its execution, the dynamic link points to the dynamic memory block.
   - This is essential for proper memory management.

Activation Record Example (x86 Assembly):

- Consider a simple C function and its corresponding x86 assembly code:

**C Code:**

```c
int add(int a, int b) {
    return a + b;
}

int main() {
    int result = add(3, 4);
    return 0;
}
```

**x86 Assembly (simplified):**

```assembly
add:
    push ebp                  ; Save current base pointer
    mov ebp, esp              ; Set base pointer to current stack pointer

    mov eax, [ebp+8]          ; Load 'a' into register eax
    add eax, [ebp+12]         ; Add 'b' to eax
    pop ebp                   ; Restore previous base pointer
    ret                       ; Return to the calling function

main:
    push ebp                  ; Save current base pointer
    mov ebp, esp              ; Set base pointer to current stack pointer

    push 4                    ; Push parameter 'b' onto the stack
    push 3                    ; Push parameter 'a' onto the stack
    call add                  ; Call the 'add' function
    add esp, 8                ; Adjust the stack pointer after function call

    mov [ebp-4], eax          ; Store the result in the 'result' variable
    pop ebp                   ; Restore previous base pointer
    mov eax, 0                ; Return 0 from the 'main' function
    ret
```

In this example, you can observe the manipulation of the stack and the activation records in the assembly code. The `push` and `pop` instructions are used to manage the stack, and the base pointer (`ebp`) is used to access parameters, local variables, and saved registers within the activation records.

### 3. Explain dynamic memory allocation strategy

Dynamic memory allocation is a process in which a program requests memory from the operating system during runtime to store data structures whose size cannot be determined at compile time. The management of dynamically allocated memory is crucial to avoid memory leaks, improve program efficiency, and ensure proper use of system resources. Here are the key aspects of dynamic memory allocation strategies:

1. **Dynamic Memory Allocation Functions:**
   - **`malloc(size_t size)`:**
     - Allocates a block of memory of the specified size.
     - Returns a pointer to the beginning of the allocated memory.
     - Memory is uninitialized.

   - **`calloc(size_t num, size_t size)`:**
     - Allocates a block of memory for an array of elements, initialized to zero.
     - Takes the number of elements (`num`) and the size of each element (`size`).

   - **`realloc(void* ptr, size_t size)`:**
     - Changes the size of the memory block pointed to by `ptr` to the specified size.
     - Returns a pointer to the resized block.
     - Can be used to resize memory previously allocated with `malloc` or `calloc`.

   - **`free(void* ptr)`:**
     - Deallocates the memory block pointed to by `ptr`, making it available for further allocations.

2. **Memory Allocation Strategies:**

   - **a. First Fit:**
     - Allocates the first available block of memory that is large enough to satisfy the request.
     - Simple but can lead to fragmentation.

   - **b. Best Fit:**
     - Allocates the smallest available block that fits the request.
     - Requires searching for the best fit, which may be more time-consuming.

   - **c. Worst Fit:**
     - Allocates the largest available block, hoping to leave larger free blocks for future allocations.
     - Can also suffer from fragmentation.

   - **d. Buddy Allocation:**
     - Allocates memory in powers of two and maintains a free list for each block size.
     - Efficient for avoiding external fragmentation.

3. **Memory Fragmentation:**

   - **a. Internal Fragmentation:**
     - Occurs when allocated memory is larger than required, wasting space within the block.
     - Common in fixed-size allocation strategies.

   - **b. External Fragmentation:**
     - Occurs when free memory is scattered in small, non-contiguous blocks.
     - Can be mitigated through compaction or dynamic strategies like buddy allocation.

4. **Garbage Collection:**

   - **a. Manual Memory Management:**
     - Requires the programmer to explicitly deallocate memory using `free`.
     - Prone to memory leaks if deallocation is overlooked.

   - **b. Automatic Memory Management (Garbage Collection):**
     - Automatically reclaims memory that is no longer in use.
     - Reduces the burden on programmers but introduces runtime overhead.

5. **Memory Allocation Algorithms:**

   - **a. First Fit Algorithm:**
     - Iterate through the free list, allocate the first block that is large enough.

   - **b. Best Fit Algorithm:**
     - Search for the smallest block that fits the request.
     - Requires scanning the entire free list, leading to overhead.

   - **c. Buddy Allocation Algorithm:**
     - Allocates memory in powers of two, coalescing adjacent free blocks.
     - Efficient for avoiding fragmentation.

6. **Memory Leak Detection:**
   - Tools and techniques are available to detect memory leaks, such as using static analysis tools, dynamic analysis tools, or incorporating memory leak detection libraries.

7. **Common Issues:**
   - **a. Dangling Pointers:**
     - Occur when a pointer points to a memory location that has been deallocated.

   - **b. Double-Free Errors:**
     - Occur when the same memory block is deallocated more than once.

   - **c. Memory Overflows:**
     - Occur when data exceeds the allocated size of a memory block.

8. **Memory Allocation in High-Level Languages:**
   - In high-level languages like Java or Python, garbage collectors automatically manage memory, reducing the likelihood of memory-related errors.

Dynamic memory allocation is a critical aspect of programming, and understanding the strategies and potential issues associated with it is essential for writing robust and efficient programs.

### 4. Write difference(s) between stack and heap memory allocation

| Feature                           | Stack Memory Allocation                                     | Heap Memory Allocation                                       |
|-----------------------------------|--------------------------------------------------------------|----------------------------------------------------------------|
| **Management**                    | Managed by the compiler.                                    | Managed explicitly by the programmer using memory allocation functions (`malloc`, `calloc`, `realloc`, `free`).     |
| **Scope**                         | Limited to the function or block in which variables are declared. | Can have a broader scope, not bound by the scope of functions or blocks.                             |
| **Size**                          | Generally smaller in size. Fixed size allocated at compile time. | Generally larger in size. Dynamically allocated, can grow or shrink during program execution.                    |
| **Speed**                         | Faster access and allocation. Involves simple pointer adjustment. | Slower access and allocation. Requires dynamic memory management, pointers, and bookkeeping.                     |
| **Lifetime**                      | Variables have a limited lifetime, automatically deallocated when the function or block exits. | Programmer must manage the lifetime of allocated memory explicitly using deallocation functions (`free`).          |
| **Fragmentation**                 | Minimal fragmentation. Memory is allocated and deallocated in a predictable order (LIFO). | May suffer from fragmentation, including internal and external fragmentation, leading to inefficient use of memory.  |
| **Allocation/Deallocation**       | Automatic. Memory is allocated and deallocated implicitly.    | Manual. Programmer allocates and deallocates memory explicitly using functions like `malloc`, `free`, etc.         |
| **Access Mechanism**              | LIFO (Last-In, First-Out). Variables are pushed and popped onto/off the stack. | Non-contiguous memory access. Pointers are used to access memory blocks, which may not be adjacent in physical memory. |
| **Example**                       | Local variables, function call information, return addresses. | Dynamically allocated data structures, objects, arrays, strings.                                                    |
| **Responsibility**                | Compiler handles memory allocation and deallocation.          | Programmer takes responsibility for memory management, including allocation and deallocation.                    |
| **Error Susceptibility**          | Less prone to memory leaks due to automatic deallocation.     | Prone to memory leaks if deallocation is overlooked or mishandled, leading to potential issues like memory exhaustion.  |
| **Size Limitations**              | Generally limited in size. Stack size is set at compile time. | Larger size. Limited by available system memory and can dynamically adjust during runtime.                           |
| **Dynamic Memory Allocation**     | Not applicable. Memory size is determined at compile time.   | Essential for managing dynamic data structures and accommodating variable-sized data during runtime.                  |

### 5. Explain the following parameter passing methods

Parameter passing methods determine how arguments are passed to functions and how changes to parameters inside the function affect the values outside the function. Let's delve into the details of each method:

1. **Call-by-Value:**
   - **Description:**
     - In call-by-value, the actual value of the argument is passed to the function.
     - A copy of the value is created in the function parameter.
   - **Characteristics:**
     - Changes made to the parameter inside the function do not affect the actual argument.
     - Simple and straightforward.
   - **Example (in C):**

     ```c
     void swap(int a, int b) {
         int temp = a;
         a = b;
         b = temp;
     }
     // Call: swap(x, y);
     ```

2. **Call-by-Reference:**
   - **Description:**
     - In call-by-reference, the memory address (reference) of the actual argument is passed to the function.
     - The function parameter becomes an alias for the actual argument.
   - **Characteristics:**
     - Changes made to the parameter inside the function affect the actual argument.
     - More memory-efficient as it avoids unnecessary copying.
   - **Example (in C):**

     ```c
     void swap(int* a, int* b) {
         int temp = *a;
         *a = *b;
         *b = temp;
     }
     // Call: swap(&x, &y);
     ```

3. **Copy-Restore:**
   - **Description:**
     - Copy-Restore is an uncommon parameter passing method.
     - The actual argument's value is copied initially, and any modifications made to the parameter inside the function are restored upon function exit.
   - **Characteristics:**
     - Unusual and not widely used.
     - Primarily a theoretical concept.
   - **Example (conceptual):**

     ```pseudo
     function addOneAndRestore(int x) {
         int copy = x;       // Copy the initial value
         x = x + 1;          // Modify the parameter
         // Upon function exit, restore the original value to x
     }
     ```

4. **Call-by-Name:**
   - **Description:**
     - In call-by-name, the actual code for the argument is substituted directly into the function.
     - The argument is not evaluated until it is used inside the function.
   - **Characteristics:**
     - Uncommon and not supported in many programming languages.
     - Evaluates the argument every time it is referenced inside the function.
   - **Example (conceptual):**

     ```pseudo
     function square(int x) {
         return x * x;
     }
     // Call: square(2 + 3)
     // Result: (2 + 3) * (2 + 3)
     ```

These methods play a significant role in determining how functions interact with their arguments, affecting issues like memory efficiency, the scope of modifications, and potential side effects. The choice of parameter passing method depends on the language and the specific requirements of the program.

### 6. Explain activation tree

An activation tree, also known as a call tree or invocation tree, is a hierarchical representation of the sequence of function or procedure calls in a program during its execution. The tree structure reflects the nested nature of function calls and provides a visual representation of the call stack. Each node in the activation tree corresponds to a particular function or procedure invocation, and the edges represent the flow of control from one function to another. The activation tree is a valuable tool for understanding the dynamic scope of function calls and the order in which functions are invoked.

Here are the key components and concepts related to the activation tree:

- Components of an Activation Tree:

1. **Root Node:**
   - The topmost node in the tree represents the initial function call that triggers the execution of the program.

2. **Internal Nodes:**
   - Internal nodes represent individual function or procedure calls.
   - Each internal node has a parent corresponding to the calling function and children corresponding to the functions being called.

3. **Leaf Nodes:**
   - Leaf nodes represent the termination of function calls.
   - They indicate functions that do not make further calls or reach the end of their execution.

4. **Edges:**
   - Edges represent the flow of control from the calling function to the called function.
   - They connect the nodes in a parent-child relationship.

- Concepts:

1. **Hierarchy:**
   - The tree structure reflects the hierarchical and nested nature of function calls.
   - Each level in the tree represents a different level of nesting in the function calls.

2. **Dynamic Scope:**
   - The activation tree provides insights into the dynamic scope of function calls, showcasing the order in which functions are invoked and return.

3. **Call Stack:**
   - The activation tree aligns closely with the call stack, with each node corresponding to a stack frame.
   - As functions are called, new nodes are added to the tree, and as functions return, nodes are removed.

4. **Recursion:**
   - Recursive function calls result in the creation of branches within the activation tree, as a function may call itself multiple times.

- Example Activation Tree:

Consider the following pseudocode:

```pseudo
function A() {
    B();
    C();
}

function B() {
    D();
}

function C() {
    // Some code
}

function D() {
    // Some code
}

// Initial call
A();
```

The corresponding activation tree might look like this:

```pseudo
        A
       / \
      B   C
         /
        D
```

In this example, function `A` calls functions `B` and `C`, and `B` calls `D`. The activation tree illustrates the sequence of function calls and their relationships.

Activation trees are useful for debugging, analyzing program flow, and understanding the order of execution in complex programs with multiple function calls and recursion. They provide a visual representation that aids in comprehension and can be a valuable tool for software developers.

## UNIT-5

### 1. Construct Syntax Tree and DAG

The given expression is: `X = a * (b+c) - (b+c) * d`

- Syntax Tree:

```CMD
      =
     / \
    X   -
       / \
      *   *
     / \ / \
    a  +   d
      / \
     b   c
```

- DAG (Directed Acyclic Graph):

```CMD
       =
      / \
     X   -
        / \
       *   *
      / \ /
     a  + 
       / \
      b   c
           \
            d
```

### 2. Translate Expression into Quadruples, Triples, and Indirect Triples The given expression is: `-(a+b)*(c+d)*(a+b*c)`

- Quadruples:

```CMD
1. t1 = a + b
2. t2 = -t1
3. t3 = c + d
4. t4 = t2 * t3
5. t5 = a + b
6. t6 = t5 * c
7. t7 = t4 * t6
```

- Triples:

```CMD
1. t1 = a + b
2. t2 = -t1
3. t3 = c + d
4. t4 = t2 * t3
5. t5 = a + b
6. t6 = t5 * c
7. t7 = t4 * t6
```

- Indirect Triples:

```CMD
1. (1) t1 = a + b
2. (2) t2 = -t1
3. (3) t3 = c + d
4. (4) t4 = t2 * t3
5. (5) t5 = a + b
6. (6) t6 = t5 * c
7. (7) t7 = t4 * t6
```

### 3. Translate Expression into Quadruples, Triples, and Indirect Triples The given expression is: `-(a+b)*(c+d)-(a+b+c)`

- Quadruples:

```CMD
1. t1 = a + b
2. t2 = -t1
3. t3 = c + d
4. t4 = t2 * t3
5. t5 = a + b
6. t6 = c
7. t7 = t5 + t6
8. t8 = t4 - t7
9. t9 = a + b
10. t10 = c
11. t11 = t9 + t10
12. t12 = t8 - t11
```

- Triples:

```CMD
1. t1 = a + b
2. t2 = -t1
3. t3 = c + d
4. t4 = t2 * t3
5. t5 = a + b
6. t6 = c
7. t7 = t5 + t6
8. t8 = t4 - t7
9. t9 = a + b
10. t10 = c
11. t11 = t9 + t10
12. t12 = t8 - t11
```

- Indirect Triples:

```CMD
1. (1) t1 = a + b
2. (2) t2 = -t1
3. (3) t3 = c + d
4. (4) t4 = t2 * t3
5. (5) t5 = a + b
6. (6) t6 = c
7. (7) t7 = t5 + t6
8. (8) t8 = t4 - t7
9. (9) t9 = a + b
10. (10) t10 = c
11. (11) t11 = t9 + t10
12. (12) t12 = t8 - t11
```

### 4. Construct Syntax Tree and DAG The given expression is: `X = a * (b+c) - (b+c) * d`

- Syntax Tree:

```CMD
      =
     / \
    X   -
       / \
      *   *
     / \ / \
    a  +   d
      / \
     b   c
```

- DAG (Directed Acyclic Graph):

```CMD
       =
      / \
     X   -
        / \
       *   *
      / \ /
     a  + 
       / \
      b   c
           \
            d
```

### 5. Translate Expression into Quadruples, Triples, and Indirect Triples: The given expression is: `-(a+b)*(c+d)*(a+b*c)`

- Quadruples:

```CMD
1. t1 = a + b
2. t2 = -t1
3. t3 = c + d
4. t4 = t2 * t3
5. t5 = a + b
6. t6 = t5 * c
7. t7 = t4 * t6
```

- Triples:

```CMD
1. t1 = a + b
2. t2 = -t1
3. t3 = c + d
4. t4 = t2 * t3
5. t5 = a + b
6. t6 = t5 * c
7. t7 = t4 * t6
```

- Indirect Triples:

```CMD
1. (1) t1 = a + b
2. (2) t2 = -t1
3. (3) t3 = c + d
4. (4) t4 = t2 * t3
5. (5) t5 = a + b
6. (6) t6 = t5 * c
7. (7) t7 = t4 * t6
```

### 6. Translate Expression into Quadruples, Triples, and Indirect Triples

The given expression is: `-(a+b)*(c+d)-(a+b+c)`

- Quadruples:

```CMD
1. t1 = a + b
2. t2 = -t1
3. t3 = c + d
4. t4 = t2 * t3
5. t5 = a + b
6. t6 = c
7. t7 = t5 + t6
8. t8 = t4 - t7
9. t9 = a + b
10. t10 = c
11. t11 = t9 + t10
12. t12 = t8 - t11
```

- Triples:

```CMD
1. t1 = a + b
2. t2 = -t1
3. t3 = c + d
4. t4 = t2 * t3
5. t5 = a + b
6. t6 = c
7. t7 = t5 + t6
8. t8 = t4 - t7
9. t9 = a + b
10. t10 = c
11. t11 = t9 + t10
12. t12 = t8 - t11
```

- Indirect Triples:

```CMD
1. (1) t1 = a + b
2. (2) t2 = -t1
3. (3) t3 = c + d
4. (4) t4 = t2 * t3
5. (5) t5 = a + b
6. (6) t6 = c
7. (7) t7 = t5 + t6
8. (8) t8 = t4 - t7
9. (9) t9 = a + b
10. (10) t10 = c
11. (11) t11 = t9 + t10
12. (12) t12 = t8 - t11
```
