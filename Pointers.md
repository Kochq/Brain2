A **pointer** is a variable that stores the memory address of another variable. It allows you to indirectly access the value of a variable by referring to its memory address.

It's a way to point to the location in the computer's memory where a particular piece of data is stored.

## Key concepts

**Declaration:**
```cpp
int *ptr;
```

**Initialization:**
```cpp
int number = 69;
int *ptr = &number;
```

**Dereferencing:**
```cpp
int value = *ptr;
```
___

You can also use the [new](New_operator.md) and [delete](Delete_operator.md) operators
