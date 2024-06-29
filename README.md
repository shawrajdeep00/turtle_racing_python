# Turtle Racing using Python

Welcome to the Turtle Racing project! This Python project simulates a turtle race using the `turtle` module. The project allows users to specify the number of racing turtles (between 2 and 10), and then the turtles race to the top of the screen. The winner is the first turtle to cross the finish line.

## Project Files

- `turtleRacing.py`: The main Python script that runs the turtle race.
- `final_output_race.png`: Screenshot of the race's final output.
- `outputWindow_screenrecord.webm`: Screen recording of the turtle race.

## Requirements

- Python 3.x

## How to Run the Project

1. **Clone the Repository**:
   ```sh
   git clone https://github.com/shawrajdeep00/turtle_racing_python.git
   cd turtle_racing_python
   ```

2. **Run the Script**:
   ```sh
   python turtleRacing.py
   ```

3. **Enter the Number of Racers**:
   When prompted, enter the number of turtles that will participate in the race (between 2 and 10).

## Explanation of the Code

The `turtleRacing.py` script contains the following sections:

### Imports

- Import the `turtle` module.
- Import the `time` module.
- Import the `random` module.

### Constants

- Set `WIDTH` and `HEIGHT` for the screen dimensions.
- Define a list `COLORS` containing the colors for the turtles.

### Function Definitions

#### `get_number_of_racers()`

**Pseudocode:**

```
Function get_number_of_racers()
    Set racers to 0
    While True
        Prompt user to enter number of racers between 2 and 10
        If input is numeric
            Convert input to integer
        Else
            Print error message and continue loop
        If racers is between 2 and 10
            Return racers
        Else
            Print error message and continue loop
```

#### `race(colors)`

**Pseudocode:**

```
Function race(colors)
    turtles = create_turtles(colors)
    While True
        For each turtle in turtles
            Move turtle forward by random distance between 1 and 20
            Get turtle's current position
            If turtle's position >= finish line
                Return turtle's color as winner
```

#### `create_turtles(colors)`

**Pseudocode:**

```
Function create_turtles(colors)
    Initialize empty list turtles
    Calculate horizontal spacing between turtles
    For each color in colors
        Create new turtle
        Set turtle color
        Set turtle shape to "turtle"
        Turn turtle to face upward
        Lift turtle pen
        Set turtle starting position
        Put turtle pen down
        Add turtle to turtles list
    Return turtles
```

#### `init_turtle()`

**Pseudocode:**

```
Function init_turtle()
    Create screen object
    Set up screen with specified width and height
    Set screen title to "Turtle Racing!"
```

### Main Program

**Pseudocode:**

```
Call get_number_of_racers()
Call init_turtle()
Shuffle COLORS list
Select subset of colors based on number of racers
Call race(colors)
Print winner's color
Wait for 5 seconds before closing window
```

## Detailed Explanation of the Script

### Imports

The script imports three modules:
- `turtle`: Provides the Turtle graphics library for creating the race.
- `time`: Allows for pauses in the script to control the flow.
- `random`: Generates random numbers to simulate the turtles' movements.

### Constants

- `WIDTH` and `HEIGHT`: These constants set the dimensions of the window where the race will take place.
- `COLORS`: A list of colors to distinguish each racing turtle.

### Function Definitions

#### `get_number_of_racers()`

This function handles user input to determine the number of turtles participating in the race. It ensures the input is valid and within the specified range (2 to 10).

#### `race(colors)`

This function conducts the race. It moves each turtle forward by a random distance in each iteration until one turtle reaches or crosses the finish line. The function returns the color of the winning turtle.

#### `create_turtles(colors)`

This function initializes the turtles. It creates a list of turtle objects, sets their colors, shapes, and initial positions on the screen.

#### `init_turtle()`

This function sets up the turtle graphics screen, configuring its dimensions and title.

### Main Program

The main part of the script orchestrates the race. It:
1. Gets the number of racers from the user.
2. Initializes the turtle screen.
3. Shuffles the colors and selects a subset based on the number of racers.
4. Starts the race and determines the winner.
5. Prints the winner's color and waits for 5 seconds before closing the window.

## Relevant Information from the Python Turtle Module

The `turtle` module in Python provides a simple way to draw shapes and create graphics. For more detailed information, you can refer to the official [Python Turtle Documentation](https://docs.python.org/3/library/turtle.html).

Key functions used in this project include:
- `turtle.Turtle()`: Creates a new turtle.
- `turtle.Screen()`: Creates a screen object.
- `Turtle.forward(distance)`: Moves the turtle forward by the specified distance.
- `Turtle.left(angle)`: Turns the turtle left by the specified angle.
- `Turtle.penup()`: Lifts the pen, so the turtle does not draw when moving.
- `Turtle.pendown()`: Puts the pen down, so the turtle draws when moving.
- `Turtle.setpos(x, y)`: Sets the turtle's position to the specified coordinates.
- `Screen.setup(width, height)`: Sets the width and height of the window.
- `Screen.title(title)`: Sets the title of the window.

## Future prospects
Implementing the Turtle Racing project is a fun and engaging way to practice programming fundamentals. It helps you get comfortable with key concepts like loops, conditionals, and functions, while also introducing you to the `turtle` graphics module in Python. By working on this project, you’ll also learn how to handle user input and use random number generation to create dynamic outcomes. In real life, these skills can open doors to more complex projects, like building graphical user interfaces, animations, or even simple games. This project not only strengthens your coding abilities but also sparks creativity, making it a great stepping stone for future development endeavors.


By following the steps and explanations provided, you can easily understand and recreate the turtle racing project from scratch. Enjoy the race!
