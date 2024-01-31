The **delete** operator is used to deallocate memory that was previously allocated using [new](New_operator.md). It releases the memory back to the system.

##### The syntax for using delete is as follows:

```cpp
// Deallocating memory for a single variable
delete intPtr;

// Deallocating memory for an array of variables
delete[] arrPtr;
```

> [!Warning]
> It's crucial to use **delete** for every corresponding [new](New_operator.md). If is not deallocated, it can lead to a gradual increase in the program's memory usage, causing a [memory leak](Memory_leak.md)

> [!Example]
> Here is a simple example on c++ using **delete** alongside with **new**
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
