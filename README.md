# **Conditional Statements**

  

**These are of two types:-**

1. if-else statement
2. switch statement

  

**#syntax to write them:-**

For if-else statement:-

```awk
   if(condition) {
     //do something if TRUE
   }
   else {
     //do something if FALSE
   }
```

  

for example / sample code:-

```cpp
  #include <stdio.h>

  int main() {
      	int age;
       //this is for taking input from the user
      printf("enter your age : ");
      scanf("%d", &age);
    
      //this is to print if the person is adult or not
     if(age > 18) {
         printf("Your are in adult category \n you can drive, vote");
     }
     else{
         printf("Your are not adult \n");
     }
     return 0;
 }
```

  

*   To add another condition we use `else if` in the code.

for example :

```cpp
#include <stdio.h>

int main() {
	int age;
    //this is for taking input from the user
    printf("enter your age : ");
    scanf("%d", &age);
    
    //this is to print if the person is adult or not
    if(age > 18) {
        printf("You are in adult category \nyou can drive, vote");
    }
    else if(age >= 14) {
        printf("You're a teenager \nbe dedicated to studies");
    }
    else{
        printf("You are not adult \n");
    }
    return 0;
}
```

  

# **Conditional Operators**

  

**Ternary :**

Format:

```ada
Condition ? doSomething if TRUE : doSomething if FALSE 
```

  

Here, ? = check the statement

: = means ye nahi to ye

  

for example:

```vim
age >= 18 ? printf("adult \n") : printf("not adult \n);
```

  

# **Switch**

  

Format:

```awk
switch(number) {
case C1 : //do something
              break;
case C2 : //do something
               break;
default : //do something
}
```

  

*   If we don't write "`break`" we'll all the output's which we have asked it to print, as we can say that here we use "`break`" to break the command after executing each case.

  

for example:

```cpp
#include <stdio.h>

int main() {
	int day;
    //this is for taking input from the user
    printf("enter day 1-7 : ");
    scanf("%d", &day);
    
    //this is to print the day according to the number input
    switch (day) {
        case 1 : printf("Monday \n");
                break;
        case 2 : printf("Tuesday \n");
                break;
        case 3 : printf("Wednesday \n");
                break;
        case 4 : printf("Thursday \n");
                break;
        case 5 : printf("Friday \n");
                break;
        case 6 : printf("Saturday \n");
                break;
        case 7 : printf("Sunday \n");
                break;     
        default : printf("not a valid day \n");  
    }
    return 0;
}
```

  

# Switch Properties:

  

1. **Cases can be in any order :** We can write cases in any order as if we write "case 1" after "case 2" it won't give any error.
2. **Nested switch (switch inside switch) are allowed :** When we are using switches we can write a switch case in another switch case and it is allowed and as it is meshed up the command line we can say it as nested.

for ex.:

*   for switches:

```cpp
#include <stdio.h>

int main() {
	int num;
    //this is for taking input from the user
    printf("enter a number to check wether it is even or odd : ");
    scanf("%d", &num);
    
    //this is to print that the input number is even or odd and wether it is positive or negative
    switch (num > 0) {
        case 1 : printf("positive \n");
                switch (num %2 == 0) {
                    case 1 : printf("even \n");
                    break;
                    default : printf("odd \n");
                }
                break;
        default : printf("negative");
    }
    return 0;
}
```

  

*   for if else:

```cpp
#include <stdio.h>

int main() {
	int num;
    //this is for taking input from the user
    printf("enter a number to check wether it is even or odd : ");
    scanf("%d", &num);
    
    //this is to print the day according to the number input
    if(num > 0) {
        printf("positive \n");
        if(num %2 == 0) {
            printf("even\n");
        } else {
            printf("odd \n");
        }
    } else {
        printf("negative \n");
    }
    return 0;
}
```

# **NEXT CHAPTER**

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
