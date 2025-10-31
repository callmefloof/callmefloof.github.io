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

project_year = "April/May 2025"
project_type = "Solo project"
project_duration = "5 weeks"


col_start = 1
col_span = 3
row_start = 3
row_span = 2



+++




{% grid(columns=8,rows=12) %}

{% gridcell(col_start=1,col_span=4,row_start=1,row_span=4) %}

{{video(source="opdrachten_2025-06-06_10-32-13.mp4 " style="width:100%;")}}
{% end %}

{% toggle_paragraph(open="open" level=2, col_start="5", col_span="4", row_start="1", row_span="4") %}
Summary

<p>As part of a C++ programming project, I made a simple clone of Speed Racer in SFML. In prior years lead I had mainly specialized in C# until late 2024 when I decided to switch major from Game Design to Game Development. I had prior experience in C++, but hadn't completed a full project with it up until this point. There was a steep learning curve not relying on the notion of a garbage collector cleaning up after me. This project was a first stepping stone for me in developing games in C++.</p>

{% end %}

{% toggle_paragraph(level=2, col_start="1", col_span="8", row_start="5", row_span="4") %}
Details

<p>I decided as part of a course on Graphics Programming to make a basic render engine. I relied on the usage of <code class="language-cpp">std::shared_ptr</code> and <code class="language-cpp">std::weak_ptr</code> to avoid issues with lifecycles.</p>

<p>
I followed the basic tutorials from LearnOpenGL to render a cube while at the same time writing classes to organize the code. I then built on top of classes like the Texture and Shader class to make a Material class.
</p>

<p>
I made these classes have configurability to make it simpler for myself to add or tweak elements in the scene and to keep the code organized.

ASsimp was used to import 3D models, OpenGL 3.3 was used for rendering, glm for math functions, vectors, and matrices, and stbi for loading textures.

Overall, I found the experience to have provided me with a lot of context as to how rendering works.
</p>


<h1>Source Code</h1>

<a href="https://git.hku.nl/joelle.ubink/glslopdrachten">Project Link</a>

{% end %}

{% toggle_paragraph(level=2, col_start="1", col_span="8", row_start="9", row_span="4") %}
Gallery

<div>{{gallery(excluded=["vlc_2025-09-29_21-05-31.png", "opdrachten_2025-05-30_19-56-24.png", "opdrachten_2025-06-06_10-32-13.mp4"])}}</div>


{% end %}



{% end %}
