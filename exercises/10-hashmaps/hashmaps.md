# HashMap

## Exercises

## 10-0:  Number of Vowels - Text Entry

In **IntelliJ IDEA**, create a **New Project** called **NumberOfVowelsText**.

In the **src** folder create a **Java class** files called *NumberOfVowelsText.java* with the following source code.

```java
public static void main(String[] args){
	// add code here that includes user input
}

public static HashMap<char, int> numVowels(String s)() {
	// add code here that creates a HashMap
	// and returns it
}
```

This program should count the **number of vowels** *(a, e, i, o, u)* found in text entered by the user.  Use a `HashMap` collection to store the vowels as `keys` and the number of vowels as `values`. Create a function `numVowels(String s)` that uses the **String** read from the user and returns a `HashMap` with `keys` that are vowels and `values` that represent the number of vowels found.

## 10-1: Nucleotides

Create a new project called `Nucleotides`.

The genetic language of every living thing on the planet is DNA. DNA is a large molecule that is built from an extremely long sequence of individual elements called nucleotides. 4 types exist in DNA and these differ only slightly and can be represented as the following symbols: **A** for adenine, **C** for cytosine, **G** for guanine, and **T** for thymine."

Given a single stranded DNA string, compute how many times each nucleotide occurs in the string.

Using the starter code,

```java
public static void main(String[] args){
   String nucleo = "AGCTTTTCATTCTGACTGCAACGGGCAATATGTCTCTGTGTGGATTAAAAAAAGAGTGTCTGATAGCAGC";
   System.out.printf("%d", numNucleotides(nucleo));
}

public static HashMap<char,int>() numNucleotides(s: &str) {
	// add code here that creates a HashMap
	// and returns it
}
```

modify the function called `numNucleotides(String s)`  that returns a `HashMap` with keys that are the nucleotides:  **'A'**, **'C'**, **'G'**, and **'T'** and values that represent **how many times each nucleotide occurs** in a string called **strand**.

## 10-2:  Number of Vowels - Text File

In **IntelliJ IDEA**, create a **New Project** called **NumberOfVowelsTextFile**.

In the **src** folder create a **Java class** files called *NumberOfVowelsTextFile.java* with the following source code.

Your program should count the **number of vowels** *(a, e, i, o, u)* found in the text file called `emma.md`.  You will need to save the text file ``emma.md`` in the `src` folder of your project.  Use a `HashMap` collection to store the vowels as `keys` and the number of vowels as `values`. Create a function `numVowels(String s)` that uses the **String** read from the file and returns a `HashMap` with `keys` that are vowels and `values` that represent the number of vowels found. *Note: The method `numVowels(String s)` in this exercise should be the same as in exercise #0 above*.

```java
public static void main(String[] args){
	// add code here that includes reading a text file
	// called emma.md, found in the src folder
}

public static HashMap<char, int>() numVowels(String s) {
	// add code here that creates a HashMap
	// and returns it
}
```

## 10-3:  Number of Words - Text File

In **IntelliJ IDEA**, create a **New Project** called **NumberOfWordsTextFile**.

In the **src** folder create a **Java class** files called *NumberOfWordsTextFile.java* with the following source code.

Your program should count the **number of times** `Emma`, `friendship`, and `match` is found in the text file called `emma.md`.  You will need to save the text file `emma.md` in the `src` folder of your project.  Use a `HashMap` collection to store the words as `keys` and the number of each word as `values`. Create a function `numWords(String s, String[] words)` that uses the **String** read from the file and an array of words (e.g. `[`Emma`, `friendship`, `match] ) and returns a `HashMap` with `keys` that are words and `values` that represent the number of each word found in the text file.

```java
public static void main(String[] args){
	// add code here that includes reading a text file
	// called emma.md, found in the src folder
}

public static HashMap<String, int>() numVowels(String s, String[] words) {
	// add code here that creates a HashMap
	// and returns it
}
```

