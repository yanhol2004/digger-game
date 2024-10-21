# Introduction
This project is an interactive 2D game implemented in Python and [Processing](https://processing.org), inspired by the classic arcade game, [Digger](https://en.wikipedia.org/wiki/Digger_(video_game)). In this game, players explore a dynamically generated underground maze, collecting emeralds and gold while evading and eliminating enemies. The gameplay is designed to challenge both quick reflexes and strategic thinking, appealing to casual and dedicated gamers alike. The game was developed as a final project for the "Intro to CS" class.

<img width="908" alt="image" src="https://github.com/user-attachments/assets/dde55747-7f16-4d26-a8f2-ba7f21eb16ec">    

<br> **Checkout the [video](https://youtube.com/shorts/g7NrTtpwd7U?feature=share) of the gameplay!**

# Key Features

### 1. Scalable Levels & Customization

The game supports a scalable number of levels, providing flexibility for users or developers to create new levels simply by configuring text files. Each text file dictates the layout, enemy behavior, and difficulty, offering endless customization. This design makes the game highly extendable and allows easy addition of new challenges and maps without altering the codebase.

### 2. AI-driven Enemy Behavior

One of the key highlights is the intelligent enemy movement system. Enemies, or “nobbins” and “hobbins,” pursue the player using a Breadth-First Search (BFS) algorithm. This ensures that enemies follow the most direct path to catch the player. Additional parameters have been introduced to modify enemy behavior, such as:

* Randomized Decision-Making: Adding a probability for enemies to make “wrong” moves, which introduces unpredictability in gameplay.
*	Variable Speed: By tuning parameters in the level configuration file, each enemy can behave differently, adding variety to their movements and making higher levels more challenging.

### 3. Dynamic Gameplay Mechanics

*	Gold Bag Physics: Players can dig through the ground and drop gold bags onto enemies. Bags, once dropped, follow gravity-based mechanics—falling through empty vertical tunnels and breaking open to release gold when they land. This mechanic adds layers of strategy: players must avoid being squashed while trying to trap enemies with falling bags.

* Physics Calculations: To calculate the movement of the bag, physics formulas are used. When the digger hits the side of the bag, its initial velocity is calculated by the law of momentum conservation, allowing the system to account for whether the bag was already in motion. The bag’s subsequent positions are determined by applying deceleration, gradually reducing its speed. Similarly, when the bag falls vertically, its speed increases according to gravity, providing realistic movement behavior as it accelerates during the fall.

### 4. In-Game Progression and Saving

*	Score Tracking & User Saving: A built-in scoreboard tracks user progress across sessions, stored in a CSV file. This not only saves high scores but also offers potential multiplayer functionality.
*	Multiple Levels & Difficulty Scaling: As players progress through the game, levels become increasingly complex, with tougher enemies and reduced bonus mode times.

### 5. Polished Visuals and Sound

The game is designed with engaging visual aesthetics, including animations for digging, enemy movement, and gold bag interactions. Sound effects complement the game’s core actions, adding to the immersion. Additionally, the user interface includes a start menu, a scoreboard, and an option to pause the game.

# Development Details

### Technologies Used:

*	Python: The game logic and mechanics are implemented in Python.
* Processing: The Processing library was used to manage the graphical elements, including animations and player input handling.

### Game Architecture:

*	Game Class: Controls the main game loop, including handling player inputs, rendering the game environment, and managing state transitions (e.g., pausing, game over).
*	Creature Class: A base class for all entities in the game, including the player and enemies, with common attributes like movement, health, and animations.
* Digger & Enemy Classes: Derived from the Creature class, with specific mechanics such as digging (for the player) and enemy AI (for nobbins and hobbins). The hobbin enemies can also destroy emeralds and bags while digging.
* Loot Class: Manages the items that can be collected, such as emeralds and gold providing bonuses and score increases.

# Gameplay Breakdown:

The player starts each level in a pre-determined underground maze. The goal is to collect all the emeralds and eliminate all enemies while avoiding being killed. Enemies spawn periodically at the top-right corner and attempt to chase the player. The player can shoot enemies with a weapon that has a cooldown period, and by strategically digging under gold bags, players can squash enemies. As levels progress, enemies become smarter, and the game’s pace accelerates, testing the player’s strategic thinking and reflexes.

# Installation Instructions:

1.	Clone the repository: git clone https://github.com/yanhol2004/digger-game/
2.	Install dependencies: Ensure Python and Processing are installed on your machine. For Processing, follow instructions at Processing.org.
3.	Run the game: Execute the Python script to start the game: python game.py

# Potential for Further Development

* Multiplayer Mode: Introducing a competitive or cooperative mode for multiple players to engage simultaneously.
*	Power-ups & New Obstacles: Adding different kinds of bonuses or hindrances in later levels (e.g., teleporters, traps).
