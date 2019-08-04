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

## Possible Future Imporvements:
* Use selenium to get game data for the AI
* Implement reinforcement learning rather than tree search
  * Q-Table and/or Q-Network
* Would be interesting to see if a Conv. NN could solve this problem visually without manually extracting number data
