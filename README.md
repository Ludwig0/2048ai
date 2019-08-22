# 2018Hackathon
This is all the code from my project made for Clemson's 2018 CU Hackit, an AI for 2048.

## Initial Release:
The initial version of this project is very over engineered. The program works like this
* Open 2048game.com with Selenium
* Take Screen shot of page
* process image s.t only the game screen is in view
* send image to AWS to do text recognition
* use value of game board for a tree search algorithm to play the game

This initial version is very slow due to the bottle necks of image processing, and constantly making requests to AWS.
The tree search algorithm was also very hastily thrown together due to time crunch. Overall this version suffers from my lack of
knowledge at the time, and trying to use too many fancy unnecessary tools

## Current State:
The project currently has implemented an environment and DQN class, but is unsuccessful in beating the game at this point in time.
One reason could be the lack of training data. The agent plays very slowly to avoid querying variable values from the web page
at a time before they have been updated. This leads to a much smaller amount of training data compared to most RL situations.
One possible improvement could be to rework the model to be a RNN that takes the previous action as input to help better view
moves as a sequence rather than independent events.
