# Changelog

All notable changes to LethalBoost will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2024-12-XX

### 🎉 Initial Release

#### Added - Core Systems
- **AI Optimization Module** - Distance-based enemy AI throttling
- **Modular Architecture** - Clean, maintainable codebase with error handling
- **Comprehensive Configuration** - 25+ configuration categories with 100+ settings
- **Debug Logging System** - Detailed performance monitoring and troubleshooting

#### Added - LOD Systems
- **Grass & Foliage LOD** - 4-level quality system (close/medium/far/very far)
  - Terrain detail distance adjustment
  - Grass object culling at 35m
  - Shadow removal at 20m
- **Interior Props LOD** - Dungeon decoration culling
  - Critical object detection (doors, ladders, terminals)
  - Collider-based safety checks
  - Ship and hangar exclusion
- **Rocks & Debris LOD** - Decorative object optimization
  - 3-level quality (full shadows/no shadows/disabled)
  - Culling at 40m
- **Decals LOD** - Surface detail optimization
  - Simple on/off at 30m
  - Stains, dirt, blood decals
- **Shadow Quality LOD** - Dynamic shadow casting
  - 3 quality levels based on distance
  - TwoSided shadow optimization
  - Complete shadow disable at 40m
- **Texture Quality LOD** - Automatic mipmap adjustment
  - Global quality based on object distribution
  - VRAM optimization
- **Reflection Probes LOD** - Probe quality management
  - Resolution reduction at medium distance
  - Complete disable at 60m
- **Camera Culling** - View distance limiting (disabled by default)
  - Indoor/outdoor detection
  - Configurable distances

#### Added - Graphics Optimization
- **Post-Processing LOD** - FPS-based quality adjustment
  - 3 quality levels (low/medium/high)
  - Automatic adjustment based on target FPS
  - Pixel light count management
- **Animation Culling** - Distance-based animator optimization
  - Critical animator detection (enemies, players, interactive)
  - 3 culling modes (full/reduced/disabled)
  - 20m/40m distance thresholds
- **Particle Optimization** - Particle system throttling
  - Distance-based emission rate reduction
  - Far particle culling
- **Light Culling** - Room-based light management
  - Unoccupied room detection
  - Light intensity reduction

#### Added - AI Enemy Optimization
- **Coil-Head** - Optimized spring man AI
- **Jester** - Optimized jester AI
- **Thumper** - Optimized crawler AI
- **Hoarding Bug** - Aggressive optimization (low threat)
- **Spore Lizard** - Optimized lizard AI
- **Bunker Spider** - Optimized spider AI
- **Manticoil** - Optimized bird AI

#### Added - Interior Optimization
- **Room Culling** - Distance-based room hiding
  - Minimum 5 visible rooms
  - Open door visibility consideration
  - Smooth transitions
- **Door Culling** - Behind-door object culling (disabled by default)
- **Physics Culling** - Empty room physics disable (disabled by default)

#### Added - Trap Optimization
- **Turret Optimization** - Distance-based update rates
  - Close: 30 Hz, Far: 5 Hz
  - Threat range detection
- **Landmine Optimization** - Proximity-based updates
  - Danger radius awareness
- **Spike Trap Optimization** - Update rate throttling

#### Added - Other Optimizations
- **NavMesh Optimization** - Pathfinding quality reduction
  - Obstacle avoidance quality levels
  - Acceleration reduction for distant agents
  - Critical agent detection (enemies)
- **Rigidbody Optimization** - Physics object management
  - Sleep state optimization
  - Interpolation reduction
- **Item Optimization** - Grabbable object optimization
  - Ground spawn optimization

#### Configuration Defaults
- Most optimizations **enabled** by default
- Safe, conservative settings
- Camera Culling **disabled** (limits view distance)
- Interior LOD **disabled** (may cause visual issues)
- Door/Physics Culling **disabled** (safety)