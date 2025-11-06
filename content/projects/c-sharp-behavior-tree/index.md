+++
title = "C# Behavior Tree"
description = ""
[taxonomy]
tags = ["C#", "Unity", "Solo Project"]
[extra]
index = 3
preview_image = ""
preview_video = ""
is_youtube = true
tags = ["C#", "Unity", "AI", "Simulation", "Solo Project"]
yvid_id = "OoIPVOmgLnA"

project_year = "December, 2024"
project_type = "Solo project"
project_duration = "3 weeks"

col_start = 1
col_span = 3
row_start = 5
row_span = 2

+++

{% grid(columns=8,rows=8) %}

{% toggle_paragraph(open="open", col_start="5", col_span="4", row_start="1", row_span="4" level=2) %}
Summary

<p>
    I built a modular Behavior Tree system in Unity to drive AI for a guard and a rogue. The system is structured around a simple <code class="language-c-sharp">BTNode</code> hierarchy with composite, decorator, and task nodes, making it easy to expand or reuse behaviors. A <code class="language-c-sharp">GlobalBlackboard</code> allows agents to react to each other’s state, while debug tools like a floating  <code class="language-c-sharp">BTLogNode</code> make testing straightforward.

    What interested me most was how versatile the Behavior Tree pattern is — beyond AI, it functions almost like a command pipeline that can model any logical flow of actions. The project deepened my appreciation for clean, modular design and how powerful even simple structures can be when built with clarity in mind.

</p>



{% end %}

{% gridcell(col_start=1,col_span=4,row_start=1,row_span=4) %}
{{ youtube(id="OoIPVOmgLnA", width="1280", height="720", class="youtube-video") }}
{% end %}

{% toggle_paragraph(col_start="1", col_span="8", row_start="5", row_span="4" level=2) %}
Details


<p>
I developed a Behavior Tree system in Unity to control two AI agents: a guard and a rogue. The main goal was to create a structure that could manage complex behavior in a modular and reusable way, while staying simple enough to adapt quickly during development. The framework is built around a <code class="language-c-sharp">BTNode</code> base class that branches into composites, decorators, and tasks. Each serves a specific purpose — composites control the flow, decorators modify or conditionally gate execution, and tasks carry out actions like moving, attacking, or reacting to the player.
</p>


<p>
To support interaction between agents, I implemented a <code class="language-c-sharp">GlobalBlackboard</code>, which allows shared data such as awareness states to pass between them. This made it easy for the rogue to respond dynamically when the guard spotted the player. I also added a <code class="language-c-sharp">BTLogNode</code> for runtime debugging, displaying the agent’s current task directly above its head to track behavior at a glance.
</p>

<p>
The real takeaway for me wasn’t just finishing the system, but understanding how flexible the Behavior Tree design pattern is. It’s not just an AI tool — it’s effectively a structured command pattern, where each node is a logical step in a flow of actions. Once I saw it that way, I started imagining how it could drive other systems too: quest scripting, event logic, or world simulation tasks. Its strength lies in how easily it can describe sequences of decisions and reactions without turning into a tangled mess of conditionals.
</p>

<p>If I revisit this project, I’d like to add a visual editor for constructing trees directly in the Unity editor, and possibly layer it with a utility-based decision system for more nuanced agent behavior. Overall, this project reinforced how much I value clean, composable systems — and how a simple, well-structured pattern can unlock a lot of creative potential.</p>

<h1>Source Code</h1>
<a href="https://git.hku.nl/joelle.ubink/unityaibehaviortree">Project Link</a>
{% end %}

{% end %}
