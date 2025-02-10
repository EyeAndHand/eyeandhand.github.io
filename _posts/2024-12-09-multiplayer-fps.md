---
layout: post
---
# Mutliplayer FPS Project
![Image](/assets/images/multiplayer-fps-image.png)
## Details
**Project Status:** Work In Progress

**Project Type:** Personal

**Engine:** Godot 4

**Primary Role:** Programmer / Game Designer

---
A multiplayer First Person Shooter title currently in development focused on PvE and PvP combat, acrobatic level traversal, and hybrid melee/ranged combat. The project is inspired by Thief: The Dark Project (1999) and its compelling level traversal, as well as the un-official multiplayer patch made for its sequel.

Please note that all images are in no way representative of the end product.

## Multiplayer Networking
![Multiplayer Networking](/assets/images/multiplayer-fps-networking.png)
The project runs on a fairly basic peer-to-peer multiplayer structure, with a pre-game lobby system and basic chat functionality. Players send their inputs to a generic "Control Manager" object, which is then send to the host and synced with the other clients, decoupling the relationship of the player and their character controls in the event of large lag spikes or a network desync.

## Combat (PvP)
![PvP Combat](/assets/images/multiplayer-fps-pvp.png)
The initial inspiration for the combat came from titles like Chivalry: Medieval Warfare and Mordhau, both of which are known for exceptionally detailed melee combat. However, my experience in those titles has found them to have large issues when it comes to how player skill is expressed and how players meaningfully interact. The primary focus of combat in these titles is deception: feinting strikes, baiting early guards, and intentionally accelerating or decelerating your strikes to catch the opponent off guard. This inevitably leads to optimal strategies that are frustrating to deal with, especially in encounters with notable skill discrepencies.

By deliberately slowing down the combat speed, and moving away from reliance on deceptive combat tactics (feinting strikes, accelerated/decelerated strikes, etc.) it allows for a more intentional and reactive approach to combat with more focus on player spacing and the individual quirks of the weapons.

Ranged combat in the aforemention titles, however, has always been rather awful. Specifically, the melee player has little to no options when engaged by a ranged player other than running directly at the ranged opponent. To remedy this, the melee player is given more resilience to ranged attacks via armour, and has options such as shields and dodges that can negate a ranged attack. Thus allowing a melee attacker to more easily close the distance or retreat without the ranged attacker dealing excessive, unavoidable damage without removing ranged attacks as a threat.
