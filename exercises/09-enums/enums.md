
# Using Enums in Java

## Exercises

Complete the following exercises.

## 14-0:  Traffic Light System

In **IntelliJ IDEA**, create a **New Project** called **TrafficLights**.

In the **src** folder create a **Java class** files called *TrafficLights.java* with the following source code.

   - Create an `enum` named `TrafficLight` with three variants: `Red`, `Yellow`, and `Green`.
   - Implement a method `duration()` that returns the duration each light stays on (e.g., `Red` for 30 seconds, `Yellow` for 5 seconds, and `Green` for 60 seconds).

## 14-1:  Shape Calculation

In **IntelliJ IDEA**, create a **New Project** called **Shapes**.

In the **src** folder create a **Java class** files called *Shapes.java* with the following source code.

   - Define an `enum` `Shape` with variants: `Circle`, `Square`, and `Rectangle`.
   - Each variant should **hold data** relevant to that shape (e.g., radius for `Circle`, side length for `Square`, and width and height for `Rectangle`).
   - Implement methods to calculate the area for each shape.

## 14-2:  Card Deck Management

In **IntelliJ IDEA**, create a **New Project** called **CardDeck**.

In the **src** folder create a **Java class** files called *CardDeck.java* with the following source code.

   - Create an `enum` `Suit` for the four suits in a deck of cards: `Hearts`, `Diamonds`, `Clubs`, and `Spades`.
   - Create another `enum` `Rank` for the ranks in a deck (e.g., `Two`, `Three`, `Four`, up to `Ace`).
   - Define a `class` `Card` that uses these [enums](/notes/13-enums/enums.md) to represent a playing card.
   - **Write a function** to create a full deck of cards (52 cards) and **another function** to deal a card from this deck.