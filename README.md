# Assignment 3

thre lane dodge game is a C game where the player controls a character moving between three lanes to avoid falling obstacles.This game includes playsound and animation-

The features game has:
* Three-lane movement (left, middle, right)
* Player controls using arrow keys
* Randomly generated obstacles
* Continuous downward movement of obstacles

👉How the game works:
The user has following moves:
* The player moves left or right using **arrow keys**.
* Movement is restricted to **three lanes**: left, middle, and right.

### Obstacle Movement

* Obstacles appear at the top in a random lane and move downwards one step at a time.
* When an obstacle reaches the bottom row, it resets to a new random lane from the top.

### Collision Detection

* A collision occurs if an obstacle reaches the bottom row in the same lane as the player.
* On collision:

  * Background music stops
  * Collision sound plays
  * Game ends with “GAME OVER” message

### Game Loop

The game runs inside an infinite loop performing these steps in order:

1. Detect player input for left/right movement
2. Draw obstacles at their current vertical position
3. Draw player at the bottom row
4. Check for collision
5. Move obstacles down one step
6. Reset obstacles when they reach the bottom
7. Repeat until collision occurs

---

## Concepts Demonstrated

* Infinite loops (`while` loop) for continuous gameplay
* Conditional statements for player movement and collision detection
* Random number generation (`rand()` and `srand()`) for obstacle lanes
* Console cursor manipulation for smooth screen updates (`SetConsoleCursorPosition`)
* Keyboard input handling without waiting for Enter (`_kbhit()` and `getch()`)
* Sound playback using WinMM library (`PlaySound()`)
* Basic game physics (player lane vs obstacle lane)

## How to Play

1. Run the program in a console window.
2. The player character appears at the bottom row.
3. Obstacles fall from the top in random lanes.
4. Move left or right to dodge obstacles.
5. If an obstacle collides with the player, the game ends
