# Infiniminer - The Voxel Mining Game that Inspired Minecraft

## Overview
This repository contains the full source code for **Infiniminer**, an open-source, block-based multiplayer sandbox game developed by **Zach Barth** (Zachtronics Industries). Released in 2009, Infiniminer introduced the core concept of a procedurally generated voxel world where players could dig and build. Its source code became public after the developer discontinued the project, directly leading to the creation and early architecture of **Minecraft**.

## Project Details
- **Developer**: Zach Barth (Zachtronics)
- **Year**: 2009
- **Platform**: Windows (XNA Framework)
- **Language**: C#

## Technology Stack
- **Languages**: C# (.NET).
- **Engine**: Microsoft XNA 3.0 / 4.0.
- **Networking**: Lidgren Networking Library.
- **Graphics**: HLSL (Visible in `.fx` files like `effect_basic.fx`).

## Repository Structure & Modules

### 1. Client (`InfiniminerClient/`)
- **Engines/**: The core systems of the game.
    - `BlockEngine.cs`: Implements the voxel rendering and block interaction logic.
    - `SkyboxEngine.cs`: Manages the environment and background rendering.
    - `PlayerEngine.cs`: Handles first-person movement and physics.
- **States/**: Management for game screens (Loading, Menu, In-game).
- **InfiniminerGame.cs**: The main XNA game loop and manager.

### 2. Server (`InfiniminerServer/`)
- Handles the authoritative game state and broadcasts block changes to clients.

### 3. Shared (`InfiniminerShared/`)
- Definitions for block types, network packets, and shared utilities used by both client and server.

## Key Technical Features
- **Voxel Rendering**: An early implementation of face-culling and chunk-management for 3D blocks.
- **Multiplayer Synchronization**: Real-time digging and building synchronized across a network.
- **Class-Based Gameplay**: Originally intended as a team-based competitive game (miners, engineers, etc.), which is reflected in the player class logic.

## Historical Significance
Infiniminer is one of the most influential "forgotten" games in history. After its source code was leaked/released, **Markus "Notch" Persson** used its blocky aesthetic and digging mechanics as the foundation for the first versions of Minecraft.

## How to Explore
1. **InfiniminerClient/Engines/BlockEngine.cs**: Examine the code that handles how the blocks are stored and rendered.
2. **InfiniminerGame.cs**: Trace the startup sequence to see how XNA initializes the graphics device.
3. **InfiniminerShared/**: Look at the block definitions to see how the world "palette" was constructed.
