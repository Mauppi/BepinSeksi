# Changelog

## 1.0.2
- Release build. Same fix as validated, with quiet logging (only logs when it removes an entry).

## 1.0.1 / 1.0.0 (dev)
- Iterated on the hook target. Root cause: a null-`Prefab` entry is registered during vanilla `StartOfRound.Awake`, which Mirage's post-`orig` enemy-registration loop then trips on. Fixed by sanitizing null-`Prefab` entries in a prefix **and postfix** on `StartOfRound.Awake` (and `Start`, for future/PR builds). The Awake postfix is the one that catches it.
