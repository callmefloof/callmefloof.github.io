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

project_year = "July, 2025"
project_type = "Solo project"
project_duration = "Ongoing"


col_start = 1
col_span = 4
row_start = 1
row_span = 2

+++

{% grid(columns=8,rows=8) %}

{% toggle_paragraph(open="open", col_start="5", col_span="4", row_start="1", row_span="4" level=2) %}
Summary

<p>I built a compact, high-performance Entity Component System module that embeds <a href="">FLECS</a> directly into Godot as a statically linked native module to simplify console porting and keep simulations fast and predictable.
An initial prototype that used Godot <code class="language-cpp">Resource</code> / <code class="language-cpp">RefCounted</code> objects caused severe heap pressure under bulk create/destroy (stress tests spiked memory above ~40 GB), so I rewrote the bridge as a <a href="https://docs.godotengine.org/en/stable/engine_details/architecture/custom_godot_servers.html"><i>Godot Server</i></a> exposing opaque <code class="language-cpp">RID</code> handles via a <code class="language-cpp">FlecsServer</code> API.
This allows designers and scripters to access entities and components from GDScript without creating thousands of Godot heap objects.
I validated the system with a real-time <a href="https://docs.godotengine.org/en/stable/tutorials/performance/using_multimesh.html"><i>MultiMesh</i></a> demo (the “Bad Apple” animation rendered as a grid of cubes).
The module is production-oriented, lowers runtime overhead, and is designed with console/static-link requirements in mind.</p>

{% end %}

{% gridcell(col_start=1,col_span=4,row_start=1,row_span=4) %}

{{youtube(id="P6AEflA3roU", width="1280", height="720", class="youtube-video")}}

{% end %}

{% toggle_paragraph(level=2, col_start="1", col_span="8", row_start="5", row_span="4") %}
Details

<p>The core uses <i><a href="https://www.flecs.dev/flecs/" >FLECS</a></i>, statically linked into Godot; entity and component lifetime, memory layout, and hot-path logic live fully in native C++. Script-side access is provided through <code class="language-cpp"><a href="https://docs.godotengine.org/en/stable/classes/class_rid.html">RID</a></code> handles managed by a <code class="language-cpp"><a href="https://github.com/callmefloof/godot-turbo/blob/main/ecs/flecs_types/flecs_server.h">FlecsServer</a></code> Godot Server, avoiding per-entity <code class="language-cpp"><a href="https://docs.godotengine.org/en/stable/classes/class_object.html">Object</a></code> allocations.
The earlier Resource-based reflection layer was discarded after profiling revealed delayed reclamation and catastrophic memory growth when rapidly creating or destroying large numbers of objects.</p>

<p>Rendering validation used a single **MultiMesh** driven by ECS-managed transforms to confirm efficient batched updates.
An experimental per-instance frustum/occlusion culling system was tested, but per-frame GPU buffer uploads caused CPU–GPU sync stalls and frame-time spikes.
Future improvements include GPU-driven culling via compute shaders and indirect draws, asynchronous or double-buffered instance uploads through the RenderingServer, and editor-friendly serialization that avoids reintroducing per-entity Godot objects.
Longer-term plans involve moving native simulation to worker threads while keeping Godot API access on the main thread.</p>

<p>In interviews I focus on the memory-debugging investigation, the trade-offs between <code class="language-cpp">RID</code> and <code class="language-cpp">Object</code> ergonomics, and approaches to eliminate remaining rendering bottlenecks.</p>

<h1>Update — Expanding the Flex Module</h1>

I’ve recently expanded the Flex module with a more complete feature set. The main focus was on introducing Flex Queries and Flex Systems, separating them from the original Flex Script System to give the runtime a cleaner and more modular structure. This makes it easier to define and manage systems without mixing in script logic, and it sets a stronger foundation for future tools and extensions.

This update was mostly about rounding off the API — polishing what was there, validating how it all fits together, and making sure the module feels cohesive and ready for production use. It’s now in a place where I can confidently start building the editor toolset on top of it.

Once that’s done, I’ll move on to rebuilding my earlier Procedural City Generator demo using the new system. The idea is to push it further and show how these new features can drive larger, more complex simulations while keeping everything flexible and performant.

<h1>Source Code</h1>
<a href="https://github.com/callmefloof/godot-turbo">Project Link</a>

{% end %}

{% end %}
