# Pizzeria Spelling Game

Pizzeria Spelling Game is a fun and educational game designed to test spelling skills and improve typing proficiency. It is particularly suitable for kids or individuals who want to learn English. The game challenges players to spell ingredients correctly within a time limit to earn points. As the game progresses, the difficulty increases, adding more words to spell and reducing the round duration.

## Game Overview

The core mechanics of the game are handled by several functions:

- `retrieve_words()`: Retrieves words (ingredients) from a .txt file, allowing for easy updates and additions.
- `get_random_word()`: Returns a random word from the available list.
- `compare_words()`: Compares two words and returns the number of missing/unmatched letters, considering shorter words as completed with "*".

The game logic and display are handled by the rest of the code, which includes:

- Difficulty selection GUI: Players can choose the desired difficulty level using customized buttons arranged in a grid layout.
- `new_round()`: Implements most of the game logic, including the countdown for each round. The score and timer are updated accordingly.
- Music integration: Background music is implemented using the `pygame` library, allowing for easy switching between music files.
- Button functionality: Each button is associated with specific functionality to enable a smooth gaming experience.

## Libraries Used

The game utilizes the following libraries:

- **tkinter**: Used for creating the graphical user interface (GUI), including buttons, labels, and text entry fields. It enables user interaction and event handling.
- **pygame**: Employed for playing background music and sound effects during the game, enhancing the overall gaming experience.
- **random**: Utilized for generating random ingredients for the spelling game.
- **time**: Imported for using the `sleep()` function to introduce delays and implement timers.
- **PIL (Python Imaging Library)**: Used for working with images, such as loading and displaying background and visual elements in the game.
- **os**: Employed for interacting with the operating system, particularly for accessing and playing audio files and managing file paths.
- **messagebox**: A module of tkinter that provides functions for displaying dialog boxes or message boxes to communicate information or messages to the player.

## Getting Started

To run the Pizzeria Spelling Game, follow these steps:

1. Ensure you have Python installed on your system.
2. Clone this repository to your local machine.
3. Install the required dependencies by running `pip install -r requirements.txt`.
4. Run the `pizzeria_spelling_game.py` file using Python.
5. Select the desired difficulty level from the GUI.
6. Enjoy playing the game and improve your spelling skills!

## Contributing

Contributions to the Pizzeria Spelling Game are welcome! If you have any ideas, suggestions, or bug fixes, please open an issue or submit a pull request. 

When contributing, please ensure that your code adheres to the existing coding style and follows best practices. Additionally, provide a detailed description of the changes you've made and the rationale behind them.

## License

The Pizzeria Spelling Game is licensed under the [MIT License](https://opensource.org/licenses/MIT). You are free to use, modify, and distribute the game for personal and commercial purposes. However, the game comes with no warranties or guarantees. Use it at your own risk.

## Acknowledgements

We would like to acknowledge the following resources and individuals that contributed to the development of the Pizzeria Spelling Game:

 language and its extensive library ecosystem.
- The creators and contributors of the tkinter, pygame, random, time, PIL, and os libraries for their excellent work.
- Our development team members who worked hard to bring this game to life.

## Conclusion

The Pizzeria Spelling Game offers an engaging and educational experience for players to improve their spelling and typing skills. With its user-friendly interface, dynamic difficulty adjustment, and entertaining gameplay, it provides an effective and enjoyable way to enhance language proficiency. Feel free to explore the code, make contributions, and customize the game to suit your needs. Enjoy playing and happy spelling!
