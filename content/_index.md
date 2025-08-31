+++
title = "Joëlle Ubink - Game System Developer"

description = "Game Developer Portfolio"

# A draft section is only loaded if the `--drafts` flag is passed to `zola build`, `zola serve` or `zola check`.
draft = false

# Used to sort pages by "date", "update_date", "title", "title_bytes", "weight", "slug" or "none". See below for more information.
sort_by = "none"

# Used by the parent section to order its subsections.
# Lower values have higher priority.
weight = 0

# Template to use to render this section page.
template = "index.html"

# This sets the number of pages to be displayed per paginated page.
# No pagination will happen if this isn't set or if the value is 0.
paginate_by = 10

# If set, this will be the path used by the paginated page. The page number will be appended after this path.
# The default is page/1.
paginate_path = "page"

# If set, there will pagination will happen in a reversed order.
paginate_reversed = false

# This determines whether to insert a link for each header like the ones you can see on this site if you hover over
# a header.
# The default template can be overridden by creating an `anchor-link.html` file in the `templates` directory.
# This value can be "left", "right", "heading" or "none".
# "heading" means the full heading becomes the text of the anchor.
insert_anchor_links = "none"

# If set to "true", the section pages will be in the search index. This is only used if
# `build_search_index` is set to "true" in the Zola configuration file.
in_search_index = true

# If set to "true", the section homepage is rendered.
# Useful when the section is used to organize pages (not used directly).
render = true

# If set to "true", the section will pass its pages on to the parent section. Defaults to `false`.
# Useful when the section shouldn't split up the parent section, like
# sections for each year under a posts section.
transparent = false

# Use aliases if you are moving content but want to redirect previous URLs to the
# current one. This takes an array of paths, not URLs.
aliases = []

# If set to "true", feed files will be generated for this section at the
# section's root path. This is independent of the site-wide variable of the same
# name. The section feed will only include posts from that respective feed, and
# not from any other sections, including sub-sections under that section.
generate_feeds = false

# Your own data.
[extra]
linkedin_link = "https://www.linkedin.com/in/jo%C3%ABlle-ubink-561156155/"
itchio_link = "https://callmefloof.itch.io/"
email = "mailto:contact@joelleubink.com"
hku_git_link = "https://git.hku.nl/users/joelle.ubink/projects"
github_link = "https://github.com/callmefloof"
gitlab_link = "https://gitlab.com/callmefloof"

programming_languages = [
    "C#",
    "C++",
]
programming_languages_skill_levels = [
    76,
    100
]

game_engines = [
    "Unity",
    "Godot",
    "Unreal Engine"
]

+++


{{ heroh1(body="About Me") }}

<div class="clear-image">

{{resize_image(class="hero-img" style="" path="/images/who.png", width=400, height=600, op="fit")}}

I’m a game development student and aspiring gameplay programmer, eager to explore and develop systems that create emergent interactions between players and the game world. I’m fascinated by breaking down game mechanics into structured, scalable systems and aspire to tackle challenges like crowd simulation, in-game relationship management, combat mechanics, and leveling systems. While I’m still building experience in these areas, I have a strong ability to mentally map system interactions and a deep curiosity for how mechanics shape player experiences. I’ve also been practicing working with various levels of system complexity, adapting designs based on the needs of the game.

Beyond gameplay systems, I have a strong passion for programming itself. I’m actively improving my skills by studying design patterns, optimizing code efficiency, and exploring new ways to create responsive and dynamic game systems.

</div> 

<br/>
<br/>

-----------------------------------------

{{heroh1(body="Development Skills")}}
<div style="margin:auto; width:40%">
    <h2 class="hero-h2" style="text-align:center">Programming Languages</h2>
    {{skilllist(skills=["C#","C++"])}}
</div>


<div style="margin:auto; width:40%">
    <h2 class="hero-h2" style="text-align:center">Game Engines</h2>
    {{skilllist(skills=["Unity","Godot", "Unreal Engine"])}}
</div>

-----------------------------------------

{{heroh1(body="Links")}}

{{contactlinks()}}
<br/>

-----------------------------------------

{{heroh1(body="Projects")}}

