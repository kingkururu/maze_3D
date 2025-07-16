# 3D Maze Game

A 3D maze game built with C++ and SFML, featuring advanced pathfinding algorithms and automated navigation systems. Building on the raycasting algorithm from previous projects, this game incorporates intelligent maze generation and AI-assisted pathfinding for enhanced gameplay experience.

<img width="641" alt="Image" src="https://github.com/user-attachments/assets/681bd3e9-5e92-47ae-bc73-865dbb595454" />
<img width="884" alt="Image" src="https://github.com/user-attachments/assets/4856a85c-618c-4cc3-9e42-bb8f56957bd5" />
<img width="950" alt="Image" src="https://github.com/user-attachments/assets/ae51ba5a-fd90-45b8-8330-e17a46d82088" />

## 🎯 Features

- **Procedural Maze Generation**: Random maze creation using Depth-First Search and Prim's algorithms
- **3D Raycasting Rendering**: Immersive 3D perspective from 2D maze data
- **Auto-Navigation**: Computer-guided movement with "Navigate Maze" functionality
- **Real-time Path Visualization**: Visual representation of calculated paths
- **Performance Optimized**: Efficient maze generation and pathfinding algorithms
- **File I/O Integration**: Save and load maze configurations
  
## 🎮 Controls

- **W**: Move forward
- **S**: Move backward  
- **A**: Rotate camera left / turn player left
- **D**: Rotate camera right / turn player right
  
## 📁 Project Structure

```
/maze_3D
│
├── .vscode/                   # VSCode settings and configurations
│
├── src/                       # Source files
│   ├── main.cpp              # Main entry point of the game
│   └── game/                 # Core engine functionalities
│       ├── globals/          # Constants and flags
│       ├── core/             # Game loop and state management
│       ├── physics/          # Physics and collision detection
│       ├── camera/           # SFML window and view management
│       ├── utils/            # Utility functions
│       └── scenes/           # Scene management
│
├── assets/                    # Game assets
│   ├── fonts/                # Font files and sources
│   ├── sound/                # Sound effects
│   ├── tiles/                # Tiles and tilemaps
│   └── sprites/              # Sprite images
│
├── libs/                      # External libraries
│   └── logging/              # Logging system
│
├── test/                      # Test game (example project)
├── Makefile                   # Build instructions
└── README.md                  # Project documentation
```
### Prerequisites
- **Compiler**: Requires clang++ (or g++) with C++17 support
- **SFML**: Simple and Fast Multimedia Library for graphics and windowing
- **Custom Game Framework**: Built on top of the SFML Game Framework

## 🚀 Building & Running

### Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/kingkururu/maze_3D
   cd maze_3D (location will be different)
   ```

2. **Build the Project**:
   ```bash
   make
   ```
   This will compile the raycasting demo along with the game framework.

3. **Run the Demo**:
   ```bash
   make run
   ```

4. **Clean the Build**:
   ```bash
   make clean
   ```
### Alternative Setup (macOS with Homebrew)

1. **Install SFML**:
   ```bash
   # Install Homebrew if not already installed
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   
   # Install SFML
   brew install sfml@2
   brew install .... (other missing libraries)
   ```

2. **Configure PATH** (add to ~/.zshrc or ~/.bash_profile):
   ```bash
   export PATH="/opt/homebrew/bin:$PATH"
   export PATH="/opt/homebrew/opt/sfml@2/bin:$PATH"
   export PATH="path to other libraries if any of them is missing)
   ```

## 🎯 Key Learning Outcomes

- **Algorithm Implementation**: Understanding maze generation and pathfinding algorithms
- **Graph Theory Applications**: Practical application of DFS, Prim's, and A* algorithms
- **AI Integration**: Implementing computer-assisted navigation and guidance systems
- **Performance Optimization**: Efficient algorithms for real-time maze generation and pathfinding
- **Data Structures**: Advanced use of graphs, priority queues, and spatial data structures
- **File I/O Operations**: C++ file handling for maze persistence and configuration
- **Game AI Development**: Creating intelligent navigation systems for enhanced gameplay

### Maze Generation Process
The game implements a sophisticated maze generation system that:
1. **Algorithm Selection**: Choose between DFS and Prim's algorithms for different maze characteristics
2. **Procedural Generation**: Create unique maze layouts using selected algorithms
3. **Path Optimization**: Calculate optimal routes using A* pathfinding
4. **File Operations**: Save generated mazes and load configurations
5. **Visual Rendering**: Display maze in 3D using raycasting techniques

### AI Navigation System
- **Pathfinding Integration**: A* algorithm calculates optimal routes from start to goal
- **Heuristic Optimization**: Combines actual distance with estimated remaining distance
- **Auto-Navigation**: Computer-controlled movement following calculated paths
- **Dynamic Guidance**: Real-time path updates and player assistance
- **Manual Override**: Player can deviate path and start guided navigation

## 🧠 Algorithm Details

### Depth-First Search (DFS)
Creates mazes with long, winding passages by exploring paths as far as possible before backtracking. Results in fewer dead ends and more challenging navigation.

### Prim's Algorithm
Generates more evenly distributed maze layouts by expanding outward from random points, creating shorter, more interconnected passages.

### A* Pathfinding
Combines the guaranteed optimality of Dijkstra's algorithm with heuristic guidance, efficiently finding the shortest path from start to goal using estimated distances.

## 🎨 Assets Credits

- **Music**: [Best Game Console](https://pixabay.com/music/video-games-game-background-1-321720/) from Pixabay
- **Graphics**: Custom artwork created using Canva and Canva AI
- **Framework**: Built using the Custom SFML Game Framework https://github.com/kingkururu/sfml_game_template/edit/main/README.md
