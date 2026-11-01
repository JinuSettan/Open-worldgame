# Technical Architecture

## Engine
Unreal Engine 5. Use a C++ foundation for reusable gameplay systems and Blueprints for iteration, mission scripting, and presentation.

## Planned project modules
- WORLDGameInstance — global session and profile setup
- WORLDGameMode — rules for the active game mode
- WORLDPlayerCharacter — player movement and interaction
- WORLDPlayerController — input and player-facing control
- WORLDWorldSubsystem — region and world-state coordination
- WORLDMissionSubsystem — mission state and objective flow
- WORLDSaveGame — persistent save data
- WORLDVehicleBase — shared vehicle interaction contract
- WORLDAIController — common AI controller foundation
- WORLDFactionComponent — faction affiliation and relationship data

These are design targets, not existing compiled classes.

## World technology
- World Partition for large-world streaming
- Data Layers for mission, outbreak, and restricted-area variants
- HLOD for distant environment representation
- Landscape and spline tools for terrain and roads
- NavMesh for AI navigation
- Static meshes and instanced meshes for environment dressing

## Gameplay systems
- Character Movement Component for Alex
- Chaos Vehicles for ground vehicles
- AI Controllers and Behavior Trees for NPC behaviours
- UMG for UI
- Data Assets / Data Tables for mission definitions
- SaveGame for persistent player and story state
- MetaSounds / Sound Cues for audio

## AI groups
Civilian, police, gang, and infected. Nearby actors may use full behaviour logic; distant crowds should use simplified simulation to protect CPU and memory budgets.

## Infected state model
Idle → Patrol → Suspicious → Investigate → Chase → Attack → Search → Return.

## Platform profiles
### PC
Scalable high-quality rendering, higher NPC and traffic budgets, configurable resolution, and advanced lighting only where supported by the target hardware.

### Android
Separate mobile scalability profile, dynamic resolution, reduced shadows and effects, smaller texture budgets, limited crowd/traffic density, and mobile-friendly lighting. Do not assume Nanite or Lumen is available or performant on every Android device. Validate on actual target phones early.

## Development constraint
A full Unreal Editor workflow and Android packaging generally require a Windows development environment with the appropriate Unreal toolchain. GitHub stores source and documentation; it does not replace the Unreal Editor or build machine.
