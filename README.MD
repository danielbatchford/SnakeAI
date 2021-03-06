# Snake AI

### About

An AI implementation of the classic snake game, which achieves a near perfect score the majority of the time. Created using https://github.com/processing/processing.
A config file is included, where certain properties can be changed.

### Sample Run

![alt text][logo]

[logo]: https://github.com/danielbatchford/SnakeAI/blob/master/sample.gif?raw=true

### How To Run This Project

Run the .jar file located at `out\SnakeAI.jar` using `java -jar SnakeAI.jar`.

Properties can be edited in `config.properties`, located on the same path.

### Controls

- Use `p` to pause the game
- Use number keys `0-9` to control the speed of the game.

---

### Behaviour

This AI obeys the following logic:

- If a path from the head of the snake can be found:
  Attempt to find a path from the apple to the predicted location of the tail once the apple is reached (Accounting for the snake growing.) - uses a heuristic that minimises "jagged" movements. This path also assumes it can cross the rear end of the snake's body provided it is far enough from it's tail.

- If this path can be found, follow the path to the apple.

- Else, find the longest path from the head of the snake to it's own tail. This path is constantly updated and attempts are made to find a valid path to the apple each step.

### Credit

Credit to https://github.com/xaguzman/pathfinding for the pathfinding library.
