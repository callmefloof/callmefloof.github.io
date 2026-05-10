+++
title = "Unity Basketball AI"
description = ""
assets=["vlc_2025-03-02_22-53-12.png"]
[taxonomy]
tags = ["C#", "Unity", "AI", "Fuzzy Logic", "Duo Project"]
[extra]
index = 3
preview_image = "vlc_2025-03-02_22-53-12.png"
preview_video = ""
is_youtube = true
tags = ["C#", "Unity", "AI", "Fuzzy Logic", "Duo Project"]
yvid_id = "lks7dUlJo6w"
project_year = "Febuary 2023"
project_type = "Duo project"
project_duration = "1.5 months"
col_start = 5
col_span = 3
row_start = 3
row_span = 2


+++





{% grid(columns=8, rows=10) %}

{% toggle_paragraph(open="open", level=2 col_start="1", col_span="4", row_start="1", row_span="4") %}
Summary

<p>While studying at Hanze University of Applied Sciences, my teammate and I developed a basketball simulation game featuring AI-controlled teams. My primary role was designing the AI, ensuring it could make strategic decisions and react dynamically to in-game situations. To achieve this, I built a StateMachine to manage different behaviors, an EnvironmentalInfoComponent to process game data and suggest actions, and a ReflexBehavior system to handle instinctive reactions, such as jumping to block a shot.</p>

{% end %}

{% gridcell(col_start=5, col_span=4, row_start=1, row_span=4) %}

{{youtube(id="lks7dUlJo6w", width="1280", height="720", class="youtube-video")}}

{% end %}



{% toggle_paragraph(level=2 col_start="1", col_span="8", row_start="5", row_span="4") %}
Details

  <h1>AI Logic</h1>
  <p>
  The AI continuously evaluates its environment, adapting its actions based on factors like ball possession, opponent positioning, and scoring opportunities. The Examine state acts as the AI’s default mode, helping it transition smoothly between actions like passing, defending, or moving toward the hoop. The ball mechanics were carefully designed to respond to player movement speed, creating a more fluid and realistic experience.
  </p>

  <h1>Debugging</h1>

  <p>
  One of the biggest challenges was debugging, as the AI’s growing complexity made it difficult to determine whether unexpected behavior was intentional or a bug. Additionally, calculating realistic ball trajectories required a physics-based approach, and I chose to use Unity’s rigid body system rather than manually interpolating the ball’s movement. This ensured that shooting and dribbling felt natural and dynamic.
  </p>

  <h1>Conclusion</h1>

  <p>
  Overall, I am proud of what we accomplished within the given timeframe. However, if I were to continue development, I would focus on cleaning up the code, implementing a custom pathfinding system for better movement control, replacing the simple player models with more detailed ones, and adding an in-game UI for configuring matches before they start.
  </>

  <h1>Source Code</h1>
  <p><a href="https://github.com/callmefloof/basketball_game">Project Link</a></p>

{% end %}

{% end %}
