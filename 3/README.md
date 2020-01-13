# Problem: Fifteen

## tl;dr

Implement the Game of Fifteen, per the below.

```
$ ./fifteen 3
WELCOME TO GAME OF FIFTEEN

8  7  6

5  4  3

2  1  _

Tile to move:
```

{% next "Let's Begin" %}

# Getting Ready

Have a more in-depth look at debugging techniques from Doug. (Odds are these 30 minutes with Doug will save you hours over the course of the term!)

<a href="http://www.youtube.com/watch?feature=player_embedded&v=VtkMZjvvKaU
" target="_blank"><img src="http://img.youtube.com/vi/VtkMZjvvKaU/0.jpg" 
alt="CS50 Debugging" width="240" height="180" border="10" /></a>

{% next "Ready to Move On %}

# Background

The Game of Fifteen is a puzzle played on a square, two-dimensional board with numbered tiles that slide. The goal of this puzzle is to arrange the board's tiles from smallest to largest, left to right, top to bottom, with an empty space in board's bottom-right corner, as in the below.

Sliding any tile that borders the board's empty space in that space constitutes a "move."  Although the configuration above depicts a game already won, notice how the tile numbered 12 or the tile numbered 15 could be slid into the empty space. Tiles may not be moved diagonally, though, or forcibly removed from the board.

Although other configurations are possible, we shall assume that this game begins with the board's tiles in reverse order, from largest to smallest, left to right, top to bottom, with an empty space in the board's bottom-right corner. *If, however, and only if the board contains an odd number of tiles (i.e., the height and width of the board are even), the positions of tiles numbered 1 and 2 must be swapped, as in the below.* The puzzle is solvable from this configuration.

{% next "Ready to Move On %}

## Understanding

Take a look at `fifteen.c`. Within this file is an entire framework for the Game of Fifteen. The challenge up next is to complete this game's implementation.

But first go ahead and compile the framework. (Can you figure out how?) And, even though it's not yet finished, go ahead and run the game. (Can you figure out how?) Odds are you'll want to run it in a larger terminal window than usual, which you can open clicking the green plus (+) next to one of your code tabs and clicking *New Terminal*. Alternatively, you can full-screen the terminal window toward the bottom of CS50 IDE's UI (within the UI's "console") by clicking the *Maximize* icon in the console's top-right corner.

Anyhow, it appears that the game is at least partly functional. Granted, it's not much of a game yet. But that's where you come in!

{% next "Ready to Move On %}

## Checking for Understanding

Read over the code and comments in `fifteen.c` and then answer the questions in `questions.md`, which is a (nearly empty) text file that we included for you inside of the distribution's `fifteen` directory.

No worries if you're not quite sure how `fprintf` or `fflush` work; we're simply using those to automate some testing.

{% next "Let's Move On" %}

# TODO

Implement the Game of Fifteen, per the comments in `fifteen.c`.

- Implement `init`.
- Implement `draw`.
- Implement `move`.
- Implement `won`.

## Walkthrough

<a href="http://www.youtube.com/watch?feature=player_embedded&v=Rx_FJb3vr9U" target="_blank"><img src="http://img.youtube.com/vi/Rx_FJb3vr9U/0.jpg" alt="Fifteen Walkthrough" width="240" height="180" border="10" /></a>

## Hints

- Remember to take "baby steps." Don't try to bite off the entire game at once.
- Implement one function at a time and be sure that it works before forging ahead. Remember to treat each function as a distinct piece of the program (e.g., the `init` function should not print anything; the `draw` function should not modify the board; etc.).
- Any design decisions not explicitly prescribed herein (e.g., how much space you should leave between numbers when printing the board) are intentionally left to you. Presumably the board, when printed, should look something like the below, but we leave it to you to implement your own vision.

```
15 14 13 12

11 10  9  8

 7  6  5  4

 3  1  2  _
```

Incidentally, recall that the positions of tiles numbered 1 and 2 should only start off swapped (as they are in the 4 × 4 example above) if the board has an odd number of tiles (as does the 4 × 4 example above). If the board has an even number of tiles, those positions should not start off swapped. And so they do not in the 3 × 3 example below:

```
8  7  6

5  4  3

2  1  _
```

Do not alter the flow of logic in `main` itself so that we can automate some tests of your program once submitted. In particular, `main` must only return `0` if and when the user has actually won the game; non-zero values should be returned in any cases of error, as implied by our distribution code.

{% next "Ready to Test" %}

# Testing

## Correctness

Note that `check50` assumes that you're indexing into `board` a la `board[row][column]`, not `board[column][row]`.

`check50 cs50/problems/2019/ap/fifteen`

## Style

`style50 fifteen.c`

## Staff Solution

If you'd like to play with the staff's own implementation of `fifteen`, you may execute the below.

`~cs50/2019/ap/chapter3/fifteen`

{% next "Ready to Submit" %}

# How to Submit

1. Ensure you have all of the files below:
   - fifteen.c
   - questions.md

1. To submit `fifteen`, execute `submit50 cs50/problems/2019/ap/fifteen` inputting your GitHub username and GitHub password as prompted.

   You may resubmit any problem as many times as you'd like.

   Your submission should be graded for correctness within 2 minutes, at which point your score will appear at https://submit.cs50.io/[submit.cs50.io]!
