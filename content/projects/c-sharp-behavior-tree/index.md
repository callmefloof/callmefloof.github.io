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

col_start = 1
col_span = 3
row_start = 5
row_span = 2

+++

{% grid(columns=8,rows=8) %}

{% toggle_paragraph(open="open", col_start="5", col_span="4", row_start="1", row_span="4" level=2) %}
Summary
{% end %}

{% gridcell(col_start=1,col_span=4,row_start=1,row_span=4) %}
{{ youtube(id="OoIPVOmgLnA", width="1280", height="720", class="youtube-video") }}
{% end %}

{% toggle_paragraph(col_start="1", col_span="8", row_start="5", row_span="4" level=2) %}
Details

<p>
    I developed a Behavior Tree system for AI agents, specifically a guard and a rogue. I created a hierarchical Behavior Tree structure with a BTNode base class, which includes composite <code class="language-c-sharp">BTCompositeNode</code>, decorator  <code class="language-c-sharp">BTDecoratorNode</code>, and task <code class="language-c-sharp">BTTaskNode</code> nodes. Each of these serves a distinct function, such as managing execution flow, modifying behavior, or performing specific agent actions.

</p>

<p>
I implemented several task nodes, including <code class="language-c-sharp">BTWalkToPointNode</code>, B<code class="language-c-sharp">TAttackPlayerNode</code>, and <code class="language-c-sharp">BTThrowSmokeBombNode</code>, to handle movement, combat, and interactions. The Guard and Rogue AI agents use this system, with the Guard detecting and reacting to the player. To facilitate communication between agents, I implemented a <code class="language-c-sharp">GlobalBlackboard</code>, allowing the rogue to respond to changes in the guard’s state.
</p>

<p>
I structured the tasks into generic and agent-specific categories to maximize reusability while maintaining flexibility. Additionally, I made the <code class="language-c-sharp">BTLogNode</code> capable of updating text above the agent’s head for easier debugging.
</p>

<h1>Source Codde</h1>
<a href="https://git.hku.nl/joelle.ubink/unityaibehaviortree">Project Link</a>
{% end %}

{% end %}
