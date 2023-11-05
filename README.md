# -A--Search-and-Probabilistic-Roadmaps-for-Robotic-Navigation-in-Occupancy-Grid-Maps

Implements A* search algorithm for efficient route planning in an 8-connected graph representation of occupancy grids.
Includes a general version of A* search abstracted for use with different graph representations, applicable to both occupancy grids and standard graphs.
Features a custom RecoverPath function to reconstruct the optimal path from start to goal after running A* search.
Utilizes the Python Imaging Library to manipulate occupancy grid map images and numpy arrays for binary thresholding.
Applies A* search to find the shortest path on a given binary occupancy grid map, plotting the path and calculating its total length.
Develops a sampling-based planner, specifically a probabilistic roadmap (PRM), to address high-dimensional planning problems where occupancy grids become impractical.
Constructs a PRM incrementally by sampling new vertices and attempting to join them to nearby vertices with a local planner.
Overlays the PRM and the optimal path found using A* search on the occupancy grid map image for visualization.
Provides implementations for uniform random sampling from free space, reachability checks between points, and construction of the PRM graph.
Explores additional algorithmic components like edge weight determination based on Euclidean distance and admissible heuristics for A* search.
