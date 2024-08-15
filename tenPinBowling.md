# Ten Pin Bowling 
## Introduction 
In the game of ten-pin bowling, a player rolls a bowling ball down a lane to knock over pins. There are ten pins set at the end of the bowling lane. Each player has 10 frames to roll a bowling ball down a lane and knock over as many pins as possible. The first nine frames are ended after two rolls, or when the player knocks down all ten pins. In the last frame the player will receive an extra roll every time they knock down all ten pins up to a maximum of three rolls. 

Your task is to create an algorithm that takes a string for a complete game of 10 frames (using standard bowling notation explained below) and returns the final score for the game. 

## Scoring 
For the first 9 frames you get 2 rolls to knock down as many of the original 10 pins as possible. You receive a point for every pin knocked down. The first 3 frames of a game might be represented like this: 

54 72 44 

In the first frame they scored 9 points (the first ball knocked down 5 pins and the second ball knocked down 4 pins). In the second frame they scored 9 points again (7 + 2). In the third frame they scored 8 points (4 + 4). After the first three frames they had scored a total of 26 (9 + 9 + 8) points. 

It gets more complicated when strikes and spares are introduced. 

A strike occurs when all 10 pins are knocked down with the first ball of the frame and is represented on the score sheet with an X. In the first 9 frames of a game this concludes the frame, and it will be scored as 10 points plus the points received from the next two rolls. If a player had 2 frames 

X 54 

The total score for those two frames would be 28. The first frame is worth 19 (10 + 5 + 4) and the second frame is worth 9 (5 + 4). 

A spare occurs when all 10 pins are knocked down within a frame and is represented by a / on the scorecard. In the first 9 frames of a game this will be scored as 10 points plus the points received on the next roll. If a player had 2 frames 

5/ 72

The total score for the two frames would be 26. The first frame is worth 17 (10 + 7) and the second frame is worth 9 (7 + 2). 

Input 
Input will be a text string representing a complete game for a single player. Each frame will have a space between them. Each of the first 9 frames can be formed of 1 or 2 characters. The last frame can be made from 2 or 3 characters. 

Output 
The output of the algorithm should be a number representing the final score.

| Test Input                          | Expected Output |
|-------------------------------------|-----------------|
| 34 81 90 09 45 21 70 44 30 52       | 71              |
| 53 71 8/ 20 7/ 04 90 X  33 27       | 84              |
| 00 00 00 00 00 00 00 00 00 5/X      | 20              |
| 00 00 00 00 00 00 00 00 00 X4/      | 20              |
| 00 00 00 00 00 00 00 00 00 X42      | 16              |
| XX XX XX XX XX XX XX XX XX XXX      | 300             |


