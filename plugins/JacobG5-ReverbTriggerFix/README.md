# Note for v80+: Mod many no longer be needed (sorta)
As of v80 part of this mod was added to the basegame. Reverb triggers are now set up with exclusion layers to prevent running checks every frame on environment colliders. Given this was one of the main performance improvements this mod provided I decided to touch up the formerly experimental feature for changing reverb trigger behavior from OnTriggerStay to OnTriggerEnter and make it enabled by default. This change may cause some issues with teleporting players or other edge cases. If you only want AudioReverbPreset caching, or you experience unforseen issues while running this, you can disable the behavioral changes in the config or disable the mod entirely as it is no longer as needed. The current implementation is a little dumb but it may help in certain situations. I would no longer consider this a must have mod.

## AudioReverbPresets
Whenever the game needs to reference AudioReverbPresets it does so by running `UnityEngine.Object.FindObjectOfType<AudioReverbPresets>()`

This is a problem because that method searches every gameobject in the loaded scene tree to locate objects with the AudioReverbPresets script. 

This mod replaces most of the calls for that method with a call to a different method that saves that object to memory and returns it if it still exists. The AudioReverbPresets object is part of a level's scene tree so when loading a new scene it should notice the reference is invalid and save the new AudioReverbPresets object for future use over the course of the round.
