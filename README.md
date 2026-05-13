# Space-Management

For our game for Assigment 2 we had to make a game following this requisites:

1. Must be open world.
2. Cant be limited to the window's size.
3. Must have animations, sound and collisions.
4. The player must be able to perform other actions other than moving.
5. There must be enemies with autonomous movement.

So we decided to make a top down game in space. The player would control a spaceship with WASD that would always look towards the cursor. The world would be a solar system similar to ours with 6 planets with color names so that it would be easier to spot them (RED, YELLOW, BLUE, PINK, WHITE, GREEN).

For the goal of the game the player would have to deliver packages from one planet to another avoiding enemies, trying to fill a quota. We also needed to make a camera that would follow the player.
We also needed to make a minimap so that the player would know where the planets where and where to go.

Camera: since the world is about 6000x6000 px you can't see everything in the window, so we had to do a camera that would follow the player. After drawing the player we created the camera script which uses a Matrix. What this does is moving everything drawn in the world in the oposite direction of the player direction, so if the player has a planet above and it moves up towards it the planet will move down, making it look like the player is moving.

Player actions: the player has WASD movement, but also can shoot

Minimap: to make the minimap we first had to separate


Enemies:
