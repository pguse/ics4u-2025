# Designing Classes in Java

In **IntelliJ IDEA**, create a **New Project** called **RobotSimulator**.

In the **src** folder create two **Java class** files called *RobotSimulator.java* and *Robot.java* with the following source code.

```java
public class RobotSimulator {  
    public static void main(String[] args) {  
        Robot robot = new Robot(0, 0, "NORTH");
        robot.followInstructions("LAAARALA");  
        System.out.printf("Position: (%d, %d)  ", robot.getX(), robot.getY());  
        System.out.println(" Direction: " + robot.getDirection());  
    }  
}
```

```java
public class Robot {  
    private int x;  
    private int y;  
    private String direction;
      
    // Constructor  
    public Robot(int x, int y, String direction) {  
        this.x = x;  
        this.y = y;  
        this.direction = direction;  
    } 
     
    // Accessors  
    public int getX() {  
        return x;  
    }  
    public int getY() {  
        return y;  
    }  
    public String getDirection() {  
        return direction;  
    }  
    
    // Mutators  
    public void turnLeft(){  
        switch (direction) {  
            case "NORTH": direction = "WEST"; break;  
            case "EAST": direction = "NORTH"; break;  
            case "SOUTH": direction = "EAST"; break;  
            case "WEST": direction = "SOUTH"; break;  
        }  
    }  
    
    public void turnRight(){  
        // finish this code - similar to turnLeft  
    }  
    
    public void advance(){  
        // finish this code - update x and y based on direction  
    }  
  
    public void followInstructions(String instructions) {  
        for ( char instruction : instructions.toCharArray()) {  
            switch (instruction) {  
                case 'L': turnLeft(); break;  
                case 'R': turnRight(); break;  
                case 'A': advance(); break;  
            }  
        }  
    }  
  
    public String toString() {  
        // finish this code - return a string representation of the robot  
        return "";  
    }  
}
```
## Exercises

## 06-6:  Turn Right

Complete the **turnRight()** method

```java
public void turnRight(){  
        // finish this code - similar to turnLeft  
    } 
```

## 06-7:  Advance

Complete the **advance()** method

```java
public void advance(){  
        // finish this code - update x and y based on direction  
    }  
```

## 06-8:  Test

**Run your project** with the current version of the **main()** method, and determine whether your program is working properly.

```java
public static void main(String[] args) {  
      Robot robot = new Robot(0, 0, "NORTH");
      robot.followInstructions("LAAARALA");  
      System.out.printf("Position: (%d, %d)  ", robot.getX(), robot.getY());  
      System.out.println(" Direction: " + robot.getDirection());
}
```

## 06-9:  User Input

Change the following line in the **main()** method, so that the **user** can **input** their own set of instructions.  You will be using the **Scanner class** like you did in the **Guessing Game** project.

```java
robot.followInstructions("LAAARALA");  
```

The program should run something like this:

![[/images/output.png]]

## 06-10:  toString() method

Complete the **toString()** method, so that the Robot object can be output using a print() method. For example, in the main() method

```java
System.out.println(robot);
```

should output something like this:

```java
Position: (0, -1)  Direction: SOUTH
```

