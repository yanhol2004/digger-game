# Project Summary
This game was implemented using python, and [Processing](https://processing.org). This game is inspired by the original game [Digger](https://en.wikipedia.org/wiki/Digger_(video_game))

# Key highlights
The interesting parts of implementation are the following:
- The game has scalable number of levels. To create a new level one just needs to create a new text file describing all the configurations (i.e. gems locations, difficulty level, etc.)
- The enemies that chase the user down using BFS algorithm. Some parameters were added to slow down the enemies, give them some probability to make a wrong choice, and randomizing variable, so that different enemies follow different path. Through the text file one can tweak these parameters creating varying difficulties.
- Game mechanics, so that user can drop money bags and loot money from them. Enemy dies if money bag falls onto them
