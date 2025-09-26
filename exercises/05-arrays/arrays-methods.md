# Arrays and Methods

## Exercises

## 05-0: Student Average

In **IntelliJ IDEA**, create a **New Project** called **StudentAverageMethod**.

In the **src** folder create a **Java class** file called *StudentAverageMethod.java* with the following source code.

Modify the starter code below so that the **average()** method returns the average of an array of integers as a **double** value.

```java
import java.util.Arrays;  
  
public class StudentAverageMethod {  
    public static void main(String[] args) {  
  
            int[] marks = {75, 82, 90, 95, 87, 80, 70, 92};  
  
            System.out.printf("Marks: %s\n", Arrays.toString(marks));  
            System.out.printf("Average:  %.2f", average(marks) );  
  
  
    }  
  
    public static double average(int[] m) {  
        return 0.0;  
    }  
}
```

## 05-1: Minimum

In **IntelliJ IDEA**, create a **New Project** called **MinimumArrayMethod**.

In the **src** folder create a **Java class** file called *MinimumArrayMethod.java* with the following source code.

Modify the starter code below so that the **minimum()** method returns the smallest value in an array of integers.

```java
import java.util.Arrays;  
  
public class MinimumArrayMethod {  
    public static void main(String[] args){  
            int[] marks = {75, 82, 90, 95, 87, 80, 70, 92};  
  
            System.out.printf("%s\n", Arrays.toString(marks));  
            System.out.printf("Minimum:  %d", minimum(marks));  
    }  
  
    public static int minimum(int[] m) {  
        return 0;  
    }  
}
```

## 05-2: Sum

In **IntelliJ IDEA**, create a **New Project** called SumArrayMethod**.

In the **src** folder create a **Java class** file called *SumArrayMethod.java* with the following source code.

Modify the starter code below so that the **sum()** method returns the sum of the values in an array of integers.

```java
import java.util.Arrays;  
  
public class SumArrayMethod {  
    public static void main(String[] args){  
        int[] marks = {75, 82, 90, 95, 87, 80, 70, 92};  
  
        System.out.printf("%s\n", Arrays.toString(marks));  
        System.out.printf("Sum:  %d", sum(marks));  
    }  
  
    public static int sum(int[] m) {  
        return 0;  
    }  
}
```

# 05-3: Tic-Tac-Toe Exercises

These exercises demonstrate how you might use a single-dimensional array in Java to store information in a grid-based game like Tic-Tac-Toe . In this case a 9 element array is used to store the 9 possible positions of the tic-tac-toe game. The index values of the array  match the grid positions given in the table below.

|   Tic  |  Tac   |  Toe   |
|:---:|:---:|:---:|
|  0  |  1  |  2  |
|  3  |  4  |  5  |
|  6  |  7  |  8  |


## Board Setup

The **board** array is filled initially with the values ```X```, ```O```, or ```-```.  In this game, this value will represent an empty square and be displayed as ```-```.  See the starter code below.

## Tasks

In **IntelliJ IDEA**, create a **New Project** called **TicTacToe**.

In the **src** folder create a **Java class** file called *TicTacToe.java* with the following source code.

```java
public class TicTacToe {  
    public static void main(String[] args) {  
            char[] board = {'X', 'O', 'X', 'O', 'X', '-', '-', 'X', 'O'};  
            display(board);  
    }  
  
    public static void display(char[] b) {  
        for (int i=0; i < b.length; i++) {  
            if (i % 3 == 0) {  
                System.out.printf("\n%c  ", b[i]);  
            } else {  
                System.out.printf("%c  ", b[i]);  
            }  
        }  
        System.out.println();  
        System.out.println("Win? " + isWin(b));  
        System.out.println("Tie? " + isTie(b));  
    }  
  
    public static boolean isWin(char[] b) {  
        return false;  
    }  
  
    public static boolean isTie(char[] b) {  
        return false;  
    }  
}
```

## 05-3-1:  Is there a Win?

Complete the **isWin()** function. It should return **true** if there is a win on the board.  Otherwise, it should return **false**. Remember, there are 8 possible ways to win in the tic-tac-toe game:  3 of the same kind _('X' or 'O')_ in any row _(3)_, any column _(3)_, or either diagonal _(2)_.

## 05-3-2:  Is there a Tie?
Complete the **isTie()** function. It should return **true** if there is a tie on the board.  Otherwise, it should return **false**.  A **tie** occurs if the board is filled, with 'X's and 'O's but there is **no win**.
