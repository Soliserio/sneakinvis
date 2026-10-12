SneakInvis
Author: Soliserio
A Windower addon that applies Sneak and Invisible using each character’s available spells, abilities, or consumables.
Installation
1. Extract the ZIP into your Windower folder, preserving this structure:Windower/
     addons/sneakinvis/sneakinvis.lua
     scripts/sneakinvis_all.txt
2. Install Windower’s Send addon to use the all-character script.
Use on all characters
Stand still and disengage, then enter in game chat:
//exec sneakinvis_all.txt
This loads the required addons and starts one buff pass on each connected character.
For an in-game macro, use:
/console exec sneakinvis_all.txt
Use on one character
//lua load sneakinvis
//sneakinvis start
Reload after updating
If the addon is already loaded, reload it before running the script again:
//send @all lua reload sneakinvis
For one character:
//lua reload sneakinvis
How it works
The addon checks these options in order:
1. Available, learned Sneak and Invisible spells, with sufficient MP and ready recasts.
2. Spectral Jig, if available and ready.
3. Silent Oil for Sneak and Prism Powder for Invisible.
Characters with both buffs already active are skipped. If only Sneak is active and Spectral Jig is selected, the addon removes Sneak first so Jig can apply both buffs.
Consumables already in Inventory are used first. Otherwise, the addon retrieves one from Mog Case, confirms the transfer, and uses it. Any unused borrowed item is returned to Mog Case when possible. Existing Inventory supplies are not moved back.
Stop or check status
Stop all characters:
//send @all sneakinvis stop
Stop the current character:
//sneakinvis stop
Check the current character:
//sneakinvis status
Notes and troubleshooting
- This is a one-shot command, not continuous rebuffing.
- Stand still and disengage before starting. Other automated actions may interfere.
- Leave a free Inventory slot when supplies must be retrieved from Mog Case.
- The addon does not change Trust, follow, or healing settings.
- An Incomplete message means the requested buffs were not confirmed. Check the accompanying reason before retrying.
- After zoning, logging out, or unloading during a transfer, check Inventory for any borrowed supplies.
