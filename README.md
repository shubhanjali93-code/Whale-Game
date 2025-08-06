# Whale-Blaster


Whale Blaster is built on a modular, state-driven architecture using HTML5 Canvas and vanilla JavaScript. The game loop is powered by requestAnimationFrame, ensuring smooth rendering and consistent frame updates.

🧩 Objective
- Survive as long as possible while shooting down enemies.
- Collect Lucky Fish to gain extra ammo and activate dual-shot mode.
- Avoid collisions with hostile creatures like Angler Fish and Hive Whales.
- Watch out for swarms of Drones—they’re fast and unpredictable!

Core Concepts:
- Game Loop & Delta Time
  - The loop calculates deltaTime to normalize movement and animation speed across devices.
  - All entities (player, enemies, particles) update and draw within this loop.
- State-Driven Entities
  - Each enemy and player object maintains its own state (sitting, running, jumping, dying, etc.).
  - Transitions are triggered by collisions, timers, or user input.
- Sprite Sheet Animation
  - Characters and effects use sprite sheets.
  - Frames are cropped and scaled dynamically to animate movement, explosions, and interactions.
- Collision Detection
  - Bounding box logic is used for player-enemy and projectile-enemy collisions.
  - Hitboxes are visualized in debug mode for precise tuning.
- Object Pooling
  - Projectiles and particles are reused to optimize performance and reduce memory churn.
- Parallax Scrolling
  - Multiple background layers scroll at different speeds to simulate depth.
  - Seamless looping is achieved by resetting layer positions once off-screen.
- Event-Driven Logic
  - Keyboard events control movement, shooting, and toggling debug mode.
  - Button click events allow instant game restart.
- Visual Polish
  - CSS filters (blur, contrast) and canvas layering enhance the aesthetic.
  - Particle systems add feedback for explosions and collisions.
