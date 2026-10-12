## SneakInvis v1.0.4
Author: Soliserio

Applies missing Sneak and Invisible buffs with one command, on one character or all your logged-in characters.

### New in this release
- Silent Oil, Prism Powder, and Ninja tools can now be pulled from Mog Satchel, Mog Sack, and Mog Case.
- Uses supplies in Inventory first.
- Confirms withdrawals before using supplies.
- Returns unused borrowed supplies to their original bag.
- Confirmed working in game on all characters; 41 offline tests passed.

### Installation
Extract the ZIP and copy its addons and scripts folders into your Windower folder, merging the folders.

### Commands — enter in game chat

Load on all characters:
//send @all lua load sneakinvis

After updating, reload on all characters:
//send @all lua reload sneakinvis

Run on all characters:
//exec sneakinvis_all.txt

Run on the current character:
//sneakinvis start

Check the current character:
//sneakinvis status

Stop the current character:
//sneakinvis stop

Stop all characters:
//send @all sneakinvis stop

In-game macro line:
/console exec sneakinvis_all.txt

### How it works
1. Uses available Sneak and Invisible spells.
2. Falls back to Spectral Jig.
3. Tries Ninja spells: Monomi and Tonko.
4. Uses Silent Oil and Prism Powder as the final fallback.

Ninja spell checks include learned spells, job level, recast, and tools. Universal Ninja tools require Ninja as the main job.

Already-active buffs are skipped. If only Sneak is active and Spectral Jig is selected, Sneak may be replaced so Jig can apply both buffs.

### Important notes
- Stand still and disengage before running.
- All-character commands require Windower Send and SneakInvis loaded on each client.
- This is a one-shot command, not continuous rebuffing.
- Leave one Inventory slot free for withdrawals.
- Do not manually move supplies during a run.
- If a transfer times out, check Inventory and the source bag before retrying.
- Consumed supplies cannot be returned.
- Trust, follow, and HealBot settings are not changed.
