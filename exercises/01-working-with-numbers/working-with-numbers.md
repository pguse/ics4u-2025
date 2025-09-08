# # Working with Numbers

## Exercises

## 01-0: Student Average

In **IntelliJ IDEA**, create a **New Project** called **StudentAverage**.

In the **src** folder create a **Java class** file called *StudentAverage.java* with the following source code

```java
public class StudentAverage {  
    public static void main(String[] args) {  
        int m1 = 80;  
        int m2 = 92;  
        int m3 = 88;  
  
        int average = (m1 + m2 + m3) / 3;  
        System.out.println("Average is: " + average);  
    }  
}
```

1. Click the **play** button to run the program.  Something isn't right.  Everything seems fine, but the way **Java** performs division depends on the types of the operands.  Check with your calculator.  Is the quotient of the division correct?  If not what do you think needs to be changed?
2. Make the necessary changes to produce the correct answer.
3.  Format the output average with **two decimal places** by using the **printf** method.

## 01-1: Volume of a Cylinder

In **IntelliJ IDEA**, create a **New Project** called **Volume**.

In the **src** folder create a **Java class** file called *Volume.java* with the following source code

```java
public class Volume {  
    public static void main(String[] args) {  
        double radius = 2.0;  
        double area = Math.PI * radius * radius;  
        System.out.println("Area of the circle: " + area);  
    }  
}
```

1. Modify the program to use the **Math.pow()** method to square the radius instead of using multiplication.
2. Modify the program to calculate the volume of a cylinder: $V = \pi r^2 h$
3. Format the output the produce an answers with 1 decimal place.

## 01-2: Hypotenuse of a Right-Angled Triangle

In **IntelliJ IDEA**, create a **New Project** called **Hypotenuse**.

In the **src** folder create a **Java class** file called *Hypotenuse.java* with the following source code

```java
public class Hypotenuse {  
    public static void main(String[] args) {  
        int a = 3;  
        int b = 4;  
        int sum = a + b;  
        int hypotenuse = Math.sqrt(sum);  
        System.out.println("Hypotenuse" + hypotenuse);  
    }  
}
```

1. Run the code.  Can you figure out what is wrong? There are two mistakes in the code.
2. Format the output so that it has one decimal place.

## 01-3: Swap Digits *(using the modulus % operator)*

In **IntelliJ IDEA**, create a **New Project** called **Swap**.

In the **src** folder create a **Java class** file called *Swap.java* with the following source code

```java
public class Swap {  
    public static void main(String[] args) {  
        int number = 75;  
        int swap;  
  
        System.out.println("Tens: " + number / 10);  
        System.out.println("Remainder: " + number % 10);  
    }  
}
```

1. Modify the starter code so that it swaps the digits of the variable *number*. You should **save** the new value in a variable called *swap* and output its value use the method **println()**.  *Assume that the number you are swapping only has two digits.*  **Note:** The */* operator returns the **quotient** of a division of two integers, while the **modulus** operator *%* returns the **remainder** of a division of two integers.