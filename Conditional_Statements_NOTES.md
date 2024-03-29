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
