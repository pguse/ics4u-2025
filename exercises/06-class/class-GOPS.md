

# Designing Classes in Java - Game of Pure Strategy Project

In **IntelliJ IDEA**, create a **New Project** called **GameOfPureStrategy**.

In the **src** folder create **Java class** files called *Main.java*, *Card.java*, *Deck.java*, and *Hand.java* with the following source code.

## Starter Code

```java
// Main.java  
import java.util.ArrayList;  
  
public class Main {  
    public static void main(String[] args) {  
        System.out.println("Welcome to the Game of Pure Strategy!");  
        // Start the game  
        Deck deck = new Deck();  
        Hand player = new Hand(deck, 13);  
        Hand computer = new Hand(deck, 13);  
        Hand prizes = new Hand(deck, 13);  
        ArrayList<Card> player_prizes = new ArrayList<>();  
        ArrayList<Card> computer_prizes = new ArrayList<>();  
  
        // Shuffle the prizes  
        prizes.shuffle();  
        // Shuffle the computer's cards  
        computer.shuffle();  
  
        // TODO  
        // Display the prize  
        System.out.printf("Prize: %s", prizes.playCard(0));  
        // Remove a card from the computer's shuffled hand  
        // Ask the player to select a card to play        
        // Output and Compare the cards        
        // If the player wins, they get the prize        
        // If the computer wins, the prize goes to the computer        
        // If it's a tie, the prize goes to the computer        
        // Repeat until all prizes are won        
        // Display the winner        
        // End the game    }  
}
```


```java
// Card.java  
public class Card {  
    public enum Suit {CLUBS, DIAMONDS, HEARTS, SPADES};  
    public enum Rank {TWO, THREE, FOUR, FIVE, SIX, SEVEN,  
        EIGHT, NINE, TEN, JACK, QUEEN, KING, ACE};  
  
    private Rank rank;  
    private Suit suit;  
  
    public Card(Rank rank, Suit suit) {  
        this.rank = rank;  
        this.suit = suit;  
    }  
  
    public Rank getRank() {  
        return rank;  
    }  
  
    public Suit getSuit() {  
        return suit;  
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
import java.util.ArrayList;  

public class Deck {  
  
    private ArrayList<Card> cards;  
  
    public Deck() {  
        cards = new ArrayList<>();  
        for (Card.Suit suit : Card.Suit.values()) {  
            for (Card.Rank rank : Card.Rank.values()) {  
                cards.add(new Card(rank, suit));  
            }  
        }  
    }  
  
    public ArrayList<Card> dealCards(int numCards) {  
        ArrayList<Card> dealtCards = new ArrayList<>();  
        for (int i = 0; i < numCards; i++) {  
            dealtCards.add(cards.removeFirst());  
        }  
        return dealtCards;  
    }  
  
    public void shuffle(){  
        for(int i = 0; i < cards.size(); i++){  
            // Random index 0 -> 51 (inclusive)  
            int randomIndex = (int)(Math.random() * cards.size());  
            // Cards randomly moved to the end  
            Card temp = cards.remove(i);  
            cards.add(temp);  
        }  
    }  
}
```

```java
// Hand.java  

import java.util.ArrayList;  
  
public class Hand {  
    private ArrayList<Card> cards;  
    private Deck deck;  
  
    public Hand(Deck deck, int numCards) {  
        this.deck = deck;  
        cards = this.deck.dealCards(numCards);  
    }  
  
    public Card playCard(int index){  
        return cards.remove(index);  
    }  
  
    public void shuffle(){  
        for(int i = 0; i < cards.size(); i++){  
            // Random index 0 -> 51 (inclusive)  
            int randomIndex = (int)(Math.random() * cards.size());  
            // Random cards are moved to the end  
            Card temp = cards.remove(i);  
            cards.add(temp);  
        }  
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

## 06-0:  Complete the Game of Pure Strategy

Follow the comments provided in the **main()** method to complete the project

```java
// TODO  
// Display the prize    
// Remove a card from the computer's shuffled hand  
// Ask the player to select a card to play  
// Output and Compare the cards  
// If the player wins, they get the prize  
// If the computer wins, the prize goes to the computer  
// If it's a tie, the prize goes to the computer  
// Repeat until all prizes are won  
// Display the winner  
// End the game
```

