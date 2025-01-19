# Pointers-
Pointers 

Here’s your code:

```c
#include<stdio.h>

int main() {
    int age = 22;

    int *ptr = &age;

    int _age = *ptr;

    printf("%d\n", _age);

    // Address
    printf("%p\n", &age);
    printf("%p\n", ptr);
    printf("%p\n", &ptr);

    // Data
    printf("%d\n", age);
    printf("%d\n", *ptr);
    printf("%d\n", *(&age));

    return 0;
}
```
output
22
garbage 
garbage 
garbage
22
22
22
Here is an example of a simple **call by value** program in C:

### Code:
```c
#include <stdio.h>

// Function to demonstrate call by value
void modifyValue(int num) {
    printf("Inside function (before modification): num = %d\n", num);
    num = 20; // Modify the value of the parameter
    printf("Inside function (after modification): num = %d\n", num);
}

int main() {
    int num = 10;

    printf("Before function call: num = %d\n", num);

    // Call the function
    modifyValue(num);

    printf("After function call: num = %d\n", num);

    return 0;
}
```

### Explanation:
1. **Call by Value**:
   - In call by value, the value of the variable is passed to the function.
   - The function creates a copy of the variable in its own memory space.
   - Any changes made to the variable inside the function do not affect the original variable.

2. **How It Works**:
   - In the `main()` function, the value of `num` is 10.
   - When the `modifyValue()` function is called, a copy of `num` is passed to the function.
   - Modifications inside `modifyValue()` do not affect the original `num` in `main()`.

### Output:
```
Before function call: num = 10
Inside function (before modification): num = 10
Inside function (after modification): num = 20
After function call: num = 10
```

Here is an example of a **call by reference** program in C using pointers:

### Code:
```c
#include <stdio.h>

// Function to demonstrate call by reference
void modifyValue(int *num) {
    printf("Inside function (before modification): *num = %d\n", *num);
    *num = 20; // Modify the value of the variable using the pointer
    printf("Inside function (after modification): *num = %d\n", *num);
}

int main() {
    int num = 10;

    printf("Before function call: num = %d\n", num);

    // Call the function and pass the address of num
    modifyValue(&num);

    printf("After function call: num = %d\n", num);

    return 0;
}
```

### Explanation:
1. **Call by Reference**:
   - In call by reference, the address of the variable is passed to the function.
   - The function uses the pointer to directly access and modify the original variable.

2. **How It Works**:
   - In the `main()` function, the variable `num` has an initial value of `10`.
   - The address of `num` is passed to the `modifyValue()` function.
   - Inside `modifyValue()`, the dereferenced pointer (`*num`) is used to modify the value of the original variable.

### Output:
```
Before function call: num = 10
Inside function (before modification): *num = 10
Inside function (after modification): *num = 20
After function call: num = 20
```

### Key Point:
- The value of `num` in the `main()` function is changed after the function call, demonstrating **call by reference**.

