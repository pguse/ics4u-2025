
# Arrays

## Exercises

## 05-0: Student Average

In **IntelliJ IDEA**, create a **New Project** called **StudentAverageArray**.

In the **src** folder create a **Java class** file called *StudentAverageArray.java* with the following source code.

1.  Modify the **starter code** below so that it averages 8 marks given in an integer array.  You will calculate the average, by using a **for-loop**.  ***Note:  You will need to use the idea of using an accumulator that you used in grade 11 with Python.***
2.  Output both the marks ***(all on one line)*** and the average, as shown in the example below.

```java
import java.util.Arrays;  
  
public class StudentAverageArray {  
    public static void main(String[] args) {  
        int[] scores = {90, 85, 95, 75, 80};  
        double average = 0;  
  
        // Simple array output as a string  
        System.out.printf("The scores are: %s\n", Arrays.toString(scores));  
  
        for (int i = 0; i < scores.length; i++) {  
            // Update the accumulator  
            average = scores[0];  
        }  
        average /= scores.length;  
        System.out.printf("The average is %.2f", average);  
    }  
}
```

**Example Output:**
```
The scores are: [90, 85, 95, 75, 80]
The average is 18.00
```

## 05-1: Reverse Output

In **IntelliJ IDEA**, create a **New Project** called **ReverseOutputArray**.

In the **src** folder create a **Java class** file called *ReverseOutputArray.java* with the following source code.

Modify the **starter code** below so that it displays the given array in reverse order.

```java
public class ReverseOutputArray {  
    public static void main(String[] args) {  
        int[] arr = {1, 2, 3, 4, 5};  
  
        // Modify the loop condition to reverse the array  
        for (int i = 0; i < arr.length; i++) {  
            System.out.print(arr[i] + " ");  
        }  
    }  
}
```

**Example Output**
```
5 4 3 2 1
```

## 05-2: Copying Elements Array-to-Array in Reverse Order

In **IntelliJ IDEA**, create a **New Project** called **CopyArrayReverseOrder**.

In the **src** folder create a **Java class** file called *CopyArrayReverseOrder.java* with the following source code.

Modify the **starter code** below to copy the elements in one array into another array, but in reverse order.  

```java
import java.util.Arrays;  
  
public class CopyArrayReverseOrder {  
    public static void main(String[] args) {  
        int[] arr = {1, 2, 3, 4, 5};  
        int[] arr2 = new int[arr.length];  
  
        for (int i = 0; i < arr.length; i++) {  
            // Assign the last element of the original array  
	        // to the first element of the reversed array
	        // and continue in the same manner with the next element
	    }  
        System.out.println("Original Array: " + Arrays.toString(arr));  
        System.out.println("Reversed Array: " + Arrays.toString(arr2));  
    }  
}
```

**Example Output**
```
Original Array: [1, 2, 3, 4, 5]
Reversed Array: [5, 4, 3, 2, 1]
```

## 05-03: Maximum and Minimum Elements in an Array

In **IntelliJ IDEA**, create a **New Project** called **MaxMinArrayElements**.

In the **src** folder create a **Java class** file called *MaxMinArrayElements.java* with the following source code.

Modify the **starter code** below to find the **maximum** and **minimum** element in a given array of positive integers.  

```java
public class MaxMinArrayElements {  
    public static void main(String[] args) {  
        int[] arr = {40, 25, 15, 70, 60, 10};  
        int max = arr[0];  
        int min = arr[0];  
        for (int i = 1; i < arr.length; i++) {  
            // Check if the current element is greater than the max element  
  
            // Check if the current element is less than the min element        }  
        System.out.println("Max: " + max);  
        System.out.println("Min: " + min);  
    }  
}
```

For a given array: [40, 25, 15, 70, 60, 10]

**Example Output**
```
Maximum: 70
Minimum: 10
```
