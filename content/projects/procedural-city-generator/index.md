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
tags = ["Unity", "C#", "Procedural Generation", "Open World"]


[extra]
index = 0
preview_image = ""
preview_video = ""
tags = ["Unity", "C#", "Procedural Generation", "Open World"]
is_youtube = true
yvid_id = "5ESn7UH4CiY"
+++
# [Project Link](https://git.hku.nl/joelle.ubink/vygr-unity)

In the first year of my degree program at HKU, I made a procedural city generator for my end-year project over a 5-6 month period.

I started making this procedural city generator in the Godot game engine but later switched to Unity. I switched to Unity as it had better tools for debugging the generation while I was working on it. The system works through layers and the only-the-fly instantiation of prefab objects. This allowed me to implement a floating origin system allowing the map size to reach millions of units without issue.

The layer system works by defining the characteristics of each layer with a custom script that tells the generator how to interpret each pixel of the image layer and how to apply it. The roadmap layout uses binary space partitioning to create a generated grid-based roadmap layout. The white space represents an area for buildings to spawn on while the black space represents a piece of road. The script interpreting the roadmap then interprets this information and instantiates it around the player. The height of buildings is determined through a pre-generated height map. The location of where roads, buildings, and water spawn are based on the Land/Ocean layer where a white pixel correlates to being land and a black pixel water.

The generator spawns objects based on where the player is located in the virtual space. The virtual space is the size of the map in pixels multiplied by the predefined in-game size of a pixel. The player can be placed at any point in the world. The world then gets spawned around the player based on the maximum spawning distance for prefab objects. The world gets regenerated whenever the player travels too far away from their origin point. The origin point is a predefined position in the Unity game world. When the world gets regenerated the position of the player gets reset to the origin point while retaining the distance traveled in virtual space.

The prefabs contained prebaked lightmap information which enabled me to optimize lighting by making lighting static when far away from the player. The windows in the buildings feature parallax mapping for extra detail.

The one major issue I faced during development was the time needed to regenerate the world around the player. At render sizes of greater than 20 by 20 pixels from the map the FPS halves and creates stutter. I was partially able to address this by spreading out the instantiation of objects over a larger amount of frames. This approach created a new issue, however, as the world seemingly reappeared in front of the player, which broke the illusion of a contiguous world space. I ultimately ended up compromising by accepting some level of stutter when the world has to be regenerated.

Due to time constraints, I was not able to look at other potential optimization techniques like object culling, (H)LODs, and object pooling. Nevertheless, I was quite happy with what I was able to make with the allotted time.

{{gallery()}}