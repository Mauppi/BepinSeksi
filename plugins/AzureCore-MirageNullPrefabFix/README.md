# Mirage Null-Prefab Fix

A tiny **companion hotfix** for [qwbarch's Mirage](https://thunderstore.io/c/lethal-company/p/qwbarch/Mirage/) on Lethal Company v81. Install it alongside Mirage — it does not replace or modify Mirage.

## The bug
On v81, Mirage's `StartOfRound.Start` hook walks `NetworkManager.NetworkConfig.Prefabs` and calls `GetComponent<EnemyAI>()` on each prefab. Some content mods register malformed `NetworkPrefab` entries (duplicate/zero `GlobalObjectIdHash`) that leave a **null `Prefab`** in that list. Calling `GetComponent` on it throws a `NullReferenceException` that aborts the hook — which can leave you staring at a black void in orbit (camera never enables) with `soundmanager` log spam.

## The fix
This mod removes the null-`Prefab` entries from `NetworkConfig.Prefabs` in a `StartOfRound.Start` **prefix**. Mirage runs `orig.Invoke` before its own loop, so the prefix executes first and Mirage never sees a null. It only touches vanilla Netcode — it does not copy or modify any Mirage code.

## Temporary
This mirrors the guard in **Mirage PR #212** (https://github.com/qwbarch/mirage/pull/212). Once qwbarch merges it and releases upstream, this mod is no longer needed and will be **deprecated** — just uninstall it then.

All credit for Mirage goes to **qwbarch**. This is an independent, interoperating patch published with qwbarch's blessing.

— AzureCore
