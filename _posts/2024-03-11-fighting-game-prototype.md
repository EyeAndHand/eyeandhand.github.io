---
layout: post
---
# Fighting Game Prototype
![Image](/assets/images/fighting-game-prototype.png)
## Details
**Project Status:** Work In Progress

**Project Type:** Personal

**Engine:** Godot 4

**Primary Role:** Programmer

---
An experiment of mine to build a modular and versatile system to create 2D fighting game characters with virtually any kind of associated mechanics systems. Made in Godot, primarily for its extremely easy plug and play multiplayer networking and its object-oriented focus. Most inspiration for the project comes from M.U.G.E.N. as well as my interest in the Capcom fighting game for JoJo's Bizarre Adventure from the late 90s.

Much groundwork still needs to be laid down for the systems, but in its current state a designer can easily create movesets for characters by typing out simple strings that are intepreted at runtime into arrays of inputs. Each player character can have a completely arbitrary set of "resources" (health, super-meter, etc.) and may have their own specialized UI displayed, as determined inside the character logic.
## System Example: Attack Logic
![Image](/assets/images/fighting-game-prototype-signal.png)
To properly decouple the character systems from any dependencies, one of the most important parts is to handle all "incoming" effects (such as getting hit by an attack) on the receiving end. When a character hitbox collides with an opposing hurtbox the attacking character sends out a signal with two arrays attached, a "value" array and a "dictionary" array. The character that was hit by the attack then receives the signal, and checks through the dictionary array for any names that it is sensitive to and then passes their associated values into the character logic.