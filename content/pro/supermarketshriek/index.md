+++
title = "Supermarket Shriek"
subtitle = "Wacky Obstacle Racing Game"
small_image = "shriek.png"
image = "shriek-title.jpg"
#startDate = "2017-12-01"
endDate = "2020-10-01"
categories = [ "Unity", "Game", "Billygoat" ]
tags = [ "Console", "Steam", "Physics", "3D Platformer", "Racing", "Global Game Jam" ]
show_date = false
+++

[![Steam](/icons/steam.svg)](https://store.steampowered.com/app/1086460/Supermarket_Shriek/)<br><br>

***Join man and goat in this chaotic, award-winning couch-co-op adventure! Tackle outlandish obstacle courses, complete rewarding challenges and dodge deadly obstacles in a hectic race to the checkout! Packed with a frantic 38 stage campaign and 3 hilariously fun PvP party modes for 2-8 players.***<br>

---

**Lead Programmer** : Player Controller, Gameplay Systems, Leaderboards, Console Integration, Game Design, Level Design<br>

---
Supermarket Shriek began life as a Global Game Jam project created by myself and Will, the director of Billy Goat Entertainment. Global Game Jam is an event where developers come together to create a game in just 48 hours, with each year built around a central theme. For Global Game Jam 2017, the theme was "Waves". We interpreted this as sound waves and created a game controlled by shouting into a microphone.<br><br>

The original idea was inspired by a web game I had played where you listened to a scream and had to decide whether it had been made by a person or a goat (this also tied into Billygoat's Logo). I combined this with the obstacle-dodging platform games I had enjoyed in custom Warcraft III mods, along with inspiration from the game show Supermarket Sweep. These ideas came together as a chaotic obstacle racing game where players control a shopping trolley using only their voice.<br><br>

We wanted the game to be playable entirely through microphone input, to the point that even starting the game could be done by shouting into the microphone.<br><br>

I worked across almost every area of the project, including the character controller, camera, core game systems, console integrations, and level design. I also designed and whiteboxed around half of the game's levels.<br><br>

One aspect of the game I am particularly pleased with is the number of subtle details that make the shopping trolley feel predictably controllable while still appearing completely out of control. For example, as the trolley moves and skids, it leaves trails behind its wheels. Originally, these formed very uniform circles, which made the movement feel too controlled. I changed the system so the trails were drawn from a randomised point near each wheel, with that position gradually wandering as the trolley moved. This gave the skids a much more chaotic appearance while keeping the underlying movement predictable. Similarly, three of the wheels accurately track the trolley's direction of travel, while the fourth spins unpredictably.<br><br>

From a programming perspective, Supermarket Shriek was a simpler project than many of the other games I have worked on, which gave me more opportunity to focus on design. I particularly enjoyed exploring the range of obstacles and interactions that could respond to the player's voice input, experimenting with different ways shouting and volume could influence gameplay.<br><br>

---
<h3>Gameplay Trailer</h3>
{{< youtube psIU8kZFoak >}}
<br><br>
<h3>2017 Global Game Jam Entry</h3>
{{< youtube ofsdsB3Isng >}}