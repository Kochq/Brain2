A memory leak occurs in a program when the program allocates memory dynamically (usually using [new](New_operator.md) in C++) but fails to deallocate or free that memory (using [delete](Delete_operator.md)) before the program terminates. 

>[!Example]
> Here is a step by step of how a memory leak can happen:
> 1. **Dynamic memory allocation:**
>    - The program allocates memory on the heap using operator like [new](New_operator.md) in C++
> 	   ```cpp
> 	   int *dynamicPtr = new int;
>      ```
> 2. **Failure to deallocate:**
>    - The program does not free or deallocate the allocated memory before the program exits or before the last reference to the allocated memory is lost.
>      ```cpp
>      // No delete statement to free the allocated memory
>      ```
> 3. **Memory Leak Occurs:**
>    - Because the memory was not deallocated, it remains reserved for the program, even though the program is finished running. This is a memory leak.
> 4. **Accumulation over time:**
>    - If memory leaks are present in a program and the program runs for an extended period or repeatedly performs the allocation without deallocation, the leaked memory can accumulate, leading to a gradual increase in the program's memory usage.

> [!Summary]
> - **Memory leaks** happen when the program loses the reference to dynamically allocated memory, preventing the system from reclaiming that memory for future use.
> - To avoid **memory leaks**, it's essential to ensure that every dynamically allocated memory block is properly deallocated using the corresponding [delete](Delete_operator.md) operator
