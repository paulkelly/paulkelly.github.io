+++
title = "Parcel Corps"
subtitle = "High-octane bicycle courier game"
small_image = "parcel.png"
image = "parcel-title.jpg"
#startDate = "2020-10-01"
endDate = "2024-10-01"
categories = [ "Unity", "Game", "Billygoat" ]
tags = [ "Console", "Steam", "Physics", "Online", "3D Platformer" ]
show_date = false
+++

[![Steam](/icons/steam.svg)](https://store.steampowered.com/app/2015960/Parcel_Corps/)<br><br>

***Ditch the 9-5 and embrace the high-octane life of a freelance bicycle messenger! Skid, grind, and wallride across eight huge levels, delivering parcels for a cast of eccentric business owners. Find shortcuts, dodge traffic, and maybe even save the world!***<br>

---

**Lead Programmer** : Player Controller and Cycling Physics, Gameplay Systems, Online Multiplayer, Leaderboards, Console Integration, Game Design, Level Design<br>

---

I was involved with Parcel Corps from the beginning, creating the first prototype for the player controller and cycling physics. A key part of this early work was understanding what made the bike feel convincing to control. In particular, I found that the rear wheel needed to follow the same path as the front wheel to avoid the bike feeling as though it was slipping. Using the relationship between the bike's wheelbase, steering angle and velocity, I developed the movement system to produce appropriate turning behaviour at different speeds.<br><br>

I spent much of the project refining the player physics, balancing responsiveness with believable movement and working to ensure the bike looked as natural as it felt to control. This required close collaboration with the animation team, as the movement and physics systems needed to work alongside the character and bike animations to create a cohesive result.<br><br>

I was responsible for implementing the game's online features, including multiplayer, cross-platform leaderboards and online ghost players. This involved writing the systems for matchmaking, character synchronisation and the game's online modes.<br><br>

For character synchronisation, I implemented a technique to help hide the effects of network latency without making other players appear jittery. The system maintained a small buffer of position data and adjusted playback speed dynamically: slowing down as the buffer began to run low, then speeding back up when sufficient data was available. This allowed movement to remain smooth while adapting to fluctuations in network conditions.<br><br>

I also built the cross-platform leaderboard infrastructure using AWS, with the database and supporting scripts for accessing and managing the data handled by our team. When players uploaded a delivery time to the leaderboard, they would also upload a ghost; a recording of their route and performance. These ghosts could then appear in other players' worlds, allowing them to encounter other players as they played.<br><br>

I was also heavily involved in level design. I created some of the early gameplay playgrounds used for testing movement and mechanics, which later became part of a finished level, as well as independently whiteboxing an entire level. Navigation was a major part of the game's delivery gameplay, with players needing to learn each environment and find efficient routes between destinations. One of the challenges we encountered was the time it could take for players to become familiar with a new level, and I particularly enjoyed designing memorable landmarks and visual points of interest, "[weenies](https://themouselets.com/what-is-a-disney-weenie)", that players could use to orient themselves and build a mental map of the environment.<br><br>

A couple of other interesting systems I worked on were the player's in-game mobile device and the delivery navigation systems. I developed a system for managing apps on the mobile device that was designed to be easy to use, allowing non-technical team members to create and configure new apps without requiring programmer involvement. I also created the minimap system used during deliveries, along with a pathfinding system that could generate and display a route between the player and their destination.<br><br>

---
<h3>Gameplay Trailer</h3>
{{< youtube 0IyJ2mR3TP4 >}}