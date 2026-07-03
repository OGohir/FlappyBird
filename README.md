# Flappy Bird (Java)

A simple recreation of the classic **Flappy Bird** game built using **Java**. This project was created to practice object-oriented programming, game loops, collision detection, keyboard input, and basic game physics.

---

## Features

* Smooth 60 FPS game loop
* Gravity and jumping mechanics
* Randomly generated pipes
* Collision detection
* Score tracking
* Game over screen
* Restart game by pressing **Space**
* Image-based graphics using Java Swing

---

# Technologies Used

* Java
* AWT Graphics
* Object-Oriented Programming (OOP)

---

# Project Structure

```text
Project
│
├── App.java          // Creates the game window
├── FlappyBird.java   // Main game logic
├── flappybird.png
├── flappybirdbg.png
├── toppipe.png
└── bottompipe.png
```

---

# How the Game Works

## App.java

Responsible for creating the game window.

It:

* Creates a `JFrame`
* Sets the window size
* Adds the `FlappyBird` panel
* Displays the game

---

## FlappyBird.java

Contains all of the game's functionality.

Responsibilities include:

* Loading images
* Drawing graphics
* Handling player input
* Applying gravity
* Moving pipes
* Detecting collisions
* Keeping score
* Restarting the game

---

# Bird

The bird stores:

```java
x
y
width
height
image
```

The bird is affected by gravity every frame and moves upward whenever the player presses the **Spacebar**.

---

# Pipes

Each pipe stores:

```java
x
y
width
height
image
passed
```

The `passed` variable ensures the player only receives one point for each pair of pipes.

Pipes continuously move from right to left across the screen.

---

# ⚙ Game Physics

### Horizontal Speed

```java
velocityX = -4;
```

Moves every pipe toward the left.

---

### Vertical Speed

```java
velocityY;
```

Controls how fast the bird moves vertically.

* Negative → Bird moves upward
* Positive → Bird falls downward

---

### Gravity

```java
gravity = 1;
```

Each frame:

```java
velocityY += gravity;
```

Gravity continuously pulls the bird downward.

---

# ⏱ Timers

The game uses two Swing timers.

## Game Loop

Runs approximately **60 times per second**.

Every frame it:

1. Updates object positions
2. Checks collisions
3. Updates the score
4. Redraws the screen

---

## Pipe Timer

Runs every **1500 milliseconds**.

Each time it runs:

* Creates one top pipe
* Creates one bottom pipe
* Adds both to the game

---



# Controls

| Key               | Action       |
| ----------------- | ------------ |
| Space             | Jump         |
| Space (Game Over) | Restart Game |

---

# Concepts Learned

* Object-Oriented Programming (OOP)
* Java Swing GUI Development
* Event Handling
* Keyboard Input
* Game Loops
* Timers
* Gravity Simulation
* Collision Detection
* ArrayLists
* Custom Rendering with Graphics
* Basic Game Physics

---

# Future Improvements

* Animated bird wings
* Sound effects
* High score tracking
* Difficulty scaling
* Pause menu
* Start screen
* Better pipe generation
* Multiple bird skins
* Mobile support
