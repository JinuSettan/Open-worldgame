# WORLD: Rise of the Underworld

An open-world, single-player action story game built around Alex, a young man whose journey from a small island pulls him into an international criminal organisation, a conspiracy involving human experimentation, and a city-wide outbreak.

> **Project status:** Pre-production / foundation setup  
> **Target engine:** Unreal Engine 5  
> **Target platforms:** Windows PC and Android  
> **Visual direction:** Cinematic realism, with platform-specific performance profiles

## Project identity

- **Game:** WORLD: Rise of the Underworld
- **Hero:** Alex
- **Mode:** Single-player story + open world
- **First development priority:** Build the San Veyra open-world region
- **Story structure:** 5 Acts / 50 planned missions
- **Important:** This repository is the WORLD game project. It is separate from MAYA, TESSA, and DogFightWar.

## Premise

Alex lives on Isla Mar, a small island where money is scarce and life revolves around the sea. After a dangerous sea accident, he leaves home to find work. In a foreign city he meets Russell and becomes involved in an attack on Viktor, the leader of the powerful fictional organisation Black Crown. Alex saves Viktor and is offered a place in the organisation.

As Alex rises through Black Crown, he discovers a conspiracy involving secret experiments, corrupt officials, and an outbreak of infected people. His personal losses force him to decide what kind of future the country should have.

## Planned regions

- **Isla Mar** — Alex's island home and opening area.
- **San Veyra, USA** — the first major open-world city and primary development target.
- **Nevada, USA** — secret research facilities and desert missions.
- **New York, USA** — a later international story region.
- **Moscow, Russia** — a later international story region.

All fictional locations and factions are original game-world creations.

## Core gameplay pillars

- Third-person exploration and story missions
- Driving, boats, and aircraft
- Safehouses, properties, shops, and side activities
- Civilian, police, gang, and infected AI
- Faction reputation and story choices
- Wanted / law-enforcement response system
- Dynamic day-night cycle and weather
- Save system and multiple endings

## Story structure

See [Docs/STORY.md](Docs/STORY.md) and [GameData/Missions](GameData/Missions).

1. The Stranger
2. The Rise
3. The Virus
4. Revenge
5. The King

Planned endings: **The King**, **Freedom**, and **The Last Virus**.

## Technical direction

Unreal Engine 5 is the intended engine. World Partition and HLOD will be evaluated for large-world streaming. The project will use a shared gameplay foundation with separate PC and Android scalability profiles. Mobile support must be validated on real devices; high-end PC rendering features must not be assumed to work on Android.

See [Docs/TECHNICAL_ARCHITECTURE.md](Docs/TECHNICAL_ARCHITECTURE.md).

## Repository layout

- `Docs/` — design and technical documentation
- `GameData/` — structured story and mission data
- `Assets/` — source asset inventory and future imported assets
- `Unreal/WORLD/` — planned Unreal project location

The Unreal Editor must generate the actual `.uproject`, maps, and binary assets. Placeholder or fake Unreal asset files will not be committed.

## Development principles

1. Build San Veyra first; expand to other regions after the core streaming and gameplay loop works.
2. Greybox first, art polish later.
3. Keep story data separate from mission logic where practical.
4. Profile Android continuously; do not treat PC settings as mobile-ready.
5. Track asset provenance and licenses before shipping.
6. Do not commit generated build folders or secrets.

## Current milestone

**M0 — Project foundation:** repository structure, story bible, world plan, technical plan, mission outline, and asset inventory.

See [Docs/ROADMAP.md](Docs/ROADMAP.md).
