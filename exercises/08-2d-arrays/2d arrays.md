# 2D Arrays

In **IntelliJ IDEA**, create a **New Project** called **TwoDimArrays**.

In the **src** folder create a **Java class** file called *TwoDimArrays.java* with the following source code.

## Exercises

## 08-0:  Print Matrix

Create a function called **printMatrix()** that outputs a 2-dimensional array in a grid format.

```java
public static void printMatrix() {
	// use a for loop along with Arrays.toString()
	// to output each row on a new line
}
```
## 08-1:  Random Matrix

Create a function called **randomMatrix()** that creates a 2-dimensional array, with **3** rows and **3** columns, made up of 0's and 1's chosen randomly.  The function should return the array that gets created.

```java
public static int[][] randomMatrix(int rows, int cols) {
    return new int[rows][cols];
}
```

## 08-2:  Find

Create a function called **find()** that searches for an integer **x** in a 2-dimensional integer array **m**.  It should return the position **[row, col]** if it finds it, otherwise it returns **[-1,-1]**.

```java
public static int[] find(int[][] m, int x){
    int[] loc = {-1, -1};
    // Search for x using a nested loop
    return loc
}
```

## 08-3:  Maximum

Create a function called **max()** that returns the maximum value in a 2-dimensional  integer array **m**.

```java
public static int max(int[][] m) {
    return 0;
}
```

## 08-4:  Addition

Create a function called **add** that adds two integer **2D arrays**, of the same size and returns a new 2-dimensional array. **Addition of arrays** produces a new array of the same size by adding **elements** from the original arrays with the **same row and column**, and placing the **sum** in the **same position** in the new array.  You can assume that the arrays have matching sizes.

```java
public static int[][] add(int[][] m, int[][] n) {
	return new int[3][3];
}
```

## 08-5:  Scalar

Create a function called **scalar()** that multiplies every value of a **2D array** **m** by the value **k**.

```java
public static int[][] scalar(int[][] m, int k) {
	return new int[3][3];
}
```
