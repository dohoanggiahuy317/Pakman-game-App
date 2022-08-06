# App_PakPak_Game_Java

## 1. Product Description
Our Pak-man is a game in which the player guides a “hungry yellow character” through a maze. The goal of the game is to devour all of the dots in the maze while escaping four different colored ghosts chasing him: Blinky (red), Pinky (pink), Inky (cyan), and Clyde (orange).<br>
The player progresses to the next level when Pak-Man consumes all of the dots. Pak- Man will lose a life if he comes into touch with a ghost; the game will terminate after all lives have been lost.<br>

There are 4 large flashing "energizers" placed in the maze's four corners. When Pak-man eats one of these, the ghosts will become blue with a dizzy face and the player can “defeat” the ghost. After a certain amount of time, the ghost will recover and re-chase Pak-man.<br>

In our game, we introduce a new feature, which is not available in the original game, that players can choose levels before starting the game. There are 3 levels: easy, medium, and hard.<br>
After the player dies, he can type their name and check his rank on the leaderboard.<br>

Our team decided to design the game following the old-school style. The player can only control and navigate to different buttons on the keyboard, not with the mouse. Moreover, the font style, 8-bit sound effect and background music will bring the player to the vibe of the 80s.

## 2. Product Functionality.
Our game is based on Java SWING, and all game states are handled by a single JFrame.<br>

There are six different maps, each saved as a .txt file. In the folder "resources," we also prepare the sound and visuals of the ghosts, map elements, Pak-man, audio files, and the leaderboard (.txt) file. To create a game with the vibe of the 80s, we decided that there is no “winning” score. The player will continue to play until he dies, which means he will return to the initial map after completing 6 maps.<br>
We create ghost algorithms in the "Entities" subdirectory. We create an algorithm for one ghost, "Blinky," and then expand the "Blinky" class and override several functions to give each ghost different characteristics.<br>

The "Tiles" folder contains classes that convert the map's.txt files with graphics into forms that the user can play.<br>
"Sound" and "SoundManager" are the two classes in the "Sound" folder. They invoke the audio in the "resources" folder and play sound at various game events.<br>

We implemented the interface "KeyListener" and extended the class "KeyEvent" to allow the player to use the keyboard to select the game mode, examine the scoreboard, and control Pak-man in the game. Pak-man is controlled by the direction keys or the keys A, W, S, and D. To check the player's action, we override two functions: "KeyPressed" and "KeyReleased."<br>
It continuously invokes the "update" function for the main game (Game Panel) to check the status of the map and the position of characters during the game. The game will switch to another map after Pak-man has completed one. This class controls the game's flow, sounds, tiles, and positions of the player or ghosts after each level.<br>

The "Leaderboard" class reads the data from the file "leaderboard.txt" and compares the scores using the Interface "Comparable" and Class “PriorityQueue.” The class compares the class “PlayerInfo” (containing name and score) by the score of each player. It will print out 10 of the highest points.<br>

The main algorithm in the game is the "Algorithms" class. When the player dies or completes a map, the Pak-man collides with the ghosts, or eats the power-up dots, the class will examine and direct the game flow with different behavior according to the game’s description. The class also manages the distance between the ghosts and Pak- man<br>
Finally, the class “UI” is used to “draw” everything into the frame. The class invokes different functions to draw items depending on the game condition. It also conjures up graphics of the map, ghosts, Pak-man, buttons, labels, and screen scores to print out.

## 3. Architecture
Pak-man is created with Java and its applications (Set, SWING, KeyEvent,
KeyListener, Collections, ArrayLists, Comparable, PriorityQueue) for many uses that
I discussed in the Production Functionality section. <br>

We also organize and tidy up each class's directory. We group images, audio, fonts,
styles, and maps in the resources folder. We divide the game classes into
subdirectories based on their functions (Core, Entities, Sound, and Tiles). <br>

We also classify functions and classes based on their function in the Core folder (UI,
Algorithms, GamePanel, KeyControl, Leaderboard, and Main) 5. Design (GUI design-main screenshots, UML-activity diagram).

## 4. Product Design
<p >
<img width="200" alt="Screen Shot 2022-08-06 at 11 16 39 AM" src="https://user-images.githubusercontent.com/72744045/183233336-f9fb381c-5707-4b36-ac91-d6645bd512b9.png">
<img width="200" alt="Screen Shot 2022-08-06 at 11 16 48 AM" src="https://user-images.githubusercontent.com/72744045/183233294-6b02bf35-fb96-48ae-8ad5-8dc1bbaac92e.png">
<img width="200" alt="Screen Shot 2022-08-06 at 11 17 18 AM" src="https://user-images.githubusercontent.com/72744045/183233301-ab148a3f-267a-4a2e-b41f-74c6f5131b50.png">
<img width="200" alt="Screen Shot 2022-08-06 at 11 17 24 AM" src="https://user-images.githubusercontent.com/72744045/183233303-c602c772-7475-4912-b4c9-35832b429e7f.png">
</p> 

<p>
<img width="200" alt="Screen Shot 2022-08-06 at 11 17 01 AM" src="https://user-images.githubusercontent.com/72744045/183233297-cf1c556a-5e82-4646-823c-d8f49bdb2cc0.png">
<img width="200" alt="Screen Shot 2022-08-06 at 11 17 08 AM" src="https://user-images.githubusercontent.com/72744045/183233300-3e178ad9-4f94-4696-b976-743d8d5ec2c4.png">
<img width="200" alt="Screen Shot 2022-08-06 at 11 17 33 AM" src="https://user-images.githubusercontent.com/72744045/183233304-196a2986-0513-4762-9389-2b7898fb9909.png">
<p/>
