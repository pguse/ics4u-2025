# Functions

## Exercises

In **IntelliJ IDEA**, create a **New Project** called **Points**.

In the **src** folder create a **Java class** file called *Points.java* with the following source code.

## 02-0: Slope

Create a **slope()** function and implement / use it in the **main()** function as shown below.  You will need to edi

```java
public class Point {  
    public static void main(String[] args) {  
        System.out.printf("Slope: %.2f", slope(1,-2, -4, 5));  
    }  
  
    public static double slope(int x1, int y1, int x2, int y2) {  
        return 1.0;  
    }  
}
```

## 02-1: Distance

Create a new file called *distance.rs* with the following source code

```rust
fn main(){
    println!("Distance between (1,2) and (7,10): {}", distance(1.0, 2.0, 7.0, 10.0));
}

fn distance(x1: f64, y1: f64, x2: f64, y2: f64) -> f64 {
    // Return the correct distance value
    x1 + y1 + x2 + y2
}
```

Write a function called **distance(x1: f64, y1: f64, x2: f64, y2: f64) -> f64** that calculates and **returns** an **f64** representing the distance between the points (x1,y1) and (x2,y2).

___

In **IntelliJ IDEA**, create a **New Project** called **Triangle**.

In the **src** folder create a **Java class** file called *Triangle.java* with the following source code.

Create the following two functions and implement / use them in the **main()** function.
## 02-2: Hypotenuse

Create a new file called *hypotenuse.rs* with the following source code

```rust
fn main(){
    println!("Hypotenuse - base: 3; height: 4: {}", hypotenuse(3.0, 4.0));
}

fn hypotenuse(a: f64, b: f64) -> f64 {
    // Return the correct hypotenuse value
    a + b
}
```

Write a function called **hypotenuse(a: f64, b: f64) -> f64** that calculates and **returns** an **f64** value representing the hypotenuse of a right triangle with sides a and b.

## 02-3: Triangle Area

Create a new file called *hypotenuse.rs* with the following source code

```rust
fn main(){
    println!("Hypotenuse - base: 3; height: 4: {}", hypotenuse(3.0, 4.0));
}

fn hypotenuse(a: f64, b: f64) -> f64 {
    // Return the correct hypotenuse value
    a + b
}
```

Write a function called **hypotenuse(a: f64, b: f64) -> f64** that calculates and **returns** an **f64** value representing the hypotenuse of a right triangle with sides a and b.

___

In **IntelliJ IDEA**, create a **New Project** called **Numbers**.

In the **src** folder create a **Java class** file called *Numbers.java* with the following source code.

Create the following two functions and implement / use them in the **main()** function.
## 02-4: Prime

Create a new file called *prime.rs* with the following source code

```rust
fn main(){
    println!("Is 15 prime? {}", is_prime(15));
}

fn is_prime(num: u32) -> bool {
    // Return the correct boolean value: true or false
    // depending upon whether the variable num is a prime number
    num == 1
}
```

Write a function called **is_prime(num: u32) -> bool** that determines whether an integer **num** is prime and **returns** a **bool** value ... either **true** or **false** . 

## 02-5: Greatest Common Divisor

Create a new file called *gcd.rs* with the following source code

```rust
fn main(){
    println!("GCD of 48 and 36: {}", gcd(48, 36));
}

fn gcd(mut m: u32, mut n: u32) -> u32 {
    // Return the correct greatest common divisor
    // between m and n
    m+n
}
```
Write a function called **gcd(m: u32, n: u32) -> u32** that **returns** a **u32** representing the greatest common divisor of the numbers m and n, assuming m > n. The best-known algorithm for finding a greatest common divisor is Euclid’s Algorithm.

**Euclid’s Algorithm** states that the **greatest common divisor** of two integers m and n is 

* n if n divides into m completely.
* However, if n does not divide into m completely, then the answer is the **greatest common divisor** of n and the **remainder** of m divided by n.
