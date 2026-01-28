
# Using Enums in Java

## Exercises

Complete the following exercises.

## 14-0:  Traffic Light System

In **IntelliJ IDEA**, create a **New Project** called **TrafficLights**.

In the **src** folder create a **Java class** files called *TrafficLights.java* with the following source code.

   - Create an `enum` named `TrafficLight` with three variants: `Red`, `Yellow`, and `Green`.
   - Implement a method `duration()` that returns the duration each light stays on (e.g., `Red` for 30 seconds, `Yellow` for 5 seconds, and `Green` for 60 seconds).
   - In the **main()** method, create a variable of type `TrafficLight`, and output the duration using the `duration()` method.

### Example Output

```
Duration of RED: 30 seconds
```
## 14-1:  Finance

In **IntelliJ IDEA**, create a **New Project** called **Finance**.

In the **src** folder create a **Java class** files called *Finance.java* with the following source code.

   - Create an `enum` named `Currency` with four variants: `USD`, `EUR`, `GBP`, and `CAD`.
   - Implement the methods `convertFrom()`, to convert an amount from, CAD, for example, to this currency  and `convertTo()`, to convert an amount from this currency back to CAD, for example
   - In the **main()** method, iterate *(using a for loop)* over all the values (`USD, EUR, GBP, CAD`) and output the equivalent amounts in US dollars.
   - In the **main()** method, pick a currency other than CAD.  Output the equivalent amount in that currency of 100 CAD dollars

```java
public class Finance {
    enum Currency {
        USD("US Dollar", 1.0),
        EUR("Euro", 0.84),
        GBP("British Pound", 0.73),
        CAD("Canadian Dollar", 1.37);

        private String displayName;
        private double rateToBase;

        // Constructor
        Currency(String displayName, double rateToBase) {
            this.displayName = displayName;
            this.rateToBase = rateToBase;
        }

        // Getter for display name
        public String getDisplayName() {
            return displayName;
        }

        // Method to convert an amount from, CAD, for example, to 
        // this currency
        public double convertFrom(double amount) {
            return 0.0;
        }

        // Method to convert an amount from this currency back to CAD,
        // for example
        public double convertTo(double amount) {
            return 0.0;
        }
    }

    public static void main(String[] args) {
        double amountInUSD = 100.0;
        double amountInCAD = 100.0;
        
	    // Iterate (using a for loop) over all the values and output
	    // the equivalent amount of 100 US dollars in each currency.
	    
	    // Pick a currency other than CAD.  Output the equivalent amount in
	    // that currency of 100 CAD dollars
    }
}
```

### Example Output:

```
$100.00 USD is equivalent to 100.00 USD (US Dollar)
$100.00 USD is equivalent to 84.00 EUR (Euro)
$100.00 USD is equivalent to 73.00 GBP (British Pound)
$100.00 USD is equivalent to 137.00 CAD (Canadian Dollar)

$100.00 CAD is equivalent to 72.99 USD (US Dollar)
```
## 14-2:  Card Deck Modelling

In **IntelliJ IDEA**, create a **New Project** called **CardDeck**.

In the **src** folder create a **Java class** files called *CardDeck.java* with the following source code.

   - Create an `enum` `Suit` for the four suits in a deck of cards: `Hearts`, `Diamonds`, `Clubs`, and `Spades`.
   - Create another `enum` `Rank` for the ranks in a deck (e.g., `Two`, `Three`, `Four`, up to `Ace`).
   - Define a `class` `Card` that uses these enums to represent a playing card.
   - Write **method** `newDeck()` to create a full deck of cards (52 cards) and **another method** `dealCard()` to deal a card from this deck.

### Starter Code

Here is how the `Card` class may be constructed

```java
public class Card {  
    public enum Suit {CLUBS, DIAMONDS, HEARTS, SPADES};  
    public enum Rank {ACE, TWO, THREE, FOUR, FIVE, SIX, SEVEN,  
                      EIGHT, NINE, TEN, JACK, QUEEN, KING};  
  
    private Rank rank;  
    private Suit suit;  
  
    public Card(Rank rank, Suit suit) {  
        this.rank = rank;  
        this.suit = suit;  
    }  
  
    public String toString() {  
        return rank + " of " + suit;  
    }  
}
```

You should create this class in a **separate file** called `Card.java`.