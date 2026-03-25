# HashMap

## Exercises

## 10-0: Nucleotides

Create a new project called `Nucleotides`.

The genetic language of every living thing on the planet is DNA. DNA is a large molecule that is built from an extremely long sequence of individual elements called nucleotides. 4 types exist in DNA and these differ only slightly and can be represented as the following symbols: **A** for adenine, **C** for cytosine, **G** for guanine, and **T** for thymine."

Given a single stranded DNA string, compute how many times each nucleotide occurs in the string.

Using the starter code,

```java
public static void main(String[] args){
   String nucleo = "AGCTTTTCATTCTGACTGCAACGGGCAATATGTCTCTGTGTGGATTAAAAAAAGAGTGTCTGATAGCAGC";
   System.out.printf("%d", numNucleotides(nucleo));
}

public static HashMap<Character,Integer>() numNucleotides(String s) {
	// add code here that creates a HashMap
	// and returns it
}
```

modify the function called `numNucleotides(String s)`  that returns a `HashMap` with keys that are the nucleotides:  **'A'**, **'C'**, **'G'**, and **'T'** and values that represent **how many times each nucleotide occurs** in a string called **strand**.
## 10-1:  Number of Vowels - Text Entry

In **IntelliJ IDEA**, create a **New Project** called **NumberOfVowelsText**.

In the **src** folder create a **Java class** files called *NumberOfVowelsText.java* with the following source code.

```java
import java.util.HashMap;  
  
public class Main {  
    public static void main(String[] args) {  
        System.out.println("Counting vowels in a string:");  
    }  
  
    public static HashMap<Character, Integer> numVowels(String s) {  
        HashMap<Character, Integer> vowels = new HashMap<Character, Integer>();  
        // add code here  
        return vowels;  
    }  
}
```

This program should count the **number of vowels** *(a, e, i, o, u)* found in text entered by the user.  Use a `HashMap` collection to store the vowels as `keys` and the number of vowels as `values`. Create a function `numVowels(String s)` that uses the **String** read from the user and returns a `HashMap` with `keys` that are vowels and `values` that represent the number of vowels found.

## 10-2:  Number of Vowels - Text File

In **IntelliJ IDEA**, create a **New Project** called **NumberOfVowelsTextFile**.

In the **src** folder create a **Java class** files called *NumberOfVowelsTextFile.java* with the following source code.

Your program should count the **number of vowels** *(a, e, i, o, u)* found in the text file called `emma.md`.  You will need to save the text file ``emma.txt`` in the `src` folder of your project.  Use a `HashMap` collection to store the vowels as `keys` and the number of vowels as `values`. Create a function `numVowels(String s)` that uses the **String** read from the file and returns a `HashMap` with `keys` that are vowels and `values` that represent the number of vowels found. *Note: The method `numVowels(String s)` in this exercise should be the same as in exercise #0 above*.

```java
public static void main(String[] args){
	// add code here that includes reading a text file
	// called emma.md, found in the src folder
}

public static HashMap<Character, Integer>() numVowels(String s) {
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

public static HashMap<String, Integer>() numVowels(String s, String[] words) {
	// add code here that creates a HashMap
	// and returns it
}
```

## 10-4:  Anagram

In **IntelliJ IDEA**, create a **New Project** called **Anagram**.

In the **src** folder create a **Java class** files called *Anagram.java* with the following source code.

```java
public static void main(String[] args){
	// add code here that includes reading input from the user
	// that includes two input strings
}

public static boolean anagram(String s1, String s2) {
	// add code here that creates a HashMap that stores the number
	// of each character in each string
	// If the HashMaps are the same, then the strings are anagrams
	return false;
}
```

An **anagram** is a word or phrase formed by **rearranging the letters** of another word or phrase, using all the original letters exactly once.

---

### Simple Examples

|Original|Anagram|
|---|---|
|`"listen"`|`"silent"`|
|`"earth"`|`"heart"`|
|`"eat"`|`"tea"` or `"ate"`|
|`"race"`|`"care"`|

---

### The Key Rules

1. **Same letters** — every letter from the original must be used
2. **Same frequency** — if a letter appears twice in the original, it must appear twice in the anagram
3. **Order doesn't matter** — the letters are simply rearranged

---

### How It Connects to the HashMap Exercise

In Exercise 3, anagrams were detected by **sorting the characters** of each word alphabetically and using that as a HashMap key:

- `"eat"` → sorted → `"aet"`
- `"tea"` → sorted → `"aet"`
- `"ate"` → sorted → `"aet"`

Since all three produce the same key `"aet"`, they get grouped together in the HashMap as a family of anagrams. This is an efficient and elegant way to detect them without comparing every word against every other word.

## 10-5:  Isomorphic Strings

In **IntelliJ IDEA**, create a **New Project** called **IsomorphicStrings**.

In the **src** folder create a **Java class** files called *IsomorphicStrings.java* with the following source code.

```java
public static void main(String[] args){
	// add code here that includes reading input from the user
	// that includes two input strings
}

public static boolean isomorphic(String s1, String s2) {
	// add code here that creates a HashMap that stores the mapping
	// of characters from one string to another
	// If the mapping of characters is 1-to-1, then the strings are isomorphic
	return false;
}
```
### Examples

Here are two clear examples of isomorphic strings:

---

### ✅ Example 1: `"egg"` and `"add"`

These **are** isomorphic.

|Index|`s` char|`t` char|Mapping|
|---|---|---|---|
|0|`e`|`a`|`e → a`|
|1|`g`|`d`|`g → d`|
|2|`g`|`d`|`g → d` ✅ (consistent)|

Every `e` maps to `a`, and every `g` maps to `d` — the structure is identical.

---

### ✅ Example 2: `"paper"` and `"title"`

These **are** isomorphic.

|Index|`s` char|`t` char|Mapping|
|---|---|---|---|
|0|`p`|`t`|`p → t`|
|1|`a`|`i`|`a → i`|
|2|`p`|`t`|`p → t` ✅ (consistent)|
|3|`e`|`l`|`e → l`|
|4|`r`|`e`|`r → e`|

Each character in `"paper"` maps consistently to exactly one character in `"title"`, and no two different characters share the same mapping.

---

### ❌ Counterexample: `"foo"` and `"bar"`

These are **not** isomorphic.

|Index|`s` char|`t` char|Mapping|
|---|---|---|---|
|0|`f`|`b`|`f → b`|
|1|`o`|`a`|`o → a`|
|2|`o`|`r`|`o → r` ❌ (conflict!)|

`o` tries to map to both `a` and `r`, which breaks the 1-to-1 rule.

---

The key rule is: **same characters must always map to the same character**, and **no two different characters can map to the same character**.