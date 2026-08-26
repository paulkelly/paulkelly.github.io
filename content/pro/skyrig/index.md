+++
title = "Skyrig"
subtitle = "Automation game set on a gas giant"
small_image = "skyrig.png"
image = "skyrig-title.jpg"
#startDate = "2025-01-01"
endDate = "2025-09-01"
categories = [ "Unity", "Game", "Rocket Flair", "Steam" ]
tags = [ "Steam", "Automation", "DOTS", "ECS", "Job System" ]
show_date = false
+++

***Build floating automated rigs in a volatile gas giant. Extract elements, synthesize compounds, and descend through atmospheric layers in this sci-fi systems-builder focused on chemistry, engineering, and survival.***<br>

---

**Co Game Director** : ECS Simulation, Tool Development, Shaders, Game Design<br>

---


I took on the role of Technical Lead for Skyrig, with a particular focus on designing the technical foundations needed to support a large-scale automation simulation. One of the key challenges was enabling potentially huge numbers of objects to update efficiently. We addressed this using a hybrid GameObject and Entity system: buildings constructed by the player remain as GameObjects, while a pure data representation of the simulation is maintained separately. Resources, which can be created, destroyed and moved in large numbers, are represented as Entities. The core simulation was implemented using ECS systems and Unity's Job System, allowing the majority of the simulation work to run off the main thread. This kept the simulation highly performant as the scale and complexity of the player's automation network increased.  <br><br>

The game world is divided into sectors that the player can build within. The underlying data and simulation continue to run regardless of the player's location, but when a player enters a sector, the relevant GameObjects and Entities are created. This allowed us to maintain a persistent simulation across the world while limiting the number of active objects that needed to exist at any one time.<br><br>

I also focused on making the game as easy as possible to expand with new content. Based on challenges we had experienced adding content to previous projects, I designed the building and content systems to be highly data-driven. New buildings could be created through ScriptableObjects containing their core data, such as models, icons, names and costs. Their functionality was built using a component-based approach, allowing features such as production or power generation and consumption to be combined as needed. I also created a tool to automatically generate building icons for use throughout the in-game construction menus.<br><br>

Another area I worked on was visual communication. I developed shaders for the game's different information lenses, helping players better understand the complex systems and activity within their growing industrial networks.<br><br>

For progression, we used a node-based visual tool I had previously developed for implementing tutorials and objectives. Similar in concept to Unreal's Blueprints, this tool allowed progression to be configured and managed visually, making it easier to create and iterate on tutorial flows and objectives without requiring them to be hard-coded.<br><br>

I also contributed extensively to the UI. We designed the game's architecture so that core game code never depended on UI scripts, keeping the simulation and presentation layers separate. Instead, the UI accessed the information it needed directly from scene objects or the main simulation data, making the overall architecture more modular and reducing dependencies between gameplay and interface systems.<br><br>

---
<h3>Announcment Trailer</h3>
{{< youtube cNMC9by34uA >}}