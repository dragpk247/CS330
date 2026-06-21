# CS330
CS330 Repository


# CS-330 Computational Graphics and Visualization Final Project

## Project Overview

This project was developed for **CS-330: Computational Graphics and Visualization** at Southern New Hampshire University. The objective of the project was to design and implement a fully interactive 3D scene using OpenGL while demonstrating fundamental computer graphics concepts including geometric modeling, transformations, texture mapping, lighting, shaders, and camera navigation.

The final scene contains multiple custom objects, textures, and lighting effects that work together to create a visually appealing environment. Users can freely explore the scene through an interactive first-person camera system.

---

## Features

### 3D Object Modeling

The scene contains multiple geometric objects created using OpenGL mesh primitives, including:

* Decorative white ring sculpture (torus)
* Melon sphere
* Melon slice
* Glass cylinder
* Candle flame
* Ground plane

Each object utilizes unique transformations including scaling, rotation, and translation.

### Texture Mapping

Multiple textures were applied throughout the scene to improve realism and visual quality.

Textures include:

* Clay texture
* Melon exterior texture
* Melon interior texture
* Glass texture
* Candle flame texture
* Ground surface texture

### Lighting System

The project implements a multi-light illumination system using:

* Ambient lighting
* Diffuse lighting
* Specular lighting

Lighting calculations are performed within the fragment shader to produce realistic shading and highlights across the scene.

### Interactive Camera Controls

Users can freely navigate the 3D environment using keyboard and mouse input.

| Control            | Action              |
| ------------------ | ------------------- |
| W                  | Move Forward        |
| S                  | Move Backward       |
| A                  | Move Left           |
| D                  | Move Right          |
| Q                  | Move Up             |
| E                  | Move Down           |
| Mouse Movement     | Look Around         |
| Mouse Scroll Wheel | Adjust Camera Speed |

---

## Technologies Used

### Programming Language

* C++

### Graphics Libraries

* OpenGL 4.4+
* GLFW
* GLAD
* GLM

### Additional Libraries

* stb_image.h (Texture Loading)

### Development Environment

* Visual Studio 2022

---

## Project Structure

```text
Project Root
│
├── SceneManager.cpp
├── SceneManager.h
├── ViewManager.cpp
├── ViewManager.h
├── ShaderManager.cpp
├── ShaderManager.h
├── ShapeMeshes.cpp
├── ShapeMeshes.h
├── camera.cpp
├── camera.h
│
├── textures/
│   ├── clay.jpg
│   ├── melon.jpg
│   ├── cantalopeinside.jpg
│   ├── Fire.jpg
│   └── ground.jpg
│
└── shaders/
    ├── vertexShader.glsl
    └── fragmentShader.glsl
```

---

## Custom Functions

### SetTransformations()

Applies object scaling, rotation, and translation before rendering.

Purpose:

* Reusable transformation setup
* Reduces duplicate code
* Simplifies object placement

### CreateGLTexture()

Loads texture images into OpenGL texture memory.

Purpose:

* Centralized texture loading
* Reusable for all scene textures

### SetShaderTexture()

Assigns textures to objects during rendering.

Purpose:

* Simplifies texture management
* Improves code readability

### SetShaderColor()

Sets object colors when textures are not used.

Purpose:

* Provides flexible object appearance
* Useful for debugging and material creation

### SetTextureUVScale()

Controls texture repetition and scaling.

Purpose:

* Adjusts texture appearance on different objects
* Prevents stretching and distortion

---

## Graphics Concepts Demonstrated

### Transformations

* Translation
* Rotation
* Scaling

### Camera Systems

* First-person camera
* Mouse-controlled view direction
* Dynamic movement speed

### Texture Mapping

* UV coordinates
* Multiple texture assignments
* Texture scaling

### Lighting and Shading

* Ambient lighting
* Diffuse reflection
* Specular highlights
* Material properties

### Shader Programming

* Vertex shader processing
* Fragment shader lighting calculations
* Uniform variable management

---

## Learning Outcomes

This project demonstrates the following computational graphics concepts:

* Creating and rendering 3D objects
* Applying transformations using matrices
* Implementing texture mapping
* Developing lighting models
* Building reusable graphics functions
* Managing shaders and materials
* Creating an interactive camera system
* Organizing graphics code using modular design principles

---

## Author

Jordan Isaac

Southern New Hampshire University

CS-330 Computational Graphics and Visualization

2026

This project was completed as part of the coursework for CS-330 at Southern New Hampshire University. The project utilizes OpenGL, GLFW, GLM, and stb_image libraries to support graphics rendering, camera movement, texture loading, and scene management.
