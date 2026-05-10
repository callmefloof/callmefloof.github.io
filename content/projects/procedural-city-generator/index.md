+++
title = "Procedural City Generator"
sort_by = "date"
description = "A procedural city generator made in Unity."
assets = [
    "Asset-2@3bxa.png",
    "brave_2024-02-19_17-31-41.png",
    "HeightMap.png",
    "map2.png",
    "mapLand.png",
    "RoadLayout.png",
    "Unity_2024-04-26_01-09-16.png",
    "Unity_2024-04-26_03-02-05-scaled.jpg"
]

[taxonomies]
tags = ["Unity", "C#", "Procedural Generation", "Open World", "Solo Project"]


[extra]
index = 0
preview_image = ""
preview_video = ""
tags = ["Unity", "C#", "Procedural Generation", "Open World", "Solo Project"]
is_youtube = true
yvid_id = "5ESn7UH4CiY"

project_year = "November 2023"
project_type = "Solo project"
project_duration = "5 months"


col_start = 1
col_span = 4
row_start = 3
row_span = 2


+++

{% grid(columns=8,rows=8) %}

{% gridcell(col_start=1,col_span=8,row_start=1,row_span=4) %}

{% grid(columns=4,rows=1) %}

{% gridcell(col_start=1,col_span=2,row_start=1,row_span=1) %}
{{youtube(id="rSOtIdGTKd0", width="1280", height="720", class="youtube-video")}}
{% end %}

{% gridcell(col_start=3,col_span=2,row_start=1,row_span=1) %}

{% toggle_paragraph(open="open" level=2, col_start="1", col_span="8", row_start="1", row_span="4") %}
Summary

<p>This project was my first deep dive into procedural world generation. I wanted to see how a city could build itself dynamically in Unity, using layered images to place roads, buildings, and water. Along the way I learned how to manage large-scale worlds, implement a floating origin to keep positions stable, and deal with performance bottlenecks during regeneration. It taught me a lot about balancing creativity with technical limits, and how to make complex systems feel responsive and believable.</p>

{% end %}

{% end %}
{% end %}

{% end %}

{% toggle_paragraph(level=2, col_start="1", col_span="8", row_start="5", row_span="4") %}
Details

<p>This was one of my first experiments in creating large, dynamic worlds. I wanted to see how far I could push procedural generation inside Unity while keeping it readable and modular. The project started in Godot but later moved to Unity for its stronger profiling and debugging tools.

The generator reads layered images to decide where roads, buildings, and water should go. Each layer has its own interpreter script, allowing me to tweak parameters individually and see changes in real time. Roads are generated using a Binary Space Partition (BSP) system that helps define blocks and intersections, while building height is derived from a grayscale heightmap. To keep everything stable at large scales, I implemented a floating origin system that recenters the world as the player moves.

Performance was the biggest challenge. Regenerating chunks caused heavy frame spikes, especially at higher detail levels. I mitigated some of this by spreading out instantiation over multiple frames, which reduced stutter but introduced some visible pop-in. If I revisit this project, I’d like to explore asynchronous generation and object pooling to keep things smooth, and perhaps use GPU instancing or impostors for distant geometry.

Despite its rough edges, the project gave me valuable insight into how procedural content can be streamed, how data and design constraints influence performance, and how to balance technical ambition with practical iteration.</p>


<h1>Source Code</h1>
<a href="https://git.hku.nl/joelle.ubink/vygr-unity">Project Link</a>

{% end %}

{% end %}
