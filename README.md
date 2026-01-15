<div align="center">

# Time Stop Clock

![forge](https://cdn.jsdelivr.net/npm/@intergrav/devins-badges@3/assets/cozy/supported/forge_vector.svg)
![fabric](https://cdn.jsdelivr.net/npm/@intergrav/devins-badges@3/assets/cozy/supported/fabric_vector.svg)
[![Available on Modrinth](https://cdn.jsdelivr.net/npm/@intergrav/devins-badges@3/assets/cozy/available/modrinth_vector.svg)](https://modrinth.com/mod/time-stop-clock-mod)
[![Available on Curseforge](https://cdn.jsdelivr.net/npm/@intergrav/devins-badges@3/assets/cozy/available/curseforge_vector.svg)](https://www.curseforge.com/minecraft/mc-mods/time-stop-clock-mod)

[![Modrinth](https://img.shields.io/modrinth/dt/time-stop-clock-mod?color=00AF5C&label=downloads&logo=modrinth)](https://modrinth.com/mod/time-stop-clock-mod)
[![CurseForge](https://cf.way2muchnoise.eu/full_690991_downloads.svg)](https://curseforge.com/minecraft/mc-mods/time-stop-clock-mod)

</div>

## Features:
Version 1.19.x has been removed, and this mod has been completely rewritten.

Migrate to [Cloth Config API](https://modrinth.com/mod/cloth-config) from Previous Config System.(V2.0.0+)
#### Items:
- Time Clock - Ability to time stop, slow down (0.5x) and speed up (2.0x)
- Arrow - Can shoot most projectiles. Hold Shift to view shootable items.
- Staff - No cooldown and no casting time (requires [Iron's Spells 'n Spellbooks](https://modrinth.com/mod/irons-spells-n-spellbooks), suitable for use during time stop).
#### Spells
- Time Freeze - Freezes the time of the current world for x seconds. The default duration is 6 seconds. The duration of [Iron's Spells 'n Spellbooks](https://modrinth.com/mod/irons-spells-n-spellbooks) increases with the level, and [Ars Nouveau](https://modrinth.com/mod/ars-nouveau) allow for free configuration.
- Time Box - When hitting a target, a Time Box is generated. Time inside the box is in a frozen state (this includes the ability to freeze only entities, blocks, and particles). When hitting a creature, a Time Box with a hitbox size of ×1.5 is generated; when hitting a block, a 5×5×5-sized Time Box is generated. The default duration is 6 seconds, and this is an exclusive spell of [Ars Nouveau](https://modrinth.com/mod/ars-nouveau).
#### Time Box
- Time inside the box is in a frozen state, and it can only freeze entities, blocks, liquids, and particles. Due to technical limitations, it can only be generated via commands or spells.
The Time Box can be reversed through the configuration file. After reversal, time outside the Time Box will be in a frozen state, while time inside the box remains normal.
#### Commands:
```
/timeclock tickrate <value> - Set the game tickrate
/timeclock pauseTime <true/false> - Set whether to enable time stop, can be used to forcibly enable or disable time stop
/timeclock whitelist list - View the whitelist
/timeclock whitelist list <true/false> - Same as above, but choose whether to output to the log
/timeclock whitelist clear  - Remove all entities in the whitelist
/timeclock whitelist remove <target> - Remove the target from the whitelist
/timeclock whitelist remove uuid <UUID> - Remove the UUID from the whitelist.
/timeclock whitelist add <target> - Add the target to the whitelist.
/timeclock config reload  - Reload the config (required after making modifications to the external config file).v2.0.0+ Removed.
/timeclock timebox add <id> <min> <max> <expandAfterCreation> <changeSpeed>
/timeclock timebox add <id> <min> <max> <expandAfterCreation> <changeSpeed> <color>
/timeclock timebox add <id> <min> <max> <expandAfterCreation> <changeSpeed> <color> <alpha>
/timeclock timebox add <id> <min> <max> <expandAfterCreation> <changeSpeed> <color> <alpha> <tick>
/timeclock timebox add <id> <min> <max> <expandAfterCreation> <changeSpeed> <color> <alpha> <tick> <removeAnimation>
/timeclock timebox add <id> <min> <max> <expandAfterCreation> <changeSpeed> <color> <alpha> <tick> <removeAnimation> <startCenter>
/timeclock timebox remove <id>
/timeclock timebox clear
/timeclock timebox list <logging>
/timeclock timebox modify <id>[<active/color/expandAfterCreation/changeSpeed>] <active/color/expandAfterCreation/speed>
/timeclock timebox modify <id> [<color>] <color> <alpha>
```

#### Key Bindings
- Left Ctrl + Mouse Wheel - Toggle time clock mode
- Right Ctrl - Open the tooltip overlay config screen

## Config:
#### General:
- bypassInvulnerableTime - Enable the desaturate shader to convert the game graphics into a black and white effect
- slotInteraction - Whether interaction with slots in the container is allowed
- model_size -The model size of WeaponProjectile (non-vanilla projectiles shot by arrow in this mod)
- cooldown - Cooldown tick using timeclock
- soundType - The sound played when using the time clock
- ability_tick - Ticks needed to recover back to normal after using time manipulation
- reverse_timebox - Whether to reverse the feature of the Time Box
- blacklist - Blacklist of "arrow" projectiles
#### Render:
- desaturate - Enable the desaturate shader to convert the game graphics into a black and white effect
- overlay_tooltip - Add overlay of tooltip for mod on the screen
- overlay_tooltip_position - Determines which corner of the screen the tooltip overlay will be rendered
- overlay_background - The background of the tooltip overlay
- overlay_background_color - The color of the overlay tooltip background
- overlay_tooltip_offsetX - The X-axis offset of the overlay tooltip
- overlay_tooltip_offsetY - The Y-axis offset of the overlay tooltip
- overlay_tooltip_color - The color of the overlay tooltip
- glowing_color - Glowing color of whitelisted entity
- timebox_face - Whether to render the time box faces
- timebox_line - Whether to render the time box lines
#### Screen:
 ![ ](https://media.forgecdn.net/attachments/722/829/2023-09-02_15.png)

 ![ ](https://media.forgecdn.net/attachments/721/466/2023-08-31_10.png)
## Issue Fix:
- [Blueprint](https://modrinth.com/mod/blueprint) conflict crash
- Server startup crash
- [Citadel](https://modrinth.com/mod/citadel) conflict
- Glowing effect not working.
- Tickrate changes in other dimensions are not syncing to the server.
- Geckolib animation is stuttering during timestop.
- "Arrow" are infinitely generating ammunition in survival mode.
- [Iron's Spells 'n Spellbooks](https://modrinth.com/mod/irons-spells-n-spellbooks) mod is failing to cast spells properly during timestop.(forge)
- [TaCZ](https://modrinth.com/mod/timeless-and-classics-zero) cannot fire during time freeze.
- Command blocks cannot execute the commands of this mod.
- Server startup conflict (Forge).

## Compatibility:
- ~~[Citadel](https://www.curseforge.com/minecraft/mc-mods/citadel) - Conflict with mixin~~ (Fixed in version 1.1.0)
