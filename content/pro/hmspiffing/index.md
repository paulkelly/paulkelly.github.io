+++
title = "Her Majesty's SPIFFING"
subtitle = "Comedy Point & Click Adventure"
small_image = "spiffing.png"
image = "spiffing-title.jpg"
#startDate = "2016-01-01"
endDate = "2016-12-01"
categories = [ "Unity", "Game", "Billygoat" ]
tags = [ "Console", "Steam", "Point & Click", "Adventure", "Comedy" ]
show_date = false
+++

[![Steam](/icons/steam.svg)](https://store.steampowered.com/app/488770/Her_Majestys_SPIFFING/)<br><br>

***Her Majesty's SPIFFING is a quaint graphic adventure game following the exploits of Captain Frank Lee English and his trusted regional accented colleague, Aled, as they travel through the cosmos in search of planets to claim for a new Galactic British Empire!***<br>

---

**Developer** : Programing, Dialogue System Tool, Puzzle & Minigame Design<br>

---
I joined HM Spiffing a few months into development, after an initial prototype had been created and as the team was preparing to launch its Kickstarter campaign.<br><br>

One of my main contributions was developing an editor tool for setting up the game's dialogue and game flow. Conversations could be created using a flowchart-style interface, linking dialogue text with the appropriate voice clips and animation files. The tool also automatically split text into lines that would fit neatly within the subtitle box, while intelligently calculating how long each line should remain on screen.<br><br>

A major issue when I joined the project was a number of bugs caused by different systems attempting to take control of the player character at the same time. I addressed this by creating a hierarchical state machine that determined which system had control at any given time. As well as resolving many of these race-condition bugs, the new system made the game feel much more responsive by allowing control to be returned to the player while other systems were still active. For example, players could now continue walking around while dialogue was playing.<br><br>

I contributed to the design and implementation of puzzles and minigames, as well as many of the smaller details that helped make the game feel polished. This included the flying minigame, footsteps that played different sound effects depending on the surface the character was walking on, and voice clips that responded to the player while changing settings in the menus. I also worked to ensure that logical player interactions were acknowledged throughout the game. For example, allowing the player to spill a cup of tea by turning it upside down while examining it. These small interactions helped reward players for experimenting with it.<br><br>

---
<h3>Launch Trailer</h3>
{{< youtube haJDhK-TXrY >}}