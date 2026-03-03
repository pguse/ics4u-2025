Designing Classes in Java - Connect4  Project

In **IntelliJ IDEA**, create a **New Project** called **Connect4**.

In the **src** folder create **Java class** files called *Main.java*, *Token.java*, *Player.java*, and *Board.java* with the following source code.

## Starter Code

```java
// Main.java  
public class Main {  
    public static void main(String[] args) {  
        Board board = new Board();  
        Player player1 = new Player(Token.Color.RED, board);  
        Player player2 = new Player(Token.Color.YELLOW, board);  
        board.display();  
    }  
}
}
```


```java 
// Token.java  
// Class describing a Connect4 piece  
public class Token {  
    public enum Color {RED, YELLOW, EMPTY};  
    private Color color;  
  
    public Token(Color color) {  
        this.color = color;  
    }  
  
    public Color getColor() {  
        return color;  
    }  
  
    public String toString() {  
        return switch(color) {  
            case RED -> "🔴";  
            case YELLOW -> "🔵";  
            case EMPTY -> "⚫";  
        };  
    }  
}
```


```java
// Player.java   
import java.util.ArrayList;  
  
public class Player {  
  
    ArrayList<Token> pieces;  
    Board board;  
  
    public Player(Token.Color color, Board board) {  
        pieces = new ArrayList<Token>();  
        for (int i = 0; i < 21; i++){  
            pieces.add(new Token(color));  
        }  
        this.board = board;  
    }  
}
```


```java
// Board.java   
// Class describing a Connect4 board  
public class Board {  
    Token[][] board;  
  
    public Board() {  
        board = new Token[6][7];  
        for (int i = 0; i < 6; i++) {  
            for (int j = 0; j < 7; j++) {  
                board[i][j] = new Token(Token.Color.EMPTY);  
            }  
        }  
    }  
  
    public void display() {  
        for (int i = 0; i < 6; i++) {  
            for (int j = 0; j < 7; j++) {  
                System.out.print(board[i][j] + " ");  
            }  
            System.out.println();  
        }  
    }  
}
```
## Exercises

## 06-0:  Complete the Connect4 Game

Given the starter code,

1. Complete the following methods:

	- playToken() in the Player class
	- detectRowWin() in the Board class
	- detectColWin() in the Board class
	- detectDiagonalUpWin() in the Board class
	- detectDiagonalDownWin() in the Board class

2. Modify the `main()` method so that the game can be played with two players, entering moves from the command line.

