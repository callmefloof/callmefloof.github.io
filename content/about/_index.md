+++
title = "About me"

description = "about me"

# A draft section is only loaded if the `--drafts` flag is passed to `zola build`, `zola serve` or `zola check`.
draft = false

# Used to sort pages by "date", "update_date", "title", "title_bytes", "weight", "slug" or "none". See below for more information.
sort_by = "none"

# Used by the parent section to order its subsections.
# Lower values have higher priority.
weight = 0

# Template to use to render this section page.
template = "about.html"

# The given template is applied to ALL pages below the section, recursively.
# If you have several nested sections, each with a page_template set, the page
# will always use the closest to itself.
# However, a page's own `template` variable will always have priority.
# Not set by default.
page_template = "blogpost.html"

# This sets the number of pages to be displayed per paginated page.
# No pagination will happen if this isn't set or if the value is 0.
paginate_by = 0

# If set, this will be the path used by the paginated page. The page number will be appended after this path.
# The default is page/1.
paginate_path = "blog"

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
index = 0
preview_image = ""
preview_video = ""
linkedin_link = "https://www.linkedin.com/in/jo%C3%ABlle-ubink-561156155/"
itchio_link = "https://callmefloof.itch.io/"
email = "mailto:contact@joelleubink.com"
hku_git_link = "https://git.hku.nl/users/joelle.ubink/projects"
github_link = "https://github.com/callmefloof"
gitlab_link = "https://gitlab.com/callmefloof"

programming_languages = [
    "C#",
    "C++",
    "Python",
    "HTML/CSS/JS",
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



<div class="clear-image">

{{header_h1(body="About Me", center=true)}}

I make games because I love creating worlds that feel alive and meaningful. What started as a spark from older games has turned into a curiosity-driven drive to capture just the right amount of detail — enough to matter, but still leaving room to experiment and discover better ways to make things work.

I tend to think in a data-first way: I like systems that are clear and predictable, but I also want the code to stay flexible so I can iterate and try new ideas without getting stuck. I don’t have all the answers, and that’s part of the fun — figuring out solutions to problems as they come is what keeps me engaged.

I’m drawn to systems that allow emergent interactions — things like crowd simulation, in-game relationships, combat mechanics, and procedural content. I want to build large, traversable worlds, but with a focus on a few hand-crafted hubs that feel polished and meaningful. These areas should stand out, while still interacting naturally with the broader simulation.

I’m still gaining experience, but I bring a strong ability to map out complex systems in my head and a constant curiosity for how mechanics shape player experiences. I’m always exploring design patterns, optimizing code, and finding ways to make systems responsive, adaptable, and intuitive to work with.
</div>

<br/>
<br/>

-----------------------------------------

{{header_h1(body="Development Skills", center=true)}}

{{header_h2(body="Programming Languages", center=true) }}
{{skilllist(skills=["C#","C++", "HTML/CSS/JS", "Python"])}}

{{header_h2(body="Game Engines", center=true)}}
{{skilllist(skills=["Unity","Godot", "Unreal Engine"])}}

<br/>

-----------------------------------------

{{header_h1(body="Links")}}

{{contactlinks()}}
<br/>
