# Cub3D

A 3D graphical game inspired by **Wolfenstein 3D**, built as part of the 42 School curriculum.  
This project uses the **MiniLibX** library to render a first-person view using a **raycasting** engine.

---

## 🎯 Project Goal
- Implement a basic 3D engine from scratch using **raycasting**.
- Load and parse a `.cub` configuration file to set up:
  - Map layout
  - Wall textures
  - Floor and ceiling colors
- Render the world in real-time with smooth player movement.

---
![Gameplay view](https://github.com/user-attachments/assets/bce4f1bb-7bea-4214-8f2e-e596f659c3b8)

---

## 🛠 Features
- **Raycasting with DDA** for wall detection.
- Textured walls with north/south/east/west mapping.
- Customizable floor and ceiling colors.
- Player movement & rotation with WASD + arrow keys.
- Minimap with centered player and entities.
- Dynamic lighting and flashlight effect.
- Animated sprites and FOV rendering.

---

## 📂 File Structure
├── includes/ # Header files   
├── mandatory/ # Source code for mandatory part     
├── bonus/ # Source code for bonus part     
├── textures/ # Wall/sprite textures     
├── maps/ # Example .cub maps        
├── Makefile    
└── README.md        

## 🗺 Map Format
A `.cub` file contains:
- **Texture paths** for each wall orientation:
NO ./textures/wall_north.xpm
SO ./textures/wall_south.xpm
WE ./textures/wall_west.xpm
EA ./textures/wall_east.xpm

- **Colors** for floor/ceiling:
F 220,100,0
C 225,30,0

- **Map layout** with:
- `1` for walls
- `0` for empty space
- `N`, `S`, `E`, `W` for player start position
- `2` or custom values for sprite
- `D` for door

---

## 🔧 Installation
```bash
git clone git@github.com:elinakly/cub3d_42.git
cd cub3d_42
make
```
- **Usage**
```bash
./cub3d maps/classic.cub
```

## BONUS
```bash
make bonus
./cub3d maps/classic_bonus.cub
```

**Controls:**

W/A/S/D → Move forward/left/backward/right

← / → → Rotate view or mouse

ESC → Exit game
