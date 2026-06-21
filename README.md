# CS330
CS330 Repository


# CS-330 Computational Graphics and Visualization Final Project

# Project Reflection

## How do I approach designing software?

I approach software design by first identifying the project requirements and then breaking the overall problem into smaller, manageable components. For this project, I began by determining the objects, textures, lighting, and navigation features that would be needed to satisfy the assignment requirements. Once the major components were identified, I planned how each object would be constructed and how the user would interact with the scene. This approach allowed me to focus on individual features while maintaining a clear vision of the final product.

### What new design skills has your work on the project helped you to craft?

Working on this project strengthened my ability to design 3D environments and visualize how multiple components work together within a scene. I gained experience with spatial reasoning, object placement, texture selection, and lighting design. I also learned how to create reusable systems that make scene management more efficient, such as transformation and texture management functions.

### What design process did you follow for your project work?

My design process followed an iterative approach. I first created a basic scene using simple geometric shapes and then gradually added more complex features such as textures, lighting, and camera controls. After each milestone, I evaluated the results, identified areas for improvement, and refined the scene accordingly. This process allowed me to build the project incrementally while ensuring that each component functioned correctly before moving on to the next stage.

### How could tactics from your design approach be applied in future work?

The modular and iterative design techniques used in this project can be applied to future software development projects. Breaking complex systems into smaller components improves organization and simplifies troubleshooting. Incremental development also allows features to be tested individually, reducing errors and improving overall software quality.

---

## How do I approach developing programs?

When developing programs, I begin by understanding the requirements and planning the functionality needed to meet those requirements. I then implement features in small sections, testing frequently to ensure correctness before moving forward. This helps prevent large-scale issues and makes debugging more manageable.

### What new development strategies did you use while working on your 3D scene?

One of the most valuable strategies I used was creating reusable functions for common operations such as object transformations, texture assignments, and shader configuration. Rather than repeating code for each object, I developed modular functions that could be reused throughout the project. I also became more comfortable using debugging techniques to identify rendering issues, texture-loading problems, and lighting configuration errors.

### How did iteration factor into your development?

Iteration played a major role in the development process. The scene evolved significantly throughout the milestones as I refined object placement, adjusted textures, improved lighting, and optimized camera controls. Many features required multiple revisions before achieving the desired visual result. Each iteration provided feedback that helped improve both the appearance and functionality of the scene.

### How has your approach to developing code evolved throughout the milestones, which led you to the project’s completion?

Throughout the course, my development process became more structured and efficient. Early milestones focused primarily on making objects appear correctly within the scene. As the project progressed, I began emphasizing code organization, modularity, and reusability. By the final milestone, I was able to implement more advanced features such as multiple light sources, texture mapping, and interactive navigation while maintaining a cleaner and more maintainable codebase.

---

## How can computer science help me in reaching my goals?

Computer science provides the technical foundation necessary to solve complex problems and create innovative solutions. The skills developed through programming, software engineering, and computational thinking are directly applicable to my long-term career goals in technology. By learning how to design, develop, and maintain software systems, I am building the knowledge required to succeed in professional software development and related technology fields.

### How do computational graphics and visualizations give you new knowledge and skills that can be applied in your future educational pathway?

Computational graphics and visualization have expanded my understanding of mathematics, algorithms, and software design. Concepts such as transformations, vectors, matrices, shaders, and rendering pipelines provide a deeper understanding of how modern graphical systems operate. These skills will support future coursework involving game development, simulation, artificial intelligence, virtual reality, and advanced software engineering topics.

### How do computational graphics and visualizations give you new knowledge and skills that can be applied in your future professional pathway?

The knowledge gained from computational graphics and visualization can be applied to many professional fields including software engineering, game development, simulation systems, data visualization, cybersecurity training environments, and virtual reality applications. Through this project, I developed experience with OpenGL, debugging complex software systems, modular programming, and interactive user interfaces. These technical skills strengthen my ability to develop high-quality software solutions and will be valuable throughout my professional career as a computer science practitioner.




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
