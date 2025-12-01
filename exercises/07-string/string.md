# Using Strings in Java

In **IntelliJ IDEA**, create a **New Project** called StringExercises.

In the **src** folder create a **Java class** file called *StringExercises.java* with the following source code.

## Exercises

## 07-0:  Reverse

Write a method called ***reverse(String s)*** that takes a string as a parameter and returns the reversed version of the string.  
_Hint:_ Use `charAt()` 

---
## 07-1:  Vowels

Create a method called ***numVowels(String s)*** that returns the number of vowels in a given string.  
_Hint:_ Convert the string to lowercase and check each character against a set of vowels.

---
## 07-2:  Palindrome

Create a method called ***isPalindrome(String s)*** that checks if a given string is a *palindrome* *(reads the same forwards and backwards)*.  It should return true for a palindrome.
_Hint:_ Compare the original string with its reversed version.

---
## 07-3:  Number of Substrings

Create a method called ***numSubstring(String s, String sub)*** that takes as parameters a main string and a substring. It should return how many times the substring appears in the main string.  
_Hint:_ Use `indexOf()` in a loop.

---
## 07-4:  Replace Spaces

Create a method called ***replaceSpaces(String s)*** that replaces all spaces in a string with underscores (`_`) and returns the new String.  
_Hint:_ Use `replace()` or `replaceAll()`.

---
## 07-5:  Extract Initials from a Full Name

Create a method called ***initials(String name)*** that takes a full name as a parameter and returns their initials (e.g., "John Doe" → "J.D."). as a String
_Hint:_ Use `split(" ")` and `charAt(0)`.

---

## 07-6:  Count Words in a Sentence

Create a method called ***countWords(String s)*** that counts the number of words in a sentence provided as a parameter, and returns the number.  
_Hint:_ Use `split("\\s+")` to separate words.