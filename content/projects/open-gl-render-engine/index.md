+++
title = "OpenGL Render Engine"
description = "A basic render engine written in C++ and OpenGL"
[taxonomy]
tags = ["C++", "OpenGL", "Rendering", "Engine", "Solo Project"]
[extra]
index = 0
preview_image = "vlc_2025-09-29_21-05-31.png"
preview_video = "opdrachten_2025-06-06_10-32-13.mp4"
is_youtube = false
tags = ["C++", "OpenGL", "Rendering", "Engine", "Solo Project"]
yvid_id = ""
+++

# [Project Link](https://git.hku.nl/joelle.ubink/glslopdrachten)
 
I decided as part of a course on Graphics Programming to make a basic render engine. I relied on the usage of `std::shared_ptr` and `std::weak_ptr` to avoid issues with lifecycles.

I followed the basic tutorials from LearnOpenGL to render a cube while at the same time writing classes to organize the code. I then built on top of classes like the Texture and Shader class to make a Material class.

I made these classes have configurability to make it simpler for myself to add or tweak elements in the scene and to keep the code organized.


ASsimp was used to import 3D models, OpenGL 3.3 was used for rendering, glm for math functions, vectors, and matrices, and stbi for loading textures.

Overall, I found the experience to have provided me with a lot of context as to how rendering works.


{{gallery()}}