+++
title = "C# Behavior Tree"
description = ""
[taxonomy]
tags = ["C#", "Unity"]
[extra]
index = 3
preview_image = ""
preview_video = ""
is_youtube = true
tags = ["C#", "Unity", "AI", "Simulation"]
yvid_id = "OoIPVOmgLnA"
+++

{{youtube(id="OoIPVOmgLnA", width="1280", height="720", class="youtube-video")}}

# [Project Link](https://git.hku.nl/joelle.ubink/unityaibehaviortree)

For this assignment, I developed a Behavior Tree system for AI agents, specifically a guard and a rogue. I created a hierarchical Behavior Tree structure with a BTNode base class, which includes composite (BTCompositeNode), decorator (BTDecoratorNode), and task (BTTaskNode) nodes. Each of these serves a distinct function, such as managing execution flow, modifying behavior, or performing specific agent actions.

I implemented several task nodes, including BTWalkToPointNode, BTAttackPlayerNode, and BTThrowSmokeBombNode, to handle movement, combat, and interactions. The Guard and Rogue AI agents use this system, with the Guard detecting and reacting to the player. To facilitate communication between agents, I implemented a GlobalBlackboard, allowing the rogue to respond to changes in the guard’s state.

I structured the tasks into generic and agent-specific categories to maximize reusability while maintaining flexibility. Additionally, I made the BTLogNode capable of updating text above the agent’s head for easier debugging.