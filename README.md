# Physics Engine & Game

A 2D physics engine with rigid-body dynamics, convex-polygon collision detection, vector mathematics, scene/state management and a Mario vs Bowser fighting game built on top of it.

## Features

- Real-time physics simulation with gravity and collisions
- 2D rigid body dynamics  
- Vector math library
- SDL2 graphics and audio
- Mario vs Bowser fighting game demo

## Building

Requires SDL2 development libraries:

```bash
make game
```

This builds a web version using Emscripten. Access at `http://localhost:8000/bin/game.html`

## Game Controls

- **Arrow Keys**: Move characters
- **Space**: Jump  
- **Enter**: Fire projectiles
- **R**: Restart game

## Game Features

- Two-player Mario vs Bowser combat
- Power-ups (speed boost, health, invincibility, bombs)
- Goomba enemies that spawn periodically
- Mystery boxes with random power-ups
- Health system with visual indicators

## Physics Engine

Core components in `include/`:
- `vector.h` - 2D vector operations
- `body.h` - Rigid body physics
- `forces.h` - Force applications (gravity, springs, etc.)
- `collision.h` - Collision detection and response
- `scene.h` - Physics world management

The engine supports gravity, elastic collisions, and various force applications for realistic 2D physics simulation.
