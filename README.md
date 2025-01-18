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
