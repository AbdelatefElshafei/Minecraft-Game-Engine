# Voxel Engine
![0](https://github.com/user-attachments/assets/cbbe532d-fd0b-48d9-8696-e6f84e7b18d8)

This project is a simple voxel engine built using Python, ModernGL, and Pygame, designed to simulate a 3D world with basic chunk and terrain generation, along with player movement, camera control, and rendering.

## Requirements

- Python 3.x
- Pygame
- ModernGL
- Numba
- NumPy
- GLM

You can install the required dependencies using pip:

```bash
pip install pygame moderngl numba numpy glm
```

## Overview

The voxel engine uses OpenGL to render a 3D world made up of chunks. The player can move around and interact with the environment, including terrain generation and a simple shader system. The engine supports the following features:

- **Chunk-based World Generation**: The world is divided into chunks for efficient rendering and manipulation.
- **Player Movement and Interaction**: The player can move through the world, looking around and interacting with the environment.
- **Shaders**: A custom shader program is used for rendering the scene.
- **Textures**: Different textures are used to represent terrain blocks such as grass, stone, dirt, and more.
- **Camera**: A simple camera setup with adjustable FOV, pitch, and aspect ratio.

## Engine Components

### 1. **VoxelEngine**
The core of the engine that handles initialization, update, rendering, and event handling.

- **Initialization**: Initializes Pygame, OpenGL settings, and other components like textures, player, and shaders.
- **Update**: Updates the player's position, scene, and other dynamic elements.
- **Render**: Clears the screen and renders the current scene.
- **Handle Events**: Listens for user input and updates the player accordingly.
- **Main Loop**: The game runs in a loop, continuously handling events, updating the state, and rendering the world.

### 2. **Player**
Controls the player's movement and interactions within the world.

- Handles keyboard input for movement and mouse input for looking around.
- Updates the player’s position based on speed and sensitivity.

### 3. **ShaderProgram**
Responsible for managing and applying the shaders used for rendering the world. Shaders handle visual effects and the rendering of terrain blocks.

### 4. **Scene**
Manages the world scene, including terrain generation, chunk management, and rendering. It updates the world based on the player’s position.

### 5. **Textures**
Handles the textures used for various terrain blocks such as sand, grass, stone, etc. These textures are applied to the terrain during rendering.

## Configuration Settings

You can configure the following settings in the `settings.py` file to adjust the world generation, player, camera, and terrain parameters.

- **OpenGL Settings**: Controls OpenGL version and depth settings.
- **Resolution**: Specifies the window resolution.
- **World Settings**: Controls world size, chunk size, and the center of the world.
- **Player Settings**: Adjusts player movement speed, rotation speed, position, and mouse sensitivity.
- **Terrain Levels**: Defines the height levels for different terrain types (e.g., snow, stone, grass).
- **Tree Settings**: Controls tree generation probabilities and dimensions.
- **Water Settings**: Defines the water level and area.
- **Cloud Settings**: Adjusts cloud scale and height.

## Running the Engine

To run the engine, execute the `main.py` script:

```bash
python main.py
```

This will initialize the Pygame window, set up the OpenGL context, and start the main game loop.
