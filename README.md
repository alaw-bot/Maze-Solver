# Maze-Solver
# Maze Solver

A comprehensive maze generation and solving application that implements multiple pathfinding algorithms with interactive visualization.

## 🎯 Features

- **Two Operating Modes:**
  - Generate and solve randomly created mazes
  - Load and solve maze images from files
  
- **Multiple Pathfinding Algorithms:**
  - Breadth-First Search (BFS)
  - Dijkstra's Algorithm
  - A* Search Algorithm

- **Interactive Interface:**
  - Click-to-select start and end points
  - Real-time algorithm visualization
  - Animated path discovery process

- **Flexible Maze Sizes:**
  - 9x9, 16x16, and 21x21 pre-defined sizes
  - Support for custom maze images

## 🛠️ Technologies Used

- **Python 3.x**
- **NumPy** - Numerical computations and maze representation
- **Pygame** - Interactive GUI and visualization
- **Matplotlib** - Image handling and plotting
- **scikit-image** - Image processing and skeletonization
- **Collections & Heapq** - Data structures for algorithms

## 📋 Prerequisites

Make sure you have Python 3.x installed on your system. You can download it from [python.org](https://www.python.org/).

## 🚀 Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/maze-solver.git
   cd maze-solver
   ```

2. **Install required dependencies:**
   ```bash
   pip install numpy pygame matplotlib scikit-image
   ```

   Or using requirements.txt (if available):
   ```bash
   pip install -r requirements.txt
   ```

## 🎮 Usage

### Running the Application

```bash
python maze_solver.py
```

### Option 1: Pre-defined Maze

1. Select option `1` when prompted
2. Choose maze size (9x9, 16x16, or 21x21)
3. Click on the maze to set the **START point** (appears green)
4. Click on a different location to set the **END point** (appears red)
5. Choose your preferred algorithm:
   - `1` - Breadth-First Search (BFS)
   - `2` - Dijkstra's Algorithm  
   - `3` - A* Search
6. Watch the algorithm solve the maze in real-time!
7. Press `R` to reset and generate a new maze

### Option 2: Image Maze

1. Select option `2` when prompted
2. Enter the relative path to your maze image file
3. Click on the displayed image to select start and end points
4. Choose your preferred solving algorithm
5. View the solution overlaid on your original maze image

## 🧠 Algorithm Comparison

| Algorithm | Time Complexity | Space Complexity | Optimal | Description |
|-----------|----------------|------------------|---------|-------------|
| **BFS** | O(V + E) | O(V) | ✅ Yes | Explores all nodes at current depth before moving deeper |
| **Dijkstra** | O((V + E) log V) | O(V) | ✅ Yes | Finds shortest path considering edge weights |
| **A*** | O(b^d) | O(b^d) | ✅ Yes* | Uses heuristics to guide search (*with admissible heuristic) |



## 🖼️ Supported Image Formats

The application supports common image formats including:
- PNG
- JPG/JPEG
- BMP
- TIFF

**Image Requirements:**
- Black walls, white paths
- Clear contrast between walls and pathways
- Reasonable resolution for processing

## ⚡ Performance Notes

- **Small mazes (9x9):** All algorithms perform similarly
- **Medium mazes (16x16):** A* typically outperforms others
- **Large mazes (21x21+):** A* shows significant advantage
- **Image mazes:** Performance depends on image complexity and resolution

## 🎨 Customization

### Color Scheme
You can modify the color scheme by editing the `colors` dictionary in the `draw_maze()` function:

```python
colors = {
    "wall": (0, 0, 0),        # Black walls
    "path": (255, 255, 255),   # White paths
    "start": (0, 255, 0),      # Green start
    "end": (255, 0, 0),        # Red end
    "explored": (173, 216, 230), # Light blue explored
    "current": (255, 165, 0),   # Orange current
    "solution": (0, 0, 255),    # Blue solution path
}
```

### Algorithm Speed
Adjust visualization speed by modifying the `time.sleep()` values in the algorithm functions.

## 🐛 Troubleshooting

### Common Issues:

1. **"No module named 'pygame'"**
   - Solution: `pip install pygame`

2. **"Could not find valid start or end points"**
   - Ensure you're clicking on white/path areas in the maze
   - Try clicking closer to clearly defined pathways

3. **Image not loading**
   - Check file path is correct and relative to script location
   - Ensure image format is supported

4. **Slow performance on large images**
   - Consider resizing large images before processing
   - Use smaller maze sizes for real-time visualization


## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### Development Setup

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📞 Support

If you encounter any issues or have questions, please:
1. Check the troubleshooting section above
2. Search existing issues on GitHub
3. Create a new issue with detailed description

## 🔮 Future Enhancements

- [ ] Additional algorithms (Greedy Best-First, Jump Point Search)
- [ ] 3D maze support
- [ ] Maze difficulty rating system
- [ ] Export solution as image/video
- [ ] Web-based interface
- [ ] Mobile app version

---

⭐ If you found this project helpful, please give it a star on GitHub!
