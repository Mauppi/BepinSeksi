# Lethal-Bots
A Lethal Company Mod that adds bot players to the game. Based off of the code of the mod Lethal Internship.<br/>
Everyone must have the mod in order for it to work!<br/>
For multiplayer, install the same complete package version on the host and every client (DLL plus both asset bundles); do not mix locally rebuilt and Thunderstore DLLs carrying the same old version number. Version 12.1.4 logs the Netcode fingerprint plus Steam relay connection/end state on both peers and shows a useful stage-specific reason instead of the game's blank rejection.<br/>

I also have a discord server as well for any questions or support: https://discord.gg/TVqJst8yHf

> [!NOTE]
> Its recommended that you install the [LethalBots NavMesh Project](https://thunderstore.io/c/lethal-company/p/TRizzle/LethalBotsNavMeshProject/) which has a ton of NavMesh Improvements and fixes for the bots!

## Preamble:<br/>

Playing solo in Lethal Company is hard, as the game is inherently designed around a team of 4 players.<br/><br/>
Now, there are certain mechanics that automatically adjust for single player, but you still run into multiple disadvantages.<br/><br/>
Loosing all your scrap if you die, enemies like the butler and coil head really screwing you over, turrets, landmines, big doors, and many other issues that are a lot easier to deal with multiple players.<br/><br/>
After I discovered the mod Lethal Interns, it inspired me in a way. I realized I could use my previous modding experience with player bots and use it to finally create player-like bots for Lethal Company.<br/><br/>
And that is how this mod came to be, and you would not believe how long it took me to get here. There are many older version of this mod, lost to time.<br/><br/>
In the end, while they may never be as smart as a real player, its still better than playing alone. <br/><br/>
Oh, and before I forget, this mod is 100% MULTIPLAYER friendly, so feel free to add them to assist your Duo or Trio.

</br>![bots_example](https://github.com/T-Rizzle12/Lethal-Bots/blob/master/Assets/Images/bots_example.png?raw=true)</br>

## Bots and how they spawn

These passionate workers spawn in after you start landing on a moon.
The number of ~~bots that spawn~~ players that join depend on how many player slots are available and the maximum number of ~~bots~~ players set in the config<br/>
<br/>**They return to the ship**
<br/>If they lose the player they are following and it starts getting late out,
<br/>they will automatically return to the ship.
<br/>
<br/>**They always follow you unless told otherwise**
<br/>Or at least try to follow you, or another player.
<br/>The moons are not very welcoming and your ~~bots~~ new co-workers may have (some) difficulties to navigate smoothly in those tricky areas due to how the navmesh is made.
<br/>
<br/>**They can loot on their own**
<br/>You are able to command your ~~Bots~~ new co-workers to enter the facility and they will search for scrap and will only return to the ship when full or after a while!
<br/>
<br/>**They continue the round after you die**
<br/>In the event of your demise, ~~bots~~ your new co-workers are capable of continuing to collect scrap without you,
<br/>You can vote to leave early which will tell ~~bots~~ your new co-workers to return to the ship
<br/>They will automatically return to the ship if not following a player after the sun sets
<br/>
<br/>

## How to use the mod
- Bots will take up player slots that are open, if you have a full server this addon won't do anything.
- Bots will join you in orbit, you can kick them from the lobby if you want to make room for friends! </br>
- Bots automatically revive after returning to orbit. </br>
- You can revive bots and bots can revive you with other mods like 'Revive company', 'Bunkbed revives' and 'Zaprillator'</br>
- Bots can sell scrap at the company. You can configure if they sell everything, or only to quota </br>

While they are spawned, while looking at them: </br>
- You can command them to follow you with as well as tell them to loot on their own with [E]</br>
- Make them drop their held item with [G], they will automatically swap to the next item in their inventory</br>
- Change the suit of the bot by the one you're wearing with \[X]</br>
- All input are configurable.</br>

## Configuration files
Lots of settings for the bot's AI can be configured, so go check them !</br>
Mod is compatible with InputUtils so you can change your inputs !</br>
There's also a config file for the identities of the bots (a name, preferred suit, a voice)</br>
![folder_config](https://github.com/T-Rizzle12/Lethal-Bots/blob/master/Assets/Images/folder_configs.png?raw=true)</br>
All config files can be found at Your_profile_folder\BepInEx\config\LethalBots\ </br>
If you want to make your own custom loadouts file, rename 'ConfigLoadoutsDefault.json' to 'ConfigLoadoutsUser.json' and the default one will be ignored. Details can be found in the default json.</br>
![folder_config](https://github.com/T-Rizzle12/Lethal-Bots/blob/master/Assets/Images/folder_config_user.png?raw=true)</br>
To link the voice folder to the bot, simply change the "VoiceFolder" property in the identity you want.

## Fully voiced bots
T-Rizzle: I may change the voice lines along with using TTS in the future, but since the original mod was under an MIT license, I will keep the original voice lines for now.
</br>A big thanks to **Mathew Kelly** and his incredible voice acting, there's more than 700 (!!) voice lines for those little guys.</br>
Chilling with you, following, founding loot, panicking, you name it, there's a voice line for every state of mind !</br>
You may know him as **Dragon-V0942** from [FurAffinity](https://www.furaffinity.net/user/dragon-v0942), and you can find some of his voice acting works on YouTube [(Voice acting example)](https://youtu.be/SZDDcCBvyjc).
</br>
</br>

## Have fun with cosmetic mods !
This mod is compatible with ModelReplacementAPI and all of its users (tooManySuits, MoreSuits, ThiccCompany, etc...).
It is also compatible with the emotes mod, emote in front of bot and they will copy your dance moves !

</br>![Lethal-Bots-Suits](https://github.com/T-Rizzle12/Lethal-Bots/blob/master/Assets/Images/bot_suits.gif?raw=true)</br>

## Chat and Voice commands!
The bots have a few chat and voice commands that you can use to tell them to do certain things.
Please note that these commands are not case sensitive, so you can use any combination of upper and lower case letters.
Also, the bot only checks for the keywords anywhere in the message, for example, you can use "Jester is going to pop!" and the bot will still respond to it.
</br>**jester** - The bot will check to see if there is an active jester, if there is, they will try to escape the facility immediately.
</br>**start the ship** - The bot will check if the host sent the command or if the host is dead, if so, the bot will start the ship.
</br>**hop off the terminal** - The bot currently on the terminal will hop off for a few seconds, allowing you to use it.
</br>**request monitoring** - The bot who is currently on the terminal will monitor you rather than cycling through the players.
</br>**request teleport** - The bot who is currently on the terminal will teleport you back to the ship.
</br>**clear monitoring** - The bot who is currently on the terminal will stop monitoring you and return to the default behavior of cycling through players.
</br>**man the ship** - Makes the bot you are looking at go to the ship terminal and start manning it.
</br>**transmit (desired message)** - The bot who is currently on the terminal will send the given message on the signal translator.
</br>**transfer loot** - The bot will cycle between facility entrances and transfer any loot they find to the ship.
</br>**gear up** - Bots that are following the player will automatically swap to the GrabLoadoutState and grab their set loadout.
</br>**create group** - This creates a new group with you as the leader!
</br>**leave group** - This causes you to leave the current group you are in.
</br>**join group** - This lets you join a group. You must look at the bot of the group you want to join.
</br>**use key** - This tells every bot that is following you to unlock the door you are looking at. NOTE: You must be standing within use range for this to work!
</br>**route (desired message)** - The bot who is currently on the terminal will attempt to route to the given moon using the terminal. (WARNING: Be careful about using this as the bot may end up routing to the wrong moon!)
</br>**wait here** - The bot will stay and hold their current position until either, it gets late out or you tell them to follow you again.
</br>**follow me** - The bot will move to follow you
</br>**lead the way** - The bot will go to search for scrap on its own
</br>**change suit** - The bot will change its suit to the suit you are wearing
</br>**drop your held item** - The bot will drop its held item. If the bot is not holding anything, it will swap to the next item in its inventory.
</br>Please note that you must be in chat range for the bot to hear you. If you are too far away, the bot will not respond to your command.
If both you and the bot have a walkie-talkie, you can use the command in the chat and the bot will respond to it.
</br>Please note that these are also voice commands, but they require you to only say the word unlike how they work as said in the chat.

Note: The bot will also respond to commands on the signal translator, but there is a separate list of commands for that.
</br>**return** - The bot will return to the ship immediately.
</br>**jester** - The bot will check to see if there is an active jester, if there is, they will try to escape the facility immediately.

### Global Chat Commands
These chat commands are global meaning bots will always respond to these commands even if they can't normally hear you.
Please note that these commands are not case sensitive, so you can use any combination of upper and lower case letters.
</br>**I will man the ship** - If you say this command, you will be marked as the Mission Controller. The previous Bot that was set as Mission Controller will hand the terminal to you. No other bots will be allowed to automatically assume the Mission Control role unless one of the following things happen:
1. You die
2. The day ends

**I will transfer loot** - This tells bots that you will be transferring loot! NOTE: All it does is add you to the LootTransferPlayers list. This causes the drop loot outside of entrances code to run!
</br>**!lb addbots** (legacy alias: **/addbots**) - This tells my mod to spawn bots on the ship. This command only works while the ship is in orbit and you must have **Allow bots in orbit** set to true. (YOU MUST HAVE NavmeshInCompany AS WELL!)
</br>**!lb blacklistitem (optional: all)** - This tells my mod to add the current item you are holding to the sell blacklist. Bots will refuse to sell the held item in particular. This ONLY applies to the HELD ITEM, unless you include all, you must do this for EACH ITEM!
</br>**!lb unblacklistitem (optional: all)** - This tells my mod to remove the current item you are holding from the sell blacklist. Bots will be allowed to sell the held item in particular. This ONLY applies to the HELD ITEM, unless you include all, you must do this for EACH ITEM!

### Integrated generative dialogue and speech

This integrated build preserves the optional, host-authoritative AI dialogue features. They are disabled by default, so the normal recorded voices and command handling remain available without an LLM or speech server.

- Generated dialogue supports LM Studio, llama.cpp, and other OpenAI-compatible chat endpoints. **Enable generated dialogue tool calling** is the host-side master switch; **Enable generated dialogue soundboard tool** controls audio-clip access; **Enable autonomous generated tools** separately controls the bounded ambient-autonomy set, while **Enable generated minor sabotage** and **Enable generated malicious actions** separately control the two personality-gated mischief lanes. Turning off the master switch disables all generated tools.
- llama.cpp requests keep model reasoning enabled unless **Generated dialogue reasoning effort** is `none`. Hidden reasoning receives a separate, trigger-bounded real-time allowance, and **Generated dialogue max tokens** remains available to the visible JSON reply instead of being consumed entirely by thinking. A configured reasoning ceiling above the real-time cap is intentionally reduced for live speech. **Generated dialogue maximum spoken words** separately controls the final ordinary spoken-line ceiling (48 by default, configurable from 12 to 72); prompts require complete sentences, and exceptional overlong output is reduced at a late sentence boundary or whole word instead of being blindly sliced at the old 110-character/18-word cutoff. Sudden danger reactions keep their intentionally short reflex limit.
- Player-directed actions require a clearly named primary bot, an unquoted/non-negated command, and one unambiguous action target. The target must occur in the imperative target span; duplicate display names, incidental secondary player names, action/enemy-name collisions, multiple live purchase offers, and model arguments that differ from the canonical target are refused. `me`/`speaker` resolves through the authenticated client ID rather than a display name. The normal autonomous tool lane cannot target players; only the separately configurable, personality-gated malicious lane can do so.
- The direct tool catalog covers grounded movement/grouping, bounded combat or retreat, Jester handling, normal loadouts, explicit self-defense preparation from real ship stock, dropship work, exact item and upgrade purchases, keys, holding/searching/selling/healing/charging/equipping, inverse teleporter and horn use, ship start/return/terminal duty, monitoring/teleport/rescue, signal messages, loot transfer, soundboard playback, independence, and a dead-only leave vote. The ambient autonomous gameplay allowlist is narrower and only offers actions that pass live feasibility checks, including risk-justified self-defense, practical mission work, bounded economy actions, and the optional mischief lanes. The expressive soundboard is independently eligible on supported dialogue triggers and uses its own short cooldowns instead of consuming the general autonomous-action cooldown.
- Terminal purchases are host-authoritative, serialized behind human terminal use, capped to a six-request queue, and revalidated against live credits, catalog availability, dropship capacity, and round state before each terminal step. Temporary mission-control and network ownership are restored after the purchase batch.
- Autonomous shopping preserves **Bot restock spending limit**, rate-limits economy actions, favors practical missing supplies, strongly de-prioritizes duplicate Weed killer, and only considers ship upgrades with a known utility score of at least 50. A directly addressed host/captain purchase may spend below the configured restock reserve when actual credits cover it; autonomous and non-host requests may not.
- Minor sabotage defaults on only because it was explicitly requested for this build, but remains independently disableable. It is limited to one action per round, shares the 120-second autonomous economy cooldown, refuses emergencies/threats/departure, never targets players, and can only ring the horn safely, abandon terminal duty, or buy one non-Weed-killer item costing at most 30 credits without touching the reserve.
- Malicious autonomy is independently disableable and limited to one personality-gated action per round with a 240-second global cooldown. It is suppressed during crew emergencies or nearby monster threats. The live action enum exposes only presently valid choices: hoard one free ship weapon, attack or kill one nearby reachable named player, or start a late departure while living crew remain outside. Every choice is owner-revalidated immediately before state mutation; arbitrary global victims and early-round departures are rejected.
- Generated speech supports ElevenLabs, local Qwen3-TTS, local Chatterbox, and Windows SAPI. Per-bot overrides are configured in `ConfigVoiceProfiles.json`.
- Put soundboard files directly in `BepInEx/config/LethalBots/Soundboard/` on the host. Up to 128 non-empty `.wav`, `.ogg`, or `.mp3` files of at most 12 MiB each are exposed to the LLM in a newly shuffled order for every eligible request. The tool and both prompt layers identify this as a live expressive capability and encourage frequent context-appropriate use during casual human replies, ambient silence, bot spawns, and ordinary game events—even when nobody explicitly asks. You can still request a random clip (for example, “Slop, play a random sound”) or name a filename/stem (for example, “Slop, play airhorn” for `airhorn.wav`). The selected bytes are validated and broadcast from the host through that bot's positional voice, so clients do not need matching files; the clip replaces spoken acknowledgement. Clear gameplay orders and urgent warnings retain priority, while short global/per-bot soundboard cooldowns prevent consecutive spam without consuming the longer autonomous gameplay-tool cooldown. Soundboard actions bypass per-client Talkativeness/Responsiveness frequency mutes so an accepted tool call reaches the whole lobby, but the synchronized **Enable generated bot speech** master setting must remain enabled.
- Player speech can use the existing SpeechRecognitionAPI commands or optional host-side faster-whisper transcription. With host faster-whisper enabled, each non-host client that enables **Enable bot Voice Recognition (Client only)** captures and forwards only its own microphone segments; the host authenticates the sender and bounds the captured walkie/position context before deciding which bots heard it. Active bot names and aliases are prioritized as transcription hotwords, and ambiguous fuzzy name matches are refused. State-changing LLM tools still require the bot name to appear explicitly in the accepted transcript. Accepted language metadata stays attached to that exact utterance so `chatterbox-local` profiles using `chatterboxLanguage: "auto"` select the matching multilingual TTS language without leaking another player's or a rejected clip's language into a queued reply.
- Accepted human voice/chat replies take the host's LLM/TTS lane ahead of scripted, bot-to-bot, event, and ambient work. Direct addresses are response-required end to end: a newer direct turn supersedes an older incidental request for that bot, stale lower-priority preparation is cancelled, the model is not allowed to silently convert the turn into memory, and a safe spoken fallback is used if generation is empty or malformed. One required reply may wait behind speech already audible from that bot; urgent danger still has the highest priority.
- Talkativeness/Responsiveness and the generated reply, scripted-speech, ambient, dead-bot, silence, and cooldown settings are enforced both when dialogue is queued and immediately before playback. Ambient silence/cooldown values are hard minimums measured from real crew speech and completed playback.
- Ambient dialogue can include randomized, context-aware self-talk after a bot has remained genuinely isolated. Self-talk uses local silence, respects Talkativeness and the global ambient cooldown, cannot call gameplay tools, is not mirrored globally to chat, and is cancelled if someone comes within hearing range before playback.
- Nearby bots can start a partner-targeted conversation from their current location, activity, health, or held items. These exchanges choose one listener, stay on the same thread, and end naturally after two or three turns instead of recursively involving the whole crew.
- Verified player hits and direct verbal threats are routed to the bot's current network owner. Armed bots use bounded self-defense policies; unarmed bots retreat and keep their distance instead of immediately following the aggressor again. Serious danger reactions preempt stale speech, while at most two different bots may overlap urgent generated reactions.
- The host stores generated-dialogue history in hashed, per-save JSON sidecars under `BepInEx/config/<plugin GUID>/DialogueMemory/`. This history can include bot memories, generated lines, and recent player chat or voice transcript text heard by bots. Challenge saves are excluded; deleting a save slot or resetting identities removes its sidecar. Set **Generated dialogue memory entries** to `0` to disable retained dialogue history and remove the selected slot's existing history when it initializes.
- The repository includes the local Qwen3/Chatterbox/faster-whisper helper under `Tools/Qwen3LocalTtsServer`.

## How the bots work
The bots take one of the player objects in the game and I attach an EnemyAI to it for the pathfinding code.
</br>As a result, the game considers the bots as a human player for most intents and purposes, although there are some hacks added since the game runs most of its player logic on the client/local player only.
</br>The bot uses states to run its AI with certain conditions that determine when the bot changes its states.

### Adaptive self-defense loadouts

When **Adaptive self-defense loadouts** is enabled, an unarmed bot still aboard during deployment evaluates the selected moon's listed risk, combined enemy power budget, facility size, weather, quota cycle, and current quota pressure. If that deterministic score reaches **Adaptive self-defense risk threshold** (default `0.58`), the owning client sends the bot through its normal loadout/fetch states to take one usable weapon already on the ship. It never creates or buys gear, avoids conductive weapons during storms, skips weapons another bot is already fetching, and prefers stronger weapons only when the assessed risk warrants them. A clearly addressed `arm yourself`, `get a weapon`, or `prepare for combat` request can invoke the same grounded behavior directly.

### Crew participation and ship doors

With **Require every bot to make a scrap run** enabled, each available bot must physically move beyond the ship perimeter or enter the facility for at least one field run per expedition. Merely entering the search state does not count. An explicit follow order from chat, voice, direct player input, or the grounded LLM `follow_player` tool remains in follow mode instead of being replaced by autonomous scrap search; sustained physical deployment with that leader counts as the bot's run. Automatic mission-control duty is deferred until that bot has deployed, assignments are claimed atomically, and staggered retries continue if a route or loadout sends it back. Other explicit directed work and active emergencies remain higher priority; Eclipse and an already-closed safe departure window waive the obligation, while a hard moon calls for defensive equipment instead of permanent ship idling.

With **Require every bot to help sell at the Company** enabled, idle/following bots and the mission controller join the existing collect-and-sell states whenever unclaimed sellable work exists. Explicit terminal purchases are allowed to finish first, item claims are shared so bots spread across available scrap, and the normal quota/**Sell all scrap on ship** rules still decide when selling is complete. This requires the supported Company NavMesh dependency.

With **Allow bots to close the ship doors** enabled, the host selects one living bot physically inside the ship to operate the doors; that bot does not need to be the mission controller. An open door may close for an enemy the bot threat system classifies as immediately dangerous near or inside the ship, even while some crew are still out, or after the configured return time once every living crew body is safely behind the inner ship boundary. A returning living crew member on the surface within 12 metres of the entrance blocks a close and causes a closed door to reopen, with urgent returners overriding the short manual-input grace. Normal button, animation, power, and overheat restrictions are honored, an automatic reopen is held long enough to cross the threshold, and manual player door input receives a five-second grace period so bots do not fight the controls.

### Navigation and hazard recovery

The bot owner now treats a destination as a logical goal instead of repeatedly committing to one shortest route. If the direct corridor is blocked or dangerous, the bot checks a bounded set of lateral, fan-shaped, and map AI-node waypoints. A detour is accepted only when both the bot-to-waypoint leg and the waypoint-to-goal leg are complete, then candidates are ranked by danger, path length, forward progress, and NavMesh clearance.

Navigation recovery measures the physical player body's progress, not only the detached NavMeshAgent. A stalled bot retries from another side of the obstacle and temporarily rejects a failed waypoint. Ladders, moving elevators, OffMeshLinks, vehicles, Tulip Snake or other enemy carries, moving physics parents, and ship landing/take-off sequences intentionally suspend NavMesh recovery while they own the physical body. A mineshaft bot retains its intended floor while the cage moves, retries the networked inside control after the normal boarding delay, and resumes at the current-floor exit even when the cage itself has no baked NavMesh. Stationary elevator physics parents no longer suppress AI or ordinary stuck recovery. The bot may reattach only its invisible owner-side navigation agent to the unchanged body. When every route fails—including while returning to the ship—it walks toward a reachable recovery node, retries its logical goal, or waits in place; navigation failure never teleports the visible bot back aboard. Follow catch-up assistance is also blocked from crossing into the ship. Actual entrance, ladder, elevator, purchased-teleporter, spawn, and ship-departure transitions keep their normal game behavior.

Environmental danger is part of route selection. Bee avoidance is centered on the hive and its defense radius rather than only the moving swarm, except when a bot is deliberately handling that hive. Safe routes are always preferred. After repeated failures, a bot may accept the lowest-risk survivable exposure and sprint through it. Marked landmine areas, off-NavMesh samples, entering live slime, active lethal traps, exposed turrets, projected drowning, and excessive sinking remain vetoes; a bot already caught in danger may sprint only along a route that moves outward and passes the detailed survival checks.

</br>BrainDead:
</br>The Brain Dead state is when the bot dies in some way shape or form. In this state the bot can vote to make the ship leave early.
</br>There are two conditions in which the bot will vote to leave early.
1. All human players are dead and its late outside
2. The ship becomes compromised, aka an enemy is on the ship

NOTE: All players, "humans and bots," must be on the ship before the bot will vote!

</br>SearchingForPlayer
</br>If the bot loses the human player they were following,
</br>they will wander around looking for a human player before searching for scrap on their own.

</br>GetCloseToPlayer
</br>The bot moves closer to the player they are following, they check horizontal and vertical distances when checking if they are close enough.

</br>JustLostPlayer
</br>The bot just lost sight of the player they were following, they will check the last position they saw you at.
</br>If your last known position is near an entrance, the bot will use it!

</br>ChillWithPlayer
</br>The bot is waiting nearby the player they are following. They will mimic emotes the player is using.
</br>If they have any loot in their inventory and they are on the ship, they will drop it off!

</br>FetchingObject
</br>The bot is moving to pickup an object. If they are holding a two handed item, they will set it down to pick up the object.

</br>PlayerInCruiser
</br>The bot will hop into the back of the cruiser the player they are following is in and ride!

</br>Panic
</br>The bot will flee from a nearby enemy. If the bot is near an entrance, it will use it to escape!
</br>NOTE: If the bot escapes the enemy, has scrap, and is not following a player. They will return to drop off scrap early!
</br>If the bot has a weapon and they believe the enemy can be killed, they will swap to the FightEnemyState

</br>ReturnToShip
</br>The bot will leave the facility and return to the ship.

</br>ChillAtShip
</br>The bot is at the ship and will empty their inventory. They will perform a random emote.
</br>If there is no nearby human player and it's not late out, the bot will go back into the facility and look for more loot after a bit!
</br>The bot will start the ship if all human players are dead, all players are on the ship, and one of the following conditions are true:
1. It's late out
2. All human players voted to leave early
3. The ship becomes compromised

</br>SearchingForScrap
</br>The bot is searching the facility for scrap. If one of the following conditions are true, the bot will return to the ship:
1. The bot has at least one piece of scrap and hasn't found any other scrap recently
2. The bot's inventory is full
3. It's late out
4. All human players voted to leave early

</br>UseInverseTeleport
</br>If the inverse teleporter is active and the bot is on the ship, the bots will move to be teleported by it.
</br>It doesn't matter if the bot successfully teleported or not, they will switch to the SearchingForScrap state after, regardless!

</br>UseKeyOnLockedDoor
</br>The bot will attempt to use a key they have in their inventory on a locked door.
</br>The bot picks the closest side of the door
</br>If both sides of the door are accessible, they will only open it if there is a distance greater than 10 m between the two sides!

</br>MissionControl
</br>The bot will use the ship terminal and monitor the ship's crew while executing commands on the terminal as well as teleporting players as needed.
</br>Here is what the bot can do while on the terminal!
- Use commands to open heavy doors, turn off turrets, disable landmines, and disable ceiling traps
- Open heavy doors for the player they are currently monitoring
- Teleport bodies of dead players
- Teleport players who they considered in grave danger
- Use the signal translator to send messages to the crew about enemies and the current time
- Use the walkie-talkie to keep players' sanity up and receive chat messages from the crew

</br>TransferLoot
</br>The bot will transfer loot from the facility entrances to the ship

</br>CollectScrapToSell
</br>The bot will collect scrap on the ship with the intent of selling it. There are a few items the bots will refuse to sell:
1. Zed Dogs
</br>Please note that this does affect any item that inherits from the following classes!
1. Gift Boxes
2. Shotguns
3. Knives
4. Shovels

</br>SellScrap
</br>The bot goes over to the company desk to sell, ringing the bell and waiting if the desk is out of space.

</br>ChargeHeldItem
</br>The bot will charge its held item using the charging coil
</br>This is called when the bot is in the mission control state, and after returning to the ship

</br>FightEnemy
</br>The bot will fight its current targeted enemy
</br>The bot will pick the shotgun for most enemies, except for snare fleas, where they prefer the shovel or knife!
</br>Here are enemies the bot will always fight as long as they have a weapon
1. Snare Fleas
2. Masked
3. Thumpers
4. Hoarding Bugs
</br>Here are the enemies the bot will fight if they have a shotgun
1. Nutcrackers
2. Brackens
3. Bunker Spiders
4. Baboon Hawks (Only when in close proximity)

</br>UseTZPInhalant
</br>The bot will use the TZPInhalant in its inventory to get a speed boost!
</br>The return to ship state calls this when the bot is carrying heavy loot!

</br>LostInFacility
</br>The bot is lost in the facility and will try to find a way out.
</br>They will wander around the facility, calling out for help.

</br>HealPlayer
</br>The bot has chosen to heal a player.
</br>Bots can "heal" players using weed killer.
</br>Bots also support healing using Usual Scrap healing items.

## On a more serious note
This mod is very alpha and I still need some polishing.
<br/>I'm just happy to share this project with you, in hope that you find it fun and enjoyable.
<br/>T-Rizzle: I have made multiple changes to this from the original addon. While Lethal Interns intend to have the, well you know, interns assist the player, I found it not to my liking, but I saw the potential it had in general.<br/> 
These bots are to be more player like and this includes advantages such as counting as real players and the downsides like limited stamina.
- Although they will never be the same a players, they are great for small groups or playing with weak or no internet.
- Or you could go crazy and use MoreCompany and run around with an army of them.
- I recommend about 23 to 31 of them. After that it really starts to get laggy and there is only so much I can do to optimize them.

## Credits
- [**Szumi57**](https://github.com/Szumi57) - Original idea and coding of the original mod, Lethal Internship.
- [**T-Rizzle**](https://github.com/T-Rizzle12) - Major code refactor, bug fixes, and new features.
- [**Gummar**](https://github.com/Gummar) - Created the new search algorithm for the bots.
- [**PixelIndieDev**](https://github.com/PixelIndieDev) - Improved bot voice code and voice command system.
- **Mathew Kelly** - Voice acting for the bots, over 700 voice lines!

## Sponsors
A special thanks to everyone who dontated to Lethal Bots!
- Xander & Yalnif

## Things to add
- More Orders, currently you can tell them to loot and follow you. There are a decent amount of chat commands at least?
- ~~Add voice recognition and TTS so bots can understand and speak to players.~~ Done in this integrated build with optional SpeechRecognitionAPI/faster-whisper input and configurable generated speech.

## Bugs to fix
- The game will lag during the inital landing sequence after the bots spawn. I have no idea what causes this, but it fixes itself after the ship lands. This only seems to happen with about 21 or more bots. If you play with the default lobby size of 4 players, you won't see this issue. (DEVUPATE: Found out it might have something to do with collision, have a few ideas on how to alleviate it!)
- Sand spider web trap not working for bots. Transpiler or Postfix should work, just need to find out what would be the best option.
- Snare Fleas ignore bots that walk under them. The cause is that they only check for the Local Client walks under them, a transpiler or postfix can fix this!
- Compatibility with modded maps, for environmental hazards damages. The cause is due to most of the player code only running on the local player, I think I can get some kill triggers to work using transpilers/postfixes.
- Bots can hear you speak if you have push to talk set. The cause of this is how PySpeech works, since it runs a separate application that listens to your microphone. I may be able to fix this......
