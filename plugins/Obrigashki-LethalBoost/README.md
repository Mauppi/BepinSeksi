# LethalBoost

**Version 1.0.0**

A comprehensive performance optimization mod for Lethal Company that significantly improves FPS and reduces lag through intelligent LOD systems, AI throttling, and graphics optimizations.

## Features

### 🎮 AI Optimization
- **Enemy AI Throttling** - Reduces update frequency for distant enemies
- **Per-Enemy Customization** - Individual settings for each enemy type
- **NavMesh Optimization** - Reduces pathfinding quality for distant agents
- **Safe Defaults** - Critical enemies maintain full functionality

### 🌿 LOD Systems
- **Grass & Foliage** - Dynamic quality based on distance (4 levels)
- **Interior Props** - Culls decorative objects in dungeons
- **Rocks & Debris** - Aggressive culling of non-gameplay objects
- **Decals** - Disables distant surface details
- **Shadow Quality** - Dynamic shadow quality (3 levels)
- **Texture Quality** - Automatic mipmap adjustment
- **Reflection Probes** - Distance-based probe quality
- **Camera Culling** - Optional view distance limiting (disabled by default)

### 🎨 Graphics Optimization
- **Post-Processing LOD** - Dynamic quality based on FPS
- **Animation Culling** - Disables distant animations
- **Particle Optimization** - Reduces particle system load
- **Light Culling** - Disables lights in unoccupied rooms

### 🏠 Interior Optimization
- **Room Culling** - Hides distant rooms
- **Door Culling** - Culls behind closed doors (optional)
- **Physics Culling** - Disables physics in empty rooms (optional)

### ⚡ Trap Optimization
- **Turret Throttling** - Distance-based update rates
- **Landmine Throttling** - Reduces far landmine updates
- **Spike Trap Throttling** - Optimizes spike trap logic

## Configuration

Configuration file: `BepInEx/config/LethalBoost.cfg`

### Configuration Categories

1. **General** - Master switches and debug options
2. **AI Optimization** - Enemy throttling settings
3. **AI Enemies** - Per-enemy optimization toggles
4. **Items** - Item optimization settings
5. **Particles** - Particle system settings
6. **Rigidbody** - Physics optimization
7. **Physics Culling** - Room-based physics
8. **Interior Rooms** - Room culling settings
9. **Interior Doors** - Door culling settings
10. **LOD Systems** (11-19) - All LOD configurations
11. **Optimization** (20-21) - Animation and NavMesh
12. **Interior Lights** (22) - Light culling
13. **Traps** (23-25) - Trap optimizations

## Compatibility

### ✅ Compatible With
- MoreCompany
- LethalLib
- Most cosmetic mods
- Most item mods

### ⚠️ May Conflict With
- Other performance mods (disable overlapping features)
- Mods that heavily modify enemy AI
- Custom enemy mods (may need per-enemy configuration)

## Known Issues

- **Interior LOD** - May cause rendering issues in some custom maps (disable if you see white/purple cubes)

## Troubleshooting

### White/Purple Cubes Visible
- Disable `EnableInteriorLOD` in config
- This is caused by colliders being visible when renderers are disabled

### Enemies Not Moving Properly
- Disable `EnableAIOptimization` or specific enemy optimization
- Increase distance thresholds in config

### Low FPS in Grass
- Ensure `EnableGrassLOD` is enabled
- Lower `GrassDetailDistance` and `GrassCullDistance` values

### Objects Disappearing
- Increase LOD distances in config
- Disable specific LOD modules causing issues

## Debug Mode

Enable debug logging to see what's being optimized:
```
EnableDebugLogging = true
```

Check `BepInEx/LogOutput.log` for detailed information.

## Support

- **Discord**: https://discord.gg/pATupFuJ42