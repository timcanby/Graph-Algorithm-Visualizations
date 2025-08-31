# 🌐 Graph Algorithm Visualizations

<div align="center">

![GitHub stars](https://img.shields.io/github/stars/timcanby/Graph-Algorithm-Visualizations?style=social)
![GitHub forks](https://img.shields.io/github/forks/timcanby/Graph-Algorithm-Visualizations?style=social)
![GitHub issues](https://img.shields.io/github/issues/timcanby/Graph-Algorithm-Visualizations)
![GitHub license](https://img.shields.io/github/license/timcanby/Graph-Algorithm-Visualizations)

**An interactive collection of graph algorithm visualizations that bring computer science concepts to life**


</div>

---

## 📖 Overview

Graph Algorithm Visualizations is a comprehensive educational toolkit designed to make complex graph algorithms accessible and intuitive through interactive web-based visualizations. Each algorithm is presented not merely as a sequence of computational steps, but as a compelling story that reveals the underlying logic and mathematical beauty of these fundamental computer science concepts.

Built entirely with modern web technologies including D3.js, HTML5, CSS3, and ES6+ JavaScript, this project delivers self-contained visualizations that require no installation, no server setup, and no external dependencies. Simply open any HTML file in your browser and begin exploring the fascinating world of graph algorithms.


## 🚀 Quick Start

Getting started with Graph Algorithm Visualizations is incredibly simple. No installation, no configuration, no dependencies – just pure, immediate access to interactive learning.

### Method 1: Direct Download and Run
1. **Clone or download** this repository to your local machine
2. **Navigate** to the project directory
3. **Open any HTML file** (e.g., `Dijkstra.html`) in your preferred web browser
4. **Start exploring** – the visualization will load immediately and be ready for interaction

### Method 2: Online Access
1. **Visit** any of the HTML files directly through GitHub's raw file viewer
2. **Save** the file to your local machine (Right-click → Save As)
3. **Open** the saved file in your browser

### System Requirements
- **Browser**: Any modern web browser (Chrome, Firefox, Safari, Edge)
- **JavaScript**: Must be enabled (enabled by default in all modern browsers)
- **Internet**: Not required after initial download (fully offline capable)
- **Operating System**: Cross-platform (Windows, macOS, Linux, mobile)

---

## 📚 Algorithms

This collection features seven carefully selected graph algorithms, each representing a different category of graph problems and solution approaches. Every algorithm includes detailed explanations, interactive controls, and visual storytelling elements.

### 🔍 Shortest Path Algorithms

#### Dijkstra's Algorithm: Single-Source Shortest Paths
**File**: `Dijkstra.html`  
**Complexity**: O((V + E) log V)  
**Use Cases**: GPS navigation, network routing, social network analysis

Dijkstra's algorithm finds the shortest paths from a single source vertex to all other vertices in a weighted graph with non-negative edge weights. The visualization presents this as a "ripple of discovery" where shortest paths expand outward like waves from the source.

**Key Visualization Features**:
- **Live Priority Queue**: Watch as vertices are selected based on their current shortest distance
- **Color-Coded Progress**: Vertices transition through states (unvisited → visiting → visited)
- **Edge Relaxation**: See how distances are updated when shorter paths are discovered
- **Interactive Source Selection**: Click any vertex to set it as the new source

**Educational Story**: Imagine you're standing at the center of a pond and drop a stone. The ripples spread outward at a constant speed, reaching closer points first and distant points later. Dijkstra's algorithm works similarly – it discovers shortest paths in order of their actual distance from the source.

#### Floyd-Warshall Algorithm: All-Pairs Shortest Paths
**File**: `Floyd-Warshall.html`  
**Complexity**: O(V³)  
**Use Cases**: Dense graphs, transitive closure, detecting negative cycles

The Floyd-Warshall algorithm computes shortest paths between every pair of vertices using dynamic programming. This visualization uniquely combines graph and matrix representations, showing how the algorithm systematically considers each vertex as an intermediate point.

**Key Visualization Features**:
- **Synchronized Graph-Matrix View**: See how matrix updates correspond to graph changes
- **Pivot Vertex Highlighting**: Watch as each vertex serves as an intermediate point
- **Interactive Path Queries**: Click any two vertices to see their shortest path
- **Triangular Relaxation**: Visualize the core operation: if dist[i][k] + dist[k][j] < dist[i][j]

**Educational Story**: Think of this algorithm as asking "What if I could go through this intermediate city?" for every possible intermediate city. It systematically explores whether routing through each vertex provides a shorter path between any pair of destinations.

#### Bellman-Ford Algorithm: Handling Negative Weights
**File**: `Bellman-Ford.html`  
**Complexity**: O(VE)  
**Use Cases**: Currency arbitrage, network protocols, graphs with negative weights

Unlike Dijkstra's algorithm, Bellman-Ford can handle negative edge weights and detect negative cycles. The visualization emphasizes the iterative refinement process and dramatically highlights negative cycle detection.

**Key Visualization Features**:
- **Iteration-Based Animation**: See V-1 rounds of edge relaxations
- **Negative Weight Handling**: Special highlighting for negative-weight edges
- **Negative Cycle Detection**: Dramatic flashing animation when cycles are found
- **Distance Convergence**: Watch how distance estimates improve over iterations

**Educational Story**: Bellman-Ford is like a patient detective who checks every possible clue (edge) multiple times to ensure no shorter path is missed. If distances keep improving after V-1 iterations, it knows something suspicious (a negative cycle) is happening.

#### A* (A-Star) Pathfinding: Heuristic-Guided Search
**File**: `A*.html`  
**Complexity**: O(b^d) where b is branching factor and d is depth  
**Use Cases**: Game AI, robotics, puzzle solving

A* combines the guaranteed optimality of Dijkstra's algorithm with the efficiency of greedy best-first search by using a heuristic function. This grid-based visualization allows interactive obstacle placement and demonstrates intelligent pathfinding.

**Key Visualization Features**:
- **Interactive Grid Environment**: Draw walls and obstacles by clicking and dragging
- **Open/Closed Set Visualization**: See which cells are being considered vs. already processed
- **Heuristic Guidance**: Watch how the algorithm intelligently explores toward the goal
- **Dynamic Start/End Points**: Drag the start (green) and end (red) points anywhere
- **Real-time Path Updates**: See the optimal path update as you modify the environment

**Educational Story**: A* is like a smart traveler who not only considers the distance already traveled but also estimates the remaining distance to the destination. This allows it to explore promising directions first while still guaranteeing the shortest path.


### 🌳 Minimum Spanning Tree Algorithms

#### Kruskal's Algorithm: Forest Merging Approach
**File**: `Kruskal.html`  
**Complexity**: O(E log E)  
**Use Cases**: Network design, clustering, circuit design

Kruskal's algorithm builds a minimum spanning tree by considering edges in order of increasing weight and adding them if they don't create a cycle. The visualization emphasizes the forest-merging nature of this approach.

**Key Visualization Features**:
- **Edge Sorting Visualization**: See edges arranged by weight in the control panel
- **Component-Based Coloring**: Different colors represent different connected components
- **Union-Find Operations**: Watch components merge as edges are accepted
- **Accept/Reject Decisions**: Clear visual feedback for each edge consideration
- **Forest Evolution**: Observe how multiple trees gradually merge into one

**Educational Story**: Imagine you're building a railway network connecting cities with the minimum total track length. Kruskal's approach is like a cost-conscious engineer who always chooses the cheapest available connection that links previously unconnected regions.

#### Prim's Algorithm: Organic Growth Approach
**File**: `Prim.html`  
**Complexity**: O((V + E) log V)  
**Use Cases**: Network design, approximation algorithms, dense graphs

Prim's algorithm grows a minimum spanning tree from a single starting vertex, always adding the cheapest edge that connects the current tree to a new vertex. The visualization presents this as organic growth from a seed.

**Key Visualization Features**:
- **Seed-Based Growth**: Watch the tree grow organically from the starting vertex
- **Frontier Edge Highlighting**: See candidate edges that could extend the tree
- **Live Priority Queue**: Observe how frontier edges are prioritized by weight
- **Growth Animation**: Smooth transitions as the tree expands vertex by vertex
- **Tree vs. Non-Tree Edges**: Clear distinction between included and excluded edges

**Educational Story**: Prim's algorithm is like growing a plant from a seed. The tree starts small and gradually extends its reach, always choosing the most efficient (lowest weight) way to connect to new territory. Unlike Kruskal's forest-merging approach, Prim maintains a single connected component throughout.

### 🔗 Graph Structure Analysis

#### Kosaraju's Algorithm: Strongly Connected Components
**File**: `Kosaraju.html`  
**Complexity**: O(V + E)  
**Use Cases**: Social network analysis, compiler optimization, web graph analysis

Kosaraju's algorithm finds strongly connected components (SCCs) in a directed graph using two depth-first searches. The visualization reveals the elegant "tangled web → reversal → discovery" process.

**Key Visualization Features**:
- **Two-Phase Process**: First DFS on original graph, second DFS on transpose
- **Finish-Time Stack**: See how vertices are ordered by their completion times
- **Graph Reversal**: Watch the graph edges reverse direction between phases
- **SCC Clustering**: Different colors highlight each strongly connected component
- **Stack-Based Discovery**: Observe how the finish-time stack guides SCC discovery

**Educational Story**: Finding strongly connected components is like untangling a complex web of relationships. Kosaraju's brilliant insight is that by traversing the graph in a specific order (determined by finish times) and then exploring the reversed graph, we can cleanly separate the tangled structure into distinct, strongly connected groups.

---

## 🎯 Features

### 🎨 Visual Design Excellence

Each visualization is crafted with careful attention to visual design principles that enhance learning and comprehension:

**Color Psychology**: Strategic use of color to convey algorithmic states and progress. For example:
- **Green**: Represents completed/optimal states (visited vertices, final paths)
- **Blue**: Indicates active processing (current vertex, frontier edges)
- **Red**: Highlights important elements (source vertices, negative cycles, obstacles)
- **Yellow/Orange**: Shows intermediate states (vertices being considered)

**Animation Timing**: Carefully calibrated animation speeds that allow users to follow the algorithm's logic without being too slow or too fast. Each transition is timed to match the cognitive load of understanding the operation being performed.

**Information Hierarchy**: Clear visual hierarchy that guides attention to the most important elements at each step. Primary actions are prominently displayed, while supporting information is available but not distracting.

### 🎮 Interactive Controls

**Real-Time Manipulation**: Most visualizations allow real-time interaction with the graph structure:
- **Vertex Selection**: Click vertices to change source points or query paths
- **Edge Modification**: Some visualizations allow weight adjustments
- **Environment Design**: A* includes full grid editing capabilities
- **Parameter Adjustment**: Speed controls and step-by-step execution options

**Responsive Feedback**: Immediate visual response to user interactions, making the experience feel fluid and engaging rather than static and predetermined.


## 📖 Usage Guide

### 🎯 For Educators

**Classroom Integration**: These visualizations are designed to enhance traditional algorithm instruction:

**Lecture Enhancement**: Use visualizations during lectures to demonstrate algorithm concepts in real-time. The large, clear graphics work well with projectors, and the step-by-step nature allows you to pause and discuss each phase of the algorithm.

**Assignment Integration**: Assign specific visualizations as homework to reinforce concepts covered in class. Students can experiment with different graph configurations and observe how algorithms behave in various scenarios.

**Assessment Tools**: Use the visualizations to create interactive quizzes and assessments. For example, ask students to predict the next step in an algorithm or explain why certain edges are chosen in a minimum spanning tree.

**Flipped Classroom**: Students can explore algorithms independently before class, allowing classroom time to focus on deeper discussions and problem-solving applications.

### 🎓 For Students

**Self-Paced Learning**: Each visualization includes comprehensive explanations and intuitive controls:

**Concept Exploration**: Start with simpler algorithms like Dijkstra's and progress to more complex ones like Kosaraju's. The visual nature helps build intuition before diving into mathematical proofs.

**Experimentation**: Try different graph configurations to see how algorithms behave. What happens to Dijkstra's algorithm on a graph with many equal-weight edges? How does A* perform with different heuristic functions?

**Debugging Understanding**: If you're implementing these algorithms in code, use the visualizations to debug your understanding. Compare your algorithm's behavior with the visualization to identify discrepancies.

**Exam Preparation**: Practice tracing through algorithms manually, then verify your work with the visualizations. This builds the pattern recognition skills needed for algorithm analysis exams.

### 🔬 For Researchers and Professionals

**Algorithm Comparison**: Use multiple visualizations to compare different approaches to the same problem:

**Teaching Tool Development**: The open-source nature makes these visualizations excellent starting points for developing more specialized educational tools.

**Presentation Aid**: Include these visualizations in conference presentations or technical talks to make complex algorithms accessible to diverse audiences.

**Prototyping**: Use the clear algorithm implementations as starting points for more complex research implementations.

---

## 🎮 Interactive Demo Examples

### Dijkstra's Algorithm Walkthrough

1. **Open** `Dijkstra.html` in your browser
2. **Observe** the initial graph with weighted edges
3. **Click** any vertex to set it as the source (it will turn green)
4. **Watch** as the algorithm explores vertices in order of their distance from the source
5. **Notice** how the priority queue (displayed on the right) updates as new vertices are discovered
6. **Experiment** with different source vertices to see how the shortest path tree changes

### A* Pathfinding Interactive Experience

1. **Open** `A*.html` in your browser
2. **Click and drag** on the grid to create walls and obstacles
3. **Drag** the green start point and red end point to different locations
4. **Click** "Start Search" to watch A* find the optimal path
5. **Observe** how the algorithm intelligently explores toward the goal rather than expanding uniformly
6. **Try** different obstacle configurations to see how A* adapts its search strategy

### Kruskal vs. Prim Comparison

1. **Open** both `Kruskal.html` and `Prim.html` in separate browser tabs
2. **Compare** how the two algorithms build the same minimum spanning tree using different strategies
3. **Notice** how Kruskal considers edges globally while Prim grows from a single point
4. **Observe** the different intermediate states – Kruskal creates a forest that merges, while Prim maintains a single connected component



<div align="center">

**Made with ❤️ for computer science education**

[⭐ Star this repository](https://github.com/timcanby/Graph-Algorithm-Visualizations) if you find it useful!

</div>


