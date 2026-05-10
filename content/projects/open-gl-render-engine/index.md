+++
title = "OpenGL Render Engine"
description = "A simple OpenGL renderer built as a learning project to explore rendering architecture, resource management, and material abstraction."

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
row_start = 5
row_span = 2



+++




{% grid(columns=8,rows=12) %}

{% gridcell(col_start=1,col_span=4,row_start=1,row_span=4) %}

{{video(source="opdrachten_2025-06-06_10-32-13.mp4 " style="width:100%;")}}
{% end %}

{% toggle_paragraph(open="open" level=2, col_start="5", col_span="4", row_start="1", row_span="4") %}
Summary

<p>As part of a graphics programming course, I developed a small render engine to better understand modern rendering pipelines. The goal was to go beyond the LearnOpenGL tutorials by organizing the code into reusable classes and managing object lifecycles safely.

I implemented a structured system using std::shared_ptr and std::weak_ptr for resource management, and built Shader, Texture, and Material classes that allowed me to configure and combine assets easily. The engine uses OpenGL 3.3 for rendering, glm for math, stb_image for texture loading, and Assimp for importing 3D models.

This project gave me practical insight into how a renderer handles data flow between CPU and GPU, how materials abstract shader parameters, and how careful memory ownership simplifies engine code.</p>

<h1>Source Code</h1>

<a href="https://git.hku.nl/joelle.ubink/glslopdrachten">Project Link</a>

{% end %}

{% toggle_paragraph(level=2, col_start="1", col_span="8", row_start="9", row_span="4") %}
Gallery

<div>{{gallery(excluded=["vlc_2025-09-29_21-05-31.png", "opdrachten_2025-05-30_19-56-24.png", "opdrachten_2025-06-06_10-32-13.mp4"])}}</div>


{% end %}



{% end %}
