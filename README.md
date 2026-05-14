# Space-Management

For our game for Assigment 2 we had to make a game following this requisites:

1. Must be open world.
2. Cant be limited to the window's size.
3. Must have animations, sound and collisions.
4. The player must be able to perform other actions other than moving.
5. There must be enemies with autonomous movement.

So we decided to make a top down game in space. The player would control a spaceship with WASD that would always look towards the cursor. The world would be a solar system similar to ours with 6 planets with color names so that it would be easier to spot them (RED, YELLOW, BLUE, PINK, WHITE, GREEN).

<img width="1279" height="717" alt="Screenshot1" src="https://github.com/user-attachments/assets/7a0592aa-31a7-4433-9c63-de3de4692eb6" />

For the goal of the game the player would have to deliver packages from one planet to another avoiding enemies, trying to fill a quota. We also needed to make a camera that would follow the player.
We also needed to make a minimap so that the player would know where the planets where and where to go.

Camera: since the world is about 6000x6000 px you can't see everything in the window, so we had to do a camera that would follow the player. After drawing the player we created the camera script which uses a Matrix. What this does is moving everything drawn in the world in the oposite direction of the player direction, so if the player has a planet above and it moves up towards it the planet will move down, making it look like the player is moving.

Player actions: the player has WASD movement, but can also shoot laser by clicking the left mouse button, then the projectile will be created and shot in the direction the ship is looking, if it hits a planet it will be destroyed, and if it hits an enemy it will kill it. The player also has a turbo when holding right click.

Minimap: to make the minimap we first had to separate the way the game was drawn, creating two separate parts in the Draw function, one will be affected by the camera Matrix, and the other one would be the UI which wouldn't be affected by the Matrix, so it would be static on screen. We put the minimap on the bottom left corner of the screen, and we had to translate the coordinates of everything on the map to the minimap. We also added an indicator to tell you where you had to go either to pickup a package or to deliver it.

Enemies: for the enemies we made a simple AI that would follow the player if it's in range, it would also die if it hits a planet or the sun and give you some money.

<img width="1278" height="715" alt="Screenshot2" src="https://github.com/user-attachments/assets/adc0f9bb-7154-4c80-8847-6961eab543e2" />

Game made by Nel Allende Iglesias and Jorge Sáez Saldaña
