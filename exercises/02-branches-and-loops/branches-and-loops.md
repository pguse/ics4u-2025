# Branches and Loops

## Exercises

## 03-0: At Least One Odd Number?

In **IntelliJ IDEA**, create a **New Project** called OneOdd.

In the **src** folder create a **Java class** file called *OneOdd.java* with the following source code

```java
public class OneOdd {  
    public static void main(String[] args) {  
        // Create variables with values  
        int a = 10;  
        int b = 15;  
  
        // Is at least one value even?  
        // Note != is the NOT EQUAL TO operator        if (a % 2 == 0 || b % 2 == 0) {  
            System.out.println("YES");  
        } else {  
            System.out.println("NO");  
        }  
    }  
}
```

Modify the source code so that it determines if at **least one of 3** given numbers is **odd**.  Currently, the source code is checking whether at least one of 2 numbers is even.

**Output:**  print "YES" if at least one of 3 numbers is odd and print "NO" otherwise.


## 03-1: Ascending Integers?

In **IntelliJ IDEA**, create a **New Project** called AscendingIntegers.

In the **src** folder create a **Java class** file called *AscendingIntegers.java* with the following source code

```java
public class AscendingIntegers {  
    public static void main(String[] args) {  
        int a = 10;  
        int b = 15;  
        int c = 20;  
  
        // Are these values descending?  
        if (a > b && b > c) {  
            System.out.println("YES");  
        } else {  
            System.out.println("NO");  
        }  
    }  
}
```

Modify the source code so that it determines whether 4 variables: *a*, *b*, *c*, and *d* contain **ascending integer values**.

 **Output:** print YES if they're given in ascending order, print NO otherwise.


## 03-2: Multiplication Table  

In **IntelliJ IDEA**, create a **New Project** called MultiplicationTable.

In the **src** folder create a **Java class** file called *MultiplicationTable.java* with the following source code

```java
public class MultiplicationTable {  
    public static void main(String[] args) {  
        int number = 5;  
  
        for (int i=1; i < 11; i++) {  
            System.out.printf("%d x %d = \n", number, i);  
        }  
    }  
}
```
Modify the source code so that the multiplication table for the variable *number* is printed out up to 10.  For example,

### Expected Output:
```
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
…
5 x 10 = 50
```
## 03-3: Divisors

In **IntelliJ IDEA**, create a **New Project** called Divisors.

In the **src** folder create a **Java class** file called *Divisors.java* with the following source code

```java
public class Divisors {  
    public static void main(String[] args) {  
        int number = 12;  
  
        System.out.printf("Divisors of %d: ", number);  
  
        for (int i = 1; i < number+1; i++) {  
  
            // Is the remainder of (number / i) equal to zero?  
  
            System.out.printf("%d ",i);  
        }  
    }  
}
```

Modify the source code to produce the expected output.
### Expected Output:
```
Divisors of 12: 1 2 3 4 6 12
```

## 03-4: Perfect Numbers

In **IntelliJ IDEA**, create a **New Project** called PerfectNumbers.

In the **src** folder create a **Java class** file called *PerfectNumbers.java* with the following source code

The **divisors** of a **perfect number** ***(except for the number itself)*** add up to the number. For example: 6 has divisors 1, 2, 3, 6 and 1 + 2 + 3 = 6. So, 6 is a perfect number. Modify the starter code so that it determines whether a number is **perfect**.

```java
public class PerfectNumbers {  
    public static void main(String[] args) {  
        int number = 12;  
        int sum = 0;  
  
        for (int i = 1; i < number; i++) {  
  
            // Is the remainder of (number / i) equal to zero?  
  
            sum = sum + i;  
        }  
  
        if (sum == number) {  
            System.out.printf("The number %d is a perfect number.", number);  
        }  
    }  
}
```

Your source code should produce the following expected outputs.

For 
```java
int number = 6
```

### Expected Output:
```
The number 6 is a perfect number.
```

For
```java
int number = 10
```

### Expected Output:
```
The number 10 is NOT a perfect number.
```
