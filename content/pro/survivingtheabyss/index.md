+++
title = "Surviving the Abyss"
subtitle = "Atmospheric horror city builder"
small_image = "abyss.png"
image = "abyss-title.jpg"
#startDate = "2023-12-01"
endDate = "2025-01-01"
categories = [ "Unity", "Game", "Rocket Flair" ]
tags = [ "Steam", "City Builder", "Job System" ]
show_date = false
+++

[![Steam](/icons/steam.svg)](https://store.steampowered.com/app/1254320/Surviving_the_Abyss/)<br><br>

***Earth, 1976. You have been tasked with managing a deep-sea science facility working to perfect cloning. Explore the darkness and keep your crew alive in this hardcore survival colony builder. And beware. The darkness hides untold horrors.***<br>

---

**Developer** : Balance, Design, Additional Content, Optimisation, Bug Fixing<br>

---

I was part of a small team responsible for taking the project from Early Access through to its full release. My work focused primarily on game design, balancing, narrative content, and helping improve the game's overall stability.<br><br>

A significant part of my role involved identifying and addressing points where progression would slow down and players could feel stuck. We approached this by repeatedly playing through the game as far as possible, identifying the point at which momentum began to stall, and investigating the systems responsible. The solutions ranged from small balance adjustments to introducing entirely new buildings or narrative events that gave players new ways to progress.<br><br>

I made a significant change to one of the game's core progression systems. Players needed to search the ocean floor for genetic material in order to clone new crew members. Originally, they could stockpile multiple copies of material from a single source and combine them to create increasingly powerful crew. I redesigned the system so that each source could provide only one unique instance of genetic material, which could then be used repeatedly. This shifted the dynamic from finding a small number of sources and waiting to accumulate enough material to continuously exploring the ocean floor in search of new discoveries. The result was a more engaging progression loop that encouraged exploration and made the overall experience feel much more compelling. <br><br>

As an example of a smaller features I worked on, I added schools of fish that react to the player's mouse cursor to make the underwater environment feel more alive. When the cursor moves quickly past them, or when they are clicked on, the fish scatter and swim away. I used Unity's Job System and a swarming algorithm to support large numbers of individually moving fish without introducing a significant performance overhead.<br><br>

I also expanded the game's narrative content, with a particular focus on strengthening its horror and atmosphere. In the Early Access version, a creature would appear relatively early and begin attacking the player's colony. I wanted to make this threat feel more mysterious and build anticipation over a longer period, so I created new narrative events that gradually introduced the creature and developed a growing sense of unease before revealing more of the threat. The game's atmosphere was one of its strongest qualities, and developing this aspect of the experience was something I found particularly engaging.<br><br>

I also designed and implemented a new final biome and the content needed to bring the game to a conclusion. This final area saw the player fighting their way through an expanding "creep", gradually building closer to the source of the monster and the culmination of the game's narrative.<br><br>

Finally, the Early Access version contained several significant bugs and technical issues. As a team, we spent considerable time addressing these problems, improving stability and implementing optimisations to ensure the full release provided a smoother and more reliable experience.<br><br>

---
<h3>Announcment Trailer</h3>
{{< youtube njF-9qjGw_4 >}}