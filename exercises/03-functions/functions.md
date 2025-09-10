# Functions

## Exercises

In **IntelliJ IDEA**, create a **New Project** called **Point**.

In the **src** folder create a **Java class** file called *Point.java* with the following source code.

## 02-0: Slope

Create a **slope()** function and implement / use it in the **main()** function as shown below.  The **slope()** function takes the **x and y values** of **two points** as **integer type *parameters***. You will need to edit the return value shown.

```java
public class Point {  
    public static void main(String[] args) {  
        System.out.printf("Slope: %.2f", slope(1,-1, -2, 3));  
    }  
  
    public static double slope(int x1, int y1, int x2, int y2) {
	    // Slope = (y2 - y1) / (x2 - x1)  
        return 1.0;  
    }  
}
```

Notice that the **return type** of the **slope()** function **double**  is indicated in front of the function name.  This explains the keyword **void** that is using in the **main()** method, since the **main()** method does not return a value.

## 02-1: Distance

Create a **distance()** function and implement / use it in the **main()** function as shown below.  The **distance()** function takes the **x and y values** of **two points** as **integer type *parameters***.  You will need to edit the return value shown.

```java
public class Point {  
    public static void main(String[] args) {  
        System.out.printf("Distance: %.2f", distance(1,-1, -2, 3));  
    }  
  
    public static double distance(int x1, int y1, int x2, int y2) {  
        // Distance = sqrt( (x2 - x1)^2 + (y2 - y1)^2 )  
        return 1.0;  
    }  
}
```

Again, notice the return type of the **distance()** function is **double**.

___

In **IntelliJ IDEA**, create a **New Project** called **RightTriangle**.

In the **src** folder create a **Java class** file called *RightTriangle.java* with the following source code.

## 02-2: Triangle Area

Create an **area()** function and implement / use it in the **main()** function as shown below.  The **area()** function takes the **two shorter sides** of a right-angled triangle as **double type *parameters***. You will need to edit the return value shown.

```java
public class RightTriangle {  
    public static void main(String[] args) {  
        System.out.printf("Area: %.2f\n", area(5.0, 12.0));  
    }  
  
    public static double area(double a, double b) {  
        // area = 0.5 * base * height  
        return 1.0;  
    }
}
```
## 02-3: Hypotenuse

Create a **hypotenuse()** function and implement / use it in the **main()** function as shown below.  The **hypotenuse()** function takes the **two shorter sides** of a right-angled triangle as **double type *parameters***. You will need to edit the return value shown.
```java
public class RightTriangle {  
    public static void main(String[] args) {  
        System.out.printf("Hypotenuse: %.2f", hypotenuse(5.0, 12.0));  
    }  
  
    public static double hypotenuse(double a, double b) {  
        return 1.0;  
    }  
}
```



___

In **IntelliJ IDEA**, create a **New Project** called **Number**.

In the **src** folder create a **Java class** file called *Number.java* with the following source code.
## 02-4: Even

Create an **isEven()** function and implement / use it in the **main()** function as shown below.  The **isEven()** function takes a single **integer type *parameter***. You will need to edit the return value shown.
```java
public class Number {  
    public static void main(String[] args) {  
        System.out.println(isEven(10));  
    }  
  
    public static boolean isEven(int number) {  
        return false;  
    }  
}
```
Notice that the **return type** of the **isEven()** function is **boolean**.

## 02-5: Prime

Create a **isPrime()** function and implement / use it in the **main()** function as shown below.  The **isPrime()** function takes a single **integer type *parameter***. You will need to edit the return value shown.  A **prime number** is defined as a **positive integer** greater than 1 that has no positive integer divisors other than 1 and themselves.

```java
public class Number {  
    public static void main(String[] args) {  
        System.out.println(isPrime(10));  
    }  
      
    public static boolean isPrime(int number) {  
        return false;  
    }     
}
```

## 02-6: Greatest Common Divisor

Create a **gcd()** function representing the **greatest common divisor** of the positive integers **m** and **n**, assuming **m > n**, and implement / use it in the **main()** function as shown below. You will need to edit the return value shown.

```java
public class Number {  
    public static void main(String[] args) {  
        System.out.println(gcd(48, 36));  
    }  

    public static int gcd(int m, int n) {  
        return 1;  
    }  
}
```
The best-known **algorithm** for finding a greatest common divisor is **Euclid’s Algorithm**.

**Euclid’s Algorithm** states that the **greatest common divisor** of two integers m and n is 

* **n** if **n** divides into **m** completely with a **remainder of zero**.
* However, if **n** does not divide into **m** completely, then the answer is the **greatest common divisor** of **n** and the **remainder** of **m** divided by **n**.
