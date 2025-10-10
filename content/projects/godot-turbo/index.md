+++
title = "Godot Turbo"
description = "A lightweight Entity-Component-System Module for Godot."
[taxonomy]
tags = ["C++", "Godot", "Flecs", "Engine", "Solo Project"]
[extra]
index = 0
preview_image = ""
preview_video = ""
is_youtube = true
tags = ["C++", "Godot", "Flecs", "Engine", "Solo Project"]
yvid_id = "P6AEflA3roU"
+++



{{youtube(id="P6AEflA3roU", width="1280", height="720", class="youtube-video")}}


# [Project Link](https://github.com/callmefloof/godot-turbo)


I made this module to have access to a fast, reliable ECS that could be integrated on a close level with Godot. I chose [FLECS](https://github.com/SanderMertens/flecs) because of its rich feature set and performance. Godot had other options and alternatives for implementing a ECS. These solutions however did not satify my requirements of having a low-level, well-optimized ECS being statically linked to Godot. Static linking provides the opportunity to simplify porting to Consoles as dynamic linking is not permitted on those platforms.

Initially I created an implentation relying on extending the Godot [Resource](https://docs.godotengine.org/en/stable/classes/class_resource.html) class as it provided a convenient way to write a reflection layer. This did not end up working due to the memory size and heap allocated nature of the underlying RefCounted and Object class. When creating or destroying a lot of instances at once memory would not be cleared quickly enough for it to add up. This caused the memory usage to spike above 40gbs.


I then scrapped most of the work done on the class structure and revised it to be a [Godot Server](https://docs.godotengine.org/en/stable/engine_details/architecture/custom_godot_servers.html), relying on [resource ID's](https://docs.godotengine.org/en/stable/classes/class_rid.html) to allow GDScript users to access Flecs via the [FlecsServer](https://github.com/callmefloof/godot-turbo/blob/main/ecs/flecs_types/flecs_server.h) class.

I also experimented with making a system to individually cull Multimesh instances, but this proved to be too challenging. I could not find update the buffer on the GPU with computed frustum and occlusion culling results without having significant framerate issues.

To test if it would work, I made a system rendering Bad Apple as spaced grid of cubes managed through a multimesh instance.

