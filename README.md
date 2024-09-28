# A* Search and Probabilistic Roadmaps for Robotic Navigation in Occupancy Grid Maps

This project implements advanced path planning algorithms for robotic navigation using occupancy grid maps. It combines the efficiency of A* search with the flexibility of Probabilistic Roadmaps (PRM) to solve complex navigation problems.

## Features

### A* Search Implementation
- Efficient route planning in 8-connected graph representation of occupancy grids
- Generalized A* search algorithm applicable to various graph representations
- Custom `RecoverPath` function for optimal path reconstruction

### Occupancy Grid Handling
- Utilizes Python Imaging Library for occupancy grid map manipulation
- Employs `numpy` arrays for binary thresholding of maps

### Path Planning and Visualization
- Applies A* search to find the shortest path on binary occupancy grid maps
- Plots the optimal path and calculates its total length
- Overlays PRM and A* path on the occupancy grid map for visual analysis

### Probabilistic Roadmap (PRM)
- Sampling-based planner for high-dimensional planning problems
- Incremental PRM construction through vertex sampling and local planning
- Implements uniform random sampling from free space
- Includes reachability checks between points

### Additional Components
- Edge weight determination based on Euclidean distance
- Admissible heuristics for A* search optimization

## Implementation Details

1. **Graph Representation**: The project uses an 8-connected graph to represent occupancy grids, allowing for more flexible movement options.

2. **A* Search Algorithm**: A generalized version of A* search is implemented, which can be used with different graph representations, including standard graphs and occupancy grids.

3. **Path Recovery**: A custom `RecoverPath` function reconstructs the optimal path from start to goal after running A* search.

4. **Image Processing**: The Python Imaging Library is used to manipulate occupancy grid map images, while `numpy` arrays handle binary thresholding.

5. **Probabilistic Roadmap**: The PRM is constructed incrementally by sampling new vertices and attempting to join them to nearby vertices using a local planner.

6. **Visualization**: The project provides tools to overlay the PRM and the optimal path found by A* search on the occupancy grid map image for easy visualization and analysis.

This project combines classical graph search algorithms with modern sampling-based techniques to provide a comprehensive solution for robotic navigation in complex environments.

## Usage

```python
# Example code snippet
import astar
import prm

# Load occupancy grid
grid = load_occupancy_grid("map.png")

# Run A* search
start = (0, 0)
goal = (100, 100)
path = astar.search(grid, start, goal)

# Construct PRM
roadmap = prm.construct(grid, num_samples=1000)

# Visualize results
visualize(grid, path, roadmap)
```

## Dependencies

- Python 3.x
- NumPy
- Pillow (Python Imaging Library)
- Matplotlib (for visualization)

## Installation

```bash
git clone https://github.com/yourusername/A-Star-and-PRM-Navigation.git
cd A-Star-and-PRM-Navigation
pip install -r requirements.txt
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
