# Analysis-of-Three-Dimensional-Tic-Tac-Toe-in-Python
Using computer science to determine that a game three dimensional tic-tac-toe cannot end in a draw.

Tic-tac-toe is a universally known game. What has helped the game become almost universal common knowledge is the simplicity of the rules and of the play style. Those two factors are also the downfall of the game: tic-tac-toe is uninteresting. When two experienced players play a match, it should always end in a draw. In the case of three dimensional tic-tac-toe, no matter how excellent the players are, one will always win. A game of three dimensional tic-tac-toe cannot end in a draw.

## Checking for a Drawn Three Dimensional Game

*below is an explanation of the program checkFor3DDraw.py*

A game of three dimensional is best understood as a combination of three two dimensional games, stacked on top of each other. With this definition, it becomes much simpler to extend work into the third dimension. When talking about a three dimensional game, I use the terms plane index, and dimensional index. Plane index refers to the positioning in the second dimension, running from 0 to 8, with 0 at the top left, and 8 at the bottom right. Dimensional index refers to the position in the stack of two dimensional games, running from 0 to 2, with 0 being the top, and 2 being the bottom.

To find out if a specific game ends in a draw, you need to rule out all the possible ways on winning. There are three main methods of winning a game of three dimensional tic-tac-toe. The first way is with all the winning tiles on the same plane, which would be done in the exact same way as a two dimensional game. The second way is with the same plane index, but a different dimensional index, a simpler explanation of this would be three tiles stacked on top of each other, to form three in a row. The third method of winning is a combination of the two listed prior. Three tiles in a row, but with both a different plane index and a different dimensional index. This is best visualized as forming the same lines as a two dimensional win, but going through all three layers.

This code works by first generating all possible combinations of moves that create a two dimensional game. All of the combinations of moves that end in a draw are then converted into games, meaning they are represented by “X”s and “O”s (2s and 1s respectively in the code) instead of the orders of moves (this is important because it greatly decreased the number of comparisons made, speeding up the code). All of those drawn games are then combined in every possible way, and are checked for the other two methods of winning. Every game ends in a win.
