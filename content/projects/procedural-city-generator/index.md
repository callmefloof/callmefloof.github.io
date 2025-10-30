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

col_start = 5
col_span = 4
row_start = 1
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

<p>During my first year at HKU, I developed a procedural city generator over a 5–6 month period as my end-of-year project.
The goal was to generate an infinite, grid-based city world in real time while maintaining stable performance and visual quality.
I began the project in Godot but switched to Unity for its superior debugging tools and faster iteration times.
The system uses layered image maps to define city features such as roads, buildings, terrain, and water, with buildings spawned dynamically around the player using a <i>floating origin system</i>.
This setup allowed the world to reach <i>millions</i> of in-game units in size without precision issues.</p>

<p>Despite performance challenges during regeneration, the project successfully demonstrated a large-scale procedural environment with static lighting, parallax windows, and an adaptable runtime generation system.</p>

{% end %}

{% end %}
{% end %}

{% end %}

{% toggle_paragraph(level=2, col_start="1", col_span="8", row_start="5", row_span="4") %}
Details

<p>The generator is built around a layer-based procedural pipeline.
Each layer corresponds to a map (e.g., roads, height, land/water), defined by a custom script that interprets pixel values to determine what should spawn and where.
For instance, a <i>roadmap</i> layer uses binary space partitioning to subdivide space and generate a grid-like street layout—white pixels represent buildable zones, while black pixels mark roads.
Other layers define building heights (via height maps) and land/water placement.</p>

<p>
Objects are instantiated on-the-fly based on the player’s position within a virtual coordinate space, calculated from map pixel size and in-game scale.
The floating-origin system re-centers the player whenever they move too far from the origin, preventing floating-point precision loss while keeping virtual travel distances consistent.
When regeneration occurs, the player is repositioned to the origin and the surrounding city is rebuilt according to their virtual coordinates.
</p>

<p>
To optimize performance, all prefabs include prebaked lightmaps, allowing distant lighting to remain static, and parallax mapping adds depth to window surfaces.
However, regeneration remained a major performance bottleneck, beyond a 20×20 map region, frame rate dropped significantly.
I mitigated this by spreading object instantiation over multiple frames, trading reduced stutter for visible world “popping.”
Although I could not fully solve this due to time constraints, possible improvements include object pooling, hierarchical LODs, and (GPU-accelerated) occlusion culling.
</p>

<p>
Overall, the project proved a functional, large-scale procedural city system capable of dynamic world generation and spatial streaming.
It served as an early exploration into scalability, floating origin mechanics, and balancing performance trade-offs in procedural world design.
</p>


<h1>Source Code</h1>
<a href="https://git.hku.nl/joelle.ubink/vygr-unity">Project Link</a>

{% end %}

{% end %}
