# A* Search and Probabilistic Roadmaps

[HW_3.ipynb](HW_3.ipynb) demonstrates A* search on an eight-connected occupancy grid and graph search on a sampled probabilistic roadmap.

## Run the notebook

1. Open it in Colab or Jupyter with NumPy, Pillow, Matplotlib, NetworkX, SciPy, and pyparsing installed.
2. Supply a grayscale occupancy-map PNG. Zero-valued pixels are obstacles and nonzero pixels are free space. The original map is external to this repository.
3. Update all three map reads to point to your PNG. Skip the first Drive mount cell when running locally.
4. Set valid free start and goal cells in both sections using row, column order, then run the cells in order.

The notebook includes saved outputs from the original map. The roadmap samples free cells randomly.
