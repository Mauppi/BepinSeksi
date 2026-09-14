# KenjiLib

It's a lib. It has scripts that I made and use on my projects. Wesley made one of them actually, but I will take credit.

If you'd like to support me, check out my ko-fi. https://ko-fi.com/itiskenji.

---
## K Destroy Around Ship
If the gameobject is in the range set up in the script, it will destroy it.

## K Lights Event
Trigger different Light Events in the interiors at will, it includes:
- Flicker Lights
- Permanent Power Off: Flickers and then turns the lights off permanently, without the HUD warning.
- Appy Event: Mimic the Apparatus event (like Permanent Power Off, but with the HUD warning)
- Power Back On: Reverts the permanent power off from this script or an apparatus event, turning the lights on again.
You can call it on enable (selecting the event that you want to play) or calling the event directly.
- Trigger JLL Appy Event: If true, it'll trigger any associated event(s) from the JLL Appy Event (JLL needs to be present for this to work)

## K Hud Messages
Allow you to call certain messages to the HUD (These are client-sided, you'll need something like JClientSync if you want them to be displayed to everyone at the same time)
For now you can call 2 types of Hud Messages
 - Status Effect: Displays a message next to the HP and Stamina, like the one that appears when near a bursted valve. Stays for a few seconds.
 - Custom ship message: Displays a message similar to the ones that are sent when the ship is about to leave.
 - Extra: You can call the Gunkfish's goop on the screen for 10 seconds

(More types may be added in the future)

## K Helmet Condensation
When enabled, activates helmet condensation when looking up.

(More stuff is planned for this script)

## K Run on Update
When enable, any event set up will run every frame.

## K Weather Extras
Lets you mimic or activate certain vanilla weather behaviours:
- Eclipse-like weather event: Will mimic the eclipse behaviour of spawning extra enemies. The variables used can be selected or use custom ones.
- Flooded-like Weather object: Will mimic the flooded behaviour on a certain gameobject. The variables used can be selected or use custom ones.
- Stormy Lightnings: When enabled, will enable vanilla lightnings.

## K Healing Area
When active, will heal players within the specified distance.

## Credits:

**Kenji**: They call me mr robot now. <br><br>
**GenericGMD**: local manul <br><br>
**Wesley**: made the destroy script <br><br>
**Reiko88**: Lent me the base code for the healing script <br><br>
<a href="https://ko-fi.com/itiskenji"><img src="https://storage.ko-fi.com/cdn/brandasset/v2/support_me_on_kofi_dark.png" alt="Ko-Fi" width="200"/></a>
<br>