The **new** operator is used for dynamic memory allocation in C++. It is used to allocate memory for a single variable or an array of variables on the heap (free store).

##### The syntax for using new is as follows:
```cpp
// Allocating memory for a single variable
int *intPtr = new int;

// Allocating memory for an array of variables
int *arrPtr = new int[5];
```

> [!Warning]
> The **new** operator returns a pointer to the allocated memory. It's important to note that memory allocated with **new** persist until it is explicitly deallocated with the [delete](Delete_operator.md) operator

> [!Example]
> Here is a simple example on c++ using [delete](Delete_operator.md) alongside with **new**
> ```cpp
> #include <iostream>
> 
> int main() {
>     // Allocating memory for a single variable
>     int *intPtr = new int;
> 
>     // Allocating memory for an array of variables
>     int *arrPtr = new int[5];
> 
>     // Deallocating memory to avoid memory leaks
>     delete intPtr;
>     delete[] arrPtr;
> 
>     return 0;
> }
> ```
