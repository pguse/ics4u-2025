
# Designing Classes in Java - Poker Project

In **IntelliJ IDEA**, create a **New Project** called **Poker**.

In the **src** folder create **Java class** files called *Poker.java*, *Card.java*, *Deck.java*, and *Hand.java* with the following source code.

## Starter Code

```java
// Poker.java  
public class Poker {  
    public static void main(String[] args) {  
        // Creating a hand from a deck  
        Deck deck = new Deck();  
        deck.shuffle();  
        Hand hand = new Hand(deck);  
        hand.display();  
  
        // Testing different types of hands  
        Hand testHand = new Hand();  
        testHand.addCard(Card.Rank.ACE, Card.Suit.SPADES);  
        testHand.addCard(Card.Rank.KING, Card.Suit.SPADES);  
        testHand.addCard(Card.Rank.QUEEN, Card.Suit.SPADES);  
        testHand.addCard(Card.Rank.JACK, Card.Suit.SPADES);  
        testHand.addCard(Card.Rank.TEN, Card.Suit.SPADES);  
        testHand.display();  
    }  
}
```


```java
// Card.java  
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
        String suit = switch(this.suit) {  
            case CLUBS -> "♣️";  
            case DIAMONDS -> "♦️";  
            case HEARTS -> "♥️";  
            case SPADES -> "♠️";  
        };  
  
        String rank = switch(this.rank) {  
            case ACE -> "A";  
            case TWO -> "2";  
            case THREE -> "3";  
            case FOUR -> "4";  
            case FIVE -> "5";  
            case SIX -> "6";  
            case SEVEN -> "7";  
            case EIGHT -> "8";  
            case NINE -> "9";  
            case TEN -> "10";  
            case JACK -> "J";  
            case QUEEN -> "Q";  
            case KING -> "K";  
        };  
  
        return  rank + suit;  
    }  
}
```


```java
// Deck.java  
public class Deck {  
  
    private Card[] cards;  
    private int currentPosition;  
  
    public Deck() {  
        cards = new Card[52];  
        int index = 0;  
        for (Card.Suit suit : Card.Suit.values()) {  
            for (Card.Rank rank : Card.Rank.values()) {  
                cards[index] = new Card(rank, suit);  
                index++;  
            }  
        }  
        currentPosition = 0;  
    }  
  
    public Card[] dealCards(int numCards) {  
        if (numCards <= 0 || currentPosition + numCards > cards.length) {  
            return new Card[0];  
        }  
  
        Card[] dealtCards = new Card[numCards];  
        for (int i = 0; i < numCards; i++) {  
            dealtCards[i] = cards[currentPosition];  
            currentPosition++;  
        }  
        return dealtCards;  
    }  
  
    public void shuffle(){  
        for(int i = 0; i < cards.length; i++){  
            // Random index 0 -> 51 (inclusive)  
            int randomIndex = (int)(Math.random() * cards.length);  
            // Cards are swapped  
            Card temp = cards[i];  
            cards[i] = cards[randomIndex];  
            cards[randomIndex] = temp;  
        }  
    }  
}
```


```java
// Hand.java  
public class Hand {  
    private Card[] cards;  
    private int currentPosition;  
  
    public Hand(Deck deck) {  
        cards = deck.dealCards(5);  
        currentPosition = 0;  
    }  
  
    public Hand() {  
        this.cards = new Card[5];  
        currentPosition = 0;  
    }  
  
    public void addCard(Card.Rank rank, Card.Suit suit){  
        if (currentPosition >= cards.length) return;  
        cards[currentPosition] = new Card(rank, suit);  
        currentPosition++;  
    }  
  
    public boolean isFlush(){  
        return false;  
    }  
  
    public boolean isStraight(){  
        return false;  
    }  
  
    public boolean isPair(){  
        return false;  
    }  
  
    public void display(){  
        for(Card card : cards){  
            System.out.printf("%s ", card);  
        }  
        System.out.println();  
    }  
}
```
## Exercises

## 06-0:  isFlush(), isStraight(), and isPair() methods

Complete and test the following methods in the Hand class

### Flush
```java
public boolean isFlush(){  
    return false;  
}  
```

## Note

In order to complete the next two methods, it will be very important that you are working with a sorted hand.  To do this, we should add a `sort()` method to the `Hand` class.  Here is a suggested implementation that uses the **selection sort** algorithm.  Although this algorithm is not very efficient (`O(n^2)`), we are dealing with only 5 cards, so it will be sufficiently fast for our use case

```java
public class Hand {
	// attributes, constructors, and other methods are here
	
	public void sort(){  
	    // Using selection sort since we are only dealing 5 cards  
	    int minIndex;  
	    for(int pos = 0; pos < cards.length - 1; pos++){  
	        minIndex = pos;  
	        for(int i = pos; i < cards.length; i++){  
	            if (cards[i].getRank().compareTo(cards[minIndex].getRank()) < 0) {  
	                minIndex = i;  
	            }  
	        }  
	        // swap cards so the minimum rank is at pos  
	        Card temp = cards[pos];  
	        cards[pos] = cards[minIndex];  
	        cards[minIndex] = temp;  
	    }  
	}
}

```

In order for this to work, you must have created a `getRank()` method in your `Card` class.  For example,
```java
public class Card {
	// attributes, constructor, and other methods
	
	public Rank getRank() {  
	    return rank;  
	}
}
```

You also need to realize that the order of the `Card.Rank` enums implies an order from **smallest to largest**.  Since we are playing poker, aces are considered high cards, so you will need to change the code in the `Card` class to look like this

```java
public enum Rank {TWO, THREE, FOUR, FIVE, SIX, SEVEN,  
    EIGHT, NINE, TEN, JACK, QUEEN, KING, ACE};
```
### Straight
```java
public boolean isStraight(){  
    return false;  
}  
```

### Pair
```java
public boolean isPair(){  
    return false;  
}
```