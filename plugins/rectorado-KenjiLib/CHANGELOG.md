## 0.7.1

* Updated **KDestroyAroundShip**

  * Now has a bool (active by default) for the deletion area to be active (to account for the new additions)
  * Added "Destroy Around Main Entrance" and "Destroy Around Fire exits" as options, if active it will destroy the gameobject in a radius around the ones active.
* Updated **KLightsEvent**

  * Added a call to activate the oldbirds.

## 0.7.0

* Added 3 new scripts: **KRunOnUpdate**, **KWeatherExtras** and **KHealingArea**
* Updated KHudMessaged: Now you can call "displaySlimeOnFace" to display the Gunkfish's goop on the screen for 10 seconds
* Cleaned the code a lil and tweaked some of the logging.
* Now a config will generate for you to select the level of  logging.

## 0.4.0

* Added 2 new scripts: **KHudMessages** and **KHelmetCondensation**

## 0.2.1

* Added a new stuff to **KLightsEvent**

  * Trigger JLL Appy Event: If true, it'll trigger any associated event(s) from the JLL Appy Event (JLL needs to be present for this to work)
  * If the permanent power off is already active (From a vanilla apparatus pull or this script) it'll skip the PermanentPowerOff or AppyEvent routines.
  * Now the AppyEvent should work like the vanilla apparatus pull (Wake up oldbirds/spawn extra enemies)

## 0.2.0

* Added a new script: **KLightsEvent**
* Updated scripts so they have tooltips explaining what it does, and some minimal logging.
* Updated **KDestroyAroundShip** to now include a useful wireframe gizmo to see what's the area.

## 0.1.0

* First Release

