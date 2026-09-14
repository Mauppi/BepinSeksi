## v0.4.0
- Removed exclusion layer override patches (as of v80 they have been made base game)
- OnTriggerEnter has been reworked to no longer disable the original component (and as such preventing coroutine execution)
- OnTriggerEnter has been made the default and the experimental config has been removed. (still will disable if you check the disable mod config)
- Refactored much of the code.
- Updated README.

## v0.3.1
- Recomp v81
- Method replacements now copy labels

## v0.3.0
- Increased stability for the Experimental OnTriggerEnter mode.
- Updated README.

## v0.2.0
- Added several transpiler patches to replace several calls to `UnityEngine.Object.FindObjectOfType<AudioReverbPresets>()` with a cached refrence.
- Updated README.

## v0.1.0 Release 
- Experimental release.