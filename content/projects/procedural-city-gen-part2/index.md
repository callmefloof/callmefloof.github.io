+++
title = "Procedural City Generator Part 2 - Optimized"
description = "A prodecurally generated city in Godot."

[taxonomy]
tags = ["C++", "Godot", "Rendering", "Engine", "Solo Project", "ECS", "Procederal Generation"]
[extra]
index = 0
preview_image = ""
preview_video = ""
is_youtube = true
tags = ["C++", "Godot", "Rendering", "Engine", "Solo Project", "ECS", "Procederal Generation"]
yvid_id = "_ke20NuWtd0"

project_year = "April/May 2026"
project_type = "Solo project"
project_duration = "Ongoing since Summer 2025"


col_start = 1
col_span = 5
row_start = 1
row_span = 2



+++


{% grid(columns=8,rows=8) %}

{% gridcell(col_start=1,col_span=4,row_start=1,row_span=4) %}

{{youtube(id="_ke20NuWtd0", width="1280", height="720", class="youtube-video")}}

{% end %}

{% toggle_paragraph(open="open", col_start="5", col_span="4", row_start="1", row_span="4" level=2) %}
Summary

<p>This project is a Godot-based continuation of a procedural city prototype I originally built in Unity during 2023–2024. I restarted it using my custom Godot Turbo module to test whether the technical foundation for my game could actually work at scale with the CPU forming the largest bottleneck as not much else is being rendered.</p>

<p>The current prototype generates and renders dense city environments at runtime, including facade geometry, prefab-driven lighting data, and large-world support through a floating origin system.</p>

<p>Current performance at 4K resolution on an RTX 4070 Ti Super, Ryzen 5900X, and 64GB DDR4 RAM:</p>

<ul>
    <li>Around 100–200 FPS on average, depending on city density</li>
    <li>Dense scenes include many generated buildings and light sources</li>
    <li>Runtime memory usage is currently around 1 GB</li>

<p>This is still prototype footage, not a finished art pass. The current phase is about proving technical viability before expanding the project with more people.</p>

{% end %}

{% toggle_paragraph(level=2, col_start="1", col_span="8", row_start="5", row_span="4") %}
Details


<p>The prototype uses Godot’s Forward+ renderer together with RenderServer-based indirect rendering to handle large amounts of generated geometry efficiently.</p>

<p>For lighting, I replaced reliance on SDFGI with a cheaper surface-based approximation using quantized ray samples. The result is more stylized and toon-like, but that fits the project’s intended look while keeping the rendering cost much lower.</p>

<p>The project is currently solo-developed, but it is not intended to stay that way forever. This phase is mainly about building enough of the technical foundation to show that the game’s city rendering and procedural environment systems are feasible.</p>

<p>The codebase has grown to over 200 C++ files (source and header files) spread across 5 modules made, so I use an LLM-assisted workflow to help manage planning and iteration. I use it to discuss system design, turn features into implementation plans, and guide code-generation tools. I still review, test, correct, and integrate the resulting work myself.</p>

<p>I am currently working on crowd systems, improving city density, and building a stronger demo scene. The biggest bottleneck at this stage is asset creation rather than core technology.</p>


{% end %}

{% end %}
