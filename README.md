# Coding-Pizzeria-Spelling-Game-in-Python

Introduction

Pizzeria Spelling Game is a fun and educational game to test spelling skills and improve typing proficiency, aim at kids, or people who want to learn English. The goal of the game is to get as many points as possible by spelling ingredients (words) correctly in a time limit. Each round has a certain length depending on the difficulty. Increasing the difficulty of the game shortens the duration of a round and increases the number of words that need to be typed. In turns, players can achieve a higher score due to the extra words.

Game Overview

•	The core mechanics of the game are handled by these functions:
1)	Retrieves words (ingredients from a .txt file) 
 
This presents a major advantage, as the list can be easily updated with new words.
2)	Returns a random word from all the words available. 
 
3)	Compares 2 words and returns the number of missing / unmatched letters. Shorter words will be automatically completed with “ * ” in order to be correctly compared. This means any extra letter will be considered a mistake. 


•	The rest of the code handles how the game works and how is displayed. 
1)	Defines each difficulty parameters. 
 
2)	GUI for Difficulty selection. Here we use grid Layout to arrange the buttons. The windows size is given by the background image size to have a clean look. By keeping each background image size, the same we achieve a coherent and consistent look. The buttons are customized to match with the overall GUI aesthetic.
coherent look.

3)	“new_round()” is where most of the game logic is coded

	Each round will start after 3 seconds. We make use of sleep() function to count 1 second of inactivity.
 
	 Difficulty Score and time adjustment
	Start_next_round() calls all the functions needed for one round.
•	Update score and Timer
 
 
	To have music we choose to use “pygame” library. 
By making a class Music Player we can switch between music files with ease. We don’t need to make a function for each file.

•	Adding functionality to each button 

The libraries we used and why we used them.

•	tkinter: tkinter is a Python library for creating graphical user interfaces (GUIs). It provides a set of tools and widgets to build interactive windows and handle user events. In the code, tkinter is used to create the game's GUI, including buttons, labels, and text entry fields. It allows the user to interact with the game by clicking buttons, entering text, and pressing keys. The event-driven nature of tkinter enables the program to respond to user actions by binding event handlers to specific events, such as button clicks or key presses. For example, the "Submit" button is associated with the submit_input() function, which is executed when the button is clicked or the Enter key is pressed.
•	pygame: pygame is a cross-platform library designed for game development. It provides functionality for graphics rendering, audio playback, and handling user input. In the code, pygame is primarily used for playing background music and sound effects during the game. The MusicPlayer class wraps the functionality of pygame.mixer.music to load and play audio files. By utilizing pygame.mixer.music.play(), the music can be played in an infinite loop. This allows the background music to continue playing throughout the game. Additionally, pygame is used to stop the music when needed, such as when a round is over or the game is finished.

Both tkinter and pygame follow an event-driven programming paradigm. They use event loops to continuously monitor for user input events, such as button clicks or key presses. When an event occurs, the associated event handler function is executed, allowing the program to respond accordingly. This event-driven concurrency model enables the game to provide an interactive and responsive user interface while simultaneously performing other tasks, such as updating the score, checking timer expiration, or transitioning between game screens.

Initially we used threads to achieve something similar but there were several downsides.

GUI frameworks, like tkinter, are not designed to be thread-safe. They typically expect GUI-related operations to be performed in the main thread. Using threads for GUI handling can lead to unpredictable behavior or even crashes in certain cases. In addition, pygame and tkinter already have “threads” in their implementation. So we decided to use them instead. 

•	random: This module provides functions for generating random numbers, choosing random elements from a sequence, and shuffling sequences randomly. In our code, it is used to generate random ingredients for the spelling game.
•	Time import sleep: The sleep function is used to introduce a delay or pause in the program's execution. It is used in combination time.time() to implement timers and wait for specific durations.
•	PIL import ImageTk, Image: The PIL (Python Imaging Library) module is used for working with images in various formats. It provides functions to open, manipulate, and display images. In our code, it is used to load and display images as background and visual elements in the game.
•	import os: The os module provides a way to interact with the operating system. It offers functions to manipulate files and directories, get environment variables, and perform other system-related operations. In our code, it is used for accessing and playing audio files and managing file paths.
•	messagebox: The messagebox module is a part of the tkinter library and provides functions to display dialog boxes or message boxes to the user. We use it to show information and display messages during the game (Score, Time is up, Round over, etc.)

Conclusion 

In conclusion, the "Pizzeria Spelling Game" is a small but engaging project designed to help young children improve their typing skills while having fun. The game presents the player with random recipe ingredients, and the player's task is to type them correctly as quickly as possible to earn points and progress to the next round.

Throughout the development cycle, several key components were implemented. The SpellingCheck function was created to compare the player's input with the generated word and calculate the number of incorrect characters. The ComputeScore function determined the score based on the number of mistakes and the length of the word. A timer was incorporated to add a time constraint.

The game features a colorful and user-friendly interface created using the tkinter library. Background music was added using the pygame library to enhance the gaming experience. Additionally, the PIL library was utilized to display images, and the messagebox module from tkinter was employed to provide feedback to the player through dialog boxes.

To maintain engagement and challenge, the game dynamically adjusted the difficulty as the player progressed. The length of the ingredient vectors increased, and the time allotted for each round decreased. The game concluded after three rounds or when the time is up. 

During the development cycle, a collaborative approach was adopted, dividing the tasks among the team members. The code was tested and to ensure smooth gameplay and address game breaking issues.

Overall, the " Pizzeria Spelling Game" offers an enjoyable and educational experience for young players, allowing them to enhance their typing skills in a fun and interactive way. The project demonstrated the effective use of various Python libraries and modules, such as random, time, tkinter, PIL, pygame, and os, with event-driven programming  approach to implement different game functionalities.
