# Minesweeper-AI-with-tensorflow.js

This code is modification of the real code by Shiffman Sir, here is the real code in p5.js: 

https://editor.p5js.org/codingtrain/sketches/-mz-ePoqd

https://thecodingtrain.com/challenges/71-minesweeper

# About the code
This code sets up a basic Minesweeper game with an AI opponent that makes random moves. It utilizes TensorFlow.js for a neural network model (though the model itself is not used in the game logic) and p5.js for canvas drawing and interaction.
 
## Use TensorFlow Model Setup:
- The createModel() function is defined to create a neural network model using TensorFlow.js.
- This model is a sequential model with one layer: a dense layer with softmax activation.
- The model is compiled with stochastic gradient descent (SGD) optimizer and categorical cross-entropy loss.

## Game Setup (setup() function):
- The setup() function is defined using p5.js.
- It creates a canvas with a size of 320x420 pixels.
- It initializes the Minesweeper grid (grid) and sets up the game by placing mines and calculating the number of neighboring mines for each cell.
- It sets an interval for making moves automatically (makeMove() function is called every second).
- It creates a "Start Again" button using the p5.js createButton() function.

## Game Logic:
- Various variables and functions for the game logic are defined, including Cell class, methods for showing cells, counting neighboring mines, revealing cells, flood filling, etc.
- The makeMove() function defines the logic for the AI's moves. It randomly selects a cell and reveals it. If the cell contains a mine, the game is over.
- The gameOver() function reveals all cells when the game ends.

## Drawing the Game (draw() function):
- The draw() function is defined using p5.js. It is called continuously and is responsible for rendering the game on the canvas.
- It clears the canvas, then iterates over the grid and draws each cell.
Additionally, it draws lines to enclose the grid.

