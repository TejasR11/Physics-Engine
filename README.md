# Game Design Document

## Section 0: Summary

Mario Battle Royale:
Team members - Eric He, Tejas Ram (roles to be decided)
Mario Battle Royale is a two player game in which characters fight against each other on a floating stadium, where the last man standing wins.

## Section 1: Gameplay
This section should address simple questions about how your game works:

The game starts out with two players on each side of the stadium. Players begin with full health and their default starter guns. Throughout the game, there will be floating "special blocks" that will grant different power ups. Players will be able to move around, jump, collect these power ups, and fire/fight each other. Movement will be controlled by the arrow keys and the "WASD" keys, while attacking will be controlled by the "shift" and "Tab" keys. Players will begin with 100 hp, and will lose health based on the quality of attack of the opponent (dependent on power ups). There will also be certain powerups that allow for characters to gain health. The winner will be determined by the player to first make the other player lose all their health. There are no levels in this game, since it is a 1v1 battle royale format. The game incorporates the physics engine through its jumping, and movement. Players will be subject to gravity, and certain powerups will use different types of physics. For example, one type of power up can be an attack/shot that is subject to gravity, while another can travel in a straight line at constant velocity. In addition we would need to implement collision detection to determine when players get hit, run into a wall, or obtain a power up. We will use sprites to create our characters and power up graphics, which we will take from online (Mario), but we will use polygons to create different bullets for different power ups. 


## Section 2: Feature Set

Priority 1:
- Create and renders the graphics and environment. Add bodies for obstacles, players, power ups, and projectiles. This will essentially be implementing the start state of the game where two players are initialized at different side of a platform they are standing on with obstacles in between. It will also define types of bodies such as bullets and power-ups so they can be accessed later on. 
- Implement key board handling for movement (jumping) and attacks using the bodies. Left and Right movement will go back and forth at constant velocity (possible acceleration feature will have to test if gameplay is still consistent). Jumping will just be going up at initial velocity then gravity taking effect. Projectile attacks will appear out of their "weapon" and move at constant velocity in direction they face.

Priority 2:
- Implement projectile handling for decrementing player health, physics of the different bullets. Branching from methods in collision handling, it would have players lose health and different types of gravity/trajectories for projectiles.
- Implement collision handling for bullets (if hit) and the characters (ex. check if on ground to prevent being able to jump in the air)

Priority 3:
- Have power-ups randomly appear throughout the screen (in reachable positions) at random time intervals with no more than two power-ups at one time; implement how player would use power-up + timer for power-ups to end. 
- Implement features of different power-ups (ex. more health/buffed speed etc.). This would define different types of power-ups with their specific features applying to the character the power-up is collected by.

Priority 4:
- Implement sprite switching for the power-ups and changing direction (ex. character will switch skin when collecting power-ups)
- Implement special animations (for example when a player collects a mini mushroom their size oscillates for a 1 second, like collecting a mushroom in mario. Also include win animations)

## Section 3: Timeline
Week 1 - Tejas will render the graphics and images, and Eric will implement the keyboard handling (both priority 1 tasks should be complete).

Week 2 - Tejas will complete the collision handling for the bullets and players, while Eric will handle the player health and physics of the different bullets. Tejas will also implement the features of the different power ups, while Eric will handle generating the power ups randomly throughout the screen.

Week 3 - Tejas will implement the special animations, while Eric will implement the sprite switching.
## Section 4: Disaster Recovery

If Tejas falls behind, Eric will allocate time to implement the priority 3 feature (different power-ups) that Tejas was supposed to do. This should help Tejas get back on track 

If Eric falls behind, Tejas will allocate time to implement the other priority 3 feature (generating the power-ups randomly) that Eric was supposed to implement. 

If Tejas or Eric falls behind on a priority 1 task, it is crucial for the other player to step in and help them complete this task immediately before moving onto priority 2 task. Essentially, each priority tasks must be completed before moving onto the next one, as they build off each other. So both teammates have to as a group figure out how to get both features in a priority tier working before moving onto the next priority tier.
