+++
title = "Flight Radar"
subtitle = "Live aircraft around any point on the map"
small_image = "flight-radar.png"
image = "flight-radar-title.jpg"
endDate = "2026-11-12"
categories = [ "ASP.NET Core", "React", "Android", "Solo" ]
tags = [ 'AI Assistance',"C#", "TypeScript", "Kotlin", "Docker", "Azure", "CI/CD", "Real-time" ]
show_date = false
+++

[![GitHub](/icons/github.svg)](https://github.com/paulkelly/nearby-flights) | <a href="https://flightradar-web.delightfulforest-82237f6b.northeurope.azurecontainerapps.io" target="_blank" rel="noopener">Live Site</a><br><br>

***"What's that plane outside my window?"*** <br/><br> ***A hosted web app with a companion Android Widget.*** <br/><br> ***Pick a spot on a map, choose a radius, and see every aircraft flying inside that circle: airline, flight, probable route, altitude and speed, updating live.***<br>

---

**Solo Developed with AI Assistance** : Backend, Frontend, Android, CI/CD, Deployment on Azure <br>

---                                                                                                                                                                                          
I built Flight Radar as a learning project to learn AI-assisted development and to get to grips with a corporate web stack: an ASP.NET Core backend, a React and TypeScript     
frontend, Docker, automated testing, and continuous deployment to the cloud. I worked with an AI coding assistant as a pair programmer. I set   the direction, made the design decisions at each step, and reviewed and tested every change. The project grew in small, focused steps from a single API endpoint to a deployed web app and a companion Android app.<br><br>

Flight data comes from ADS-B, the position broadcasts aircraft send out, collected by volunteer receivers. The backend sits between the app and these community data sources, so it can convert units, retry brief failures, and fall back to a second provider when the first is down. It also caches each area's results so that many viewers cost a single upstream request. To make that work, searches are snapped to a grid before they reach the cache: much like spatial hashing in a game, nearby searches land in the same bucket and share one result.<br><br>                                                                                                 Many of the problems turned out to be familiar from games. Positions arrive every few seconds, so the map uses dead reckoning to extrapolate each aircraft from its speed, track and climb rate    between updates, the same technique used to smooth networked players. A background poller keeps the areas people are watching fresh and lets the rest sleep. Fresh data is pushed to browsers over WebSockets, with one group per area, and Redis passes the messages between server instances.<br><br>

ADS-B says where an aircraft is, but not where it's going. Routes come from a community database of the routes usually flown under each flight number, and they're often out of date, so the backend only shows a route if it fits the aircraft's position and heading. When none fits, the app works out what it can from the aircraft itself: one climbing out of Dublin is "From Dublin", and one descending towards it is "To Dublin".<br><br>
The Android app added a home-screen widget and a lock-screen notification showing the nearest
aircraft to a saved place. Widgets can't hold a connection open, and Android only runs background work every 15 minutes or so, so the server does the watching: it checks each registered location
every minute and sends a Firebase push only when the aircraft the widget would show changes. It works like state replication. The server remembers what each client last saw and sends only the changes, with hysteresis, so that two aircraft at nearly the same distance don't trigger a push every minute. Caps on how many places are watched around the clock keep the load fair on a free community data source.<br><br>

Everything is built and tested on every change. Around 1,800 automated tests cover the backend, frontend and Android app, including tests against real Postgres and Redis instances in throwaway containers. GitHub Actions runs them on every pull request, along with a smoke test of the whole Docker stack. Once a change is merged, it's published as container images and deployed to Azure Container Apps. The infrastructure is described in code (Bicep), and GitHub logs in to Azure with short-lived tokens rather than stored passwords. Dependabot keeps the dependencies up to date, and the workflows themselves are pinned to exact versions.<br><br>

Coming from games turned out to be an advantage. Thinking in time budgets, smoothing movement between network updates and only sending what changed are everyday game techniques, and they made the app fast and kept it light on a free data source. Playtesting habits carried over too: I kept trying the app as a user and changing whatever felt awkward, from cluttered notifications to controls that didn't read clearly. Building it with tests, code review, automated pipelines and cloud deployment showed me I can bring that game developer's focus on responsiveness and the user into the way corporate teams build software.<br><br>

---
<h3>Screenshots</h3>

{{< figure src="/images/flight-radar-widget.png" alt="Home-screen widget showing the nearest aircraft" caption="The Android widget" >}}