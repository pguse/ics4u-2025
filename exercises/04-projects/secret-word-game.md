
# Secret Word Game

We are going to build a **Secret Word Game** as a follow-up to our Guessing Game project

## STEP #0

In **IntelliJ IDEA**, create a **New Project** called **SecretWordGame**.

In the **src** folder create a **Java class** file called *SecretWordGame.java* with the following source code.

Copy the following **starter code** (see below) into your *SecretWordGame.java* file.
## Starter Code

```java
import java.util.Arrays;  
import java.util.Scanner;  
  
public class SecretWordGame {  
    public static void main(String[] args){  
        // Create an array of words to choose from  
        String[] words = {"orange", "lemon", "apple", "banana", "grape", "strawberry", "blueberry", "mango", "watermelon", "pineapple"};  
        // Generate a random word from the word array  
        String secretWord = words[ (int) (Math.random() * words.length) ];  
        int numberOfChars = secretWord.length();  
  
		// For now let's know the secret word for testing purposes
        System.out.println(secretWord);  
  
        // Create an array of underscores equal to the length of the random word  
        char[] guess = new char[numberOfChars];  
        for (int i = 0; i < numberOfChars; i++) {  
            guess[i] = '_';  
        }  
        // Can we fill the array above another way?  
  
		System.out.println( Arrays.toString(guess) );
		
        // Choose an example of a user guess        
	    // Replace the next line with a user input line using the Scanner class        
	    char user_guess = 'e';  
  
        // Compare the user guess to each character in the random word. 
        // If there is a match, replace the corresponding underscore character
        // in the underscore array with the guessed letter.        
        for (int i = 0; i < numberOfChars; i++) {  
            if (secretWord.charAt(i) == user_guess) {  
                guess[i] = user_guess;  
            }  
        }  
  
        System.out.println( Arrays.toString(guess) );  
    }  
}
```
## STEP #1

Modify the line
```java
System.out.println( Arrays.toString(guess) );
```
so that it outputs a the current version of the word *(underscores and known characters)* without the brackets and commas

![[https://github.com/pguse/ics4u-2025/blob/main/images/step1.png]]
## STEP #2

Allow the user to input their letter guess using the **Scanner** class.  Refer back to the guessing game if you don't remember how to do this. You will next to use the **nextLine()** method, which returns a **String** instead of the **nextInt()** method that you used in the guessing game. You will need to convert the input from a **String** to a **char** data type in order to make comparisons with each letter in the word.

## STEP #3

Create a **game loop** so that the user can make repeated guesses.  The current version of the word should be displayed after each guess.

## STEP #4

Use a **score** to keep track of **how many incorrect letters** were guessed.  The user should **lose 10 points** for guessing an **incorrect letter**. The user should not lose points for guessing a correct letter. The **updated score** should be displayed at each stage of the game.

## STEP #5

End the game when the **score** becomes **zero** or when the word is correctly guessed.  If the score becomes **zero**, tell the user the secret word.
