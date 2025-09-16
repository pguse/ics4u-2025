
# Guessing Game

We are going to build a **Guessing Game** similar to what you may have created with **Python** in the past.

## STEP #0

In **IntelliJ IDEA**, create a **New Project** called **GuessingGame**.

In the **src** folder create a **Java class** file called *GuessingGame.java* with the following source code.

Copy the following **starter code** (see below) into your *GuessingGame.java* file.
## Starter Code

```java
import java.util.Scanner;  
  
public class GuessingGame {  
    public static void main(String[] args) {  
        int min = 1;  
        int max = 100;  
        // Generate a random whole number between 1 and 100  
  
        // STEP #1 - Modify the next line so that it generates        
        // a random whole number between 1 and 100, including the        
        // end points of the interval        
        
        int randomNum = (int) Math.random();  
  
        System.out.println("Welcome to the Guessing Game");  
        System.out.println("I'm thinking of a number between " + min + " and " + max);  
        System.out.println("Can you guess what it is?");  
  
        int guess = -1;  
        Scanner scanner = new Scanner(System.in);  
  
        while (guess != randomNum){  
            // User inputs a number  
            System.out.print("Please enter a number: ");  
  
            // Read the integer  
            guess = scanner.nextInt();  
            // Give the user feedback  
            System.out.println("You entered: " + guess);  
  
            // STEP #2 - Respond to the user.  
            // Is their guess too high, too low or correct? Respond            
            // appropriately.  
            // STEP #3 - Use a counter to keep track of how many guesses           
		    // were made.  The user should be allowed to make only 7 guesses.      
		}  
        // STEP #4 - Let the user know how many guesses they made.  
  
	    // STEP #5 - If the user guesses correctly, congratulate them.  If not,    
	    // let the user know what the secret number was.    
	}  
}
```
## STEP #1

Modify the line
```java
int randomNum = (int) Math.random();
```
so that it generates a **random whole number** between **1** and **100**, including the end points of the interval.  What does **Math.random()** do?  Check [here](https://www.w3schools.com/java/ref_math_random.asp) or [here](https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html#random--).

## STEP #2

Respond to the user.  Is their guess too high, too low or correct? Respond appropriately.  

## STEP #3

Use a **counter** to keep track of** **how many guesses** were made.  The user should be allowed to make only **7 guesses**.

## STEP #4

Let the user know how many guesses they made.  
  
## STEP #5

If the user guesses correctly, congratulate them.  If not, let the user know what the secret number was.  