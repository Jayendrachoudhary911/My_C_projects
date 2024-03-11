# Loop Control Instructions

**Q. Why do we use Loop Control Instructions?**

Ans. To repeat some part of the program we use L.C.I.

  

It is if three types:-

1. for
2. while
3. do while

  

## **`for`** loop:

```cpp
for(initialisation; condition; updation) {
//do something
}
```

To print numbers form 1 - 100 using for loop:

```cpp
#include <stdio.h>

int main() {
    for(int i=1; i <= 100; i+=1) {
        printf("%d \n", i);
    }
    return 0;
}
```

  

**Q. Write a program to print the numbers from 0-10.**

Ans.

```cpp
#include <stdio.h>

int main() {
    for(int i=0; i <= 10; i+=1) {
        printf("%d \n", i);
    }
    return 0;
}
```

  

### **Increment operator**

*   `++i` **(Pre increment operator)** it means that it firstly increase the value and then it use it.

#include <stdio.h>

```perl
int main() {
    int i=1;
    printf("%d \n", ++i);
    printf("%d \n", i);
    return 0;
}
```

  

*   `i++` **(Post increment operator)** it means that it firstly use the value and then increase it.

```cpp
#include <stdio.h>
int main() {
    int i=1;
    printf("%d \n", i++);
    printf("%d \n", i);
    return 0;
}
```

  

### **Decrement Operator**

*   `--i` **(Pre decrement)** it means that it firstly decrease the value and then it use it.

```cpp
#include <stdio.h>

int main() {
    int i=1;
    printf("%d \n", --i);
    printf("%d \n", i);
    return 0;
}
```

  

*   `i--` **(Post decrement operator)** it means that it firstly use the value and then decrease it.

```cpp
#include <stdio.h>

int main() {
    int i=1;
    printf("%d \n", i--);
    printf("%d \n", i);
    return 0;
}
```

**Note: we can use them also use them for** **`float`** **and** **`char`** **values also.**

Examples:

for `float` values

```cpp
#include <stdio.h>

int main() {
    for(float i=1.0; i<=5; i++) {
        printf("%f \n", i);
    }
    return 0;
}
```

  

for `char` values

```cpp
#include <stdio.h>

int main() {
    for(char ch='a'; ch<='z'; ch++) {
        printf("%c \n", ch);
    }
    return 0;
}
```

  

*   If we leave the **condition** blank in for **loop** it is known as **infinite loop.**

for ex.

```cpp
#include <stdio.h>

int main() {
    for(float i=1.0; ; i++) {
        printf("Hello world! \n");
    }
    return 0;
}
```

  

## **`while`** loop:

In while loop we have to declare the value outside the while loop and write updation statement inside it before ending it.

format:

```awk
while(condition) {
//do something
}
```

for example:

```cpp
#include <stdio.h>

int main() {
    int i = 1;
    while(i<=5) {
        printf("Hello world! \n");
        i++;
    }
    return 0;
}
```

  

  

**Q. Write a code to print the number from 0 to n, if n is given by user.**

Ans.

```cpp
#include <stdio.h>

int main() {
    int n;
    printf("enter a number:");
    scanf("%d", &n);

    int i=0;
    while(i <= n) {
        printf("%d \n", i);
        i++;
    }
    return 0;
}
```

  

## `do while` loop:

format:

```awk
do {
//do something
} while(condition);
```

for ex.:

```cpp
#include <stdio.h>

int main() {
    int i=1;
    do {
        printf("%d \n", i);
        i++;
    } while(i<=5);
    return 0;
}
```

  

**Q. Write a code to print the sum of first n natural numbers. Also print them in reverse.**

Ans.

for forward:

```cpp
#include <stdio.h>

int main() {
    int n;
    printf("enter a natural number:");
    scanf("%d", &n);

    int sum = 0;
    for(int i = 1; i <= n; i++) {
        sum += i;
    }
    printf("sum is %d \n", sum);
    return 0;
}
```

to print the input number i reverse order:

```cpp
#include <stdio.h>

int main() {
    int n;
    printf("enter a natural number:");
    scanf("%d", &n);

    for(int i = n; i >= 1; i--) {
        printf("%d \n", i);
    }
    
    return 0;
}
```

  

**OR**

Ans.

**combined code for the above is:**

```cpp
#include <stdio.h>

int main() {
    int n;
    printf("enter a natural number:");
    scanf("%d", &n);

    int sum = 0;
    for(int i = 1, j = n; i <= n && j >= 1; i++ , j--) {
        sum += i;
        printf("%d \n", j);
    }
    printf("sum is %d \n", sum);
    return 0;
}
```
