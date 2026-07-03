# Heuristic Algorithm Teaching Notebooks

This repository is a heuristic algorithm project designed for teaching and classroom demonstrations. Each algorithm is provided as an independent Jupyter Notebook, with emphasis on three things:

1. The underlying idea should be explained clearly.
2. The experiments should run successfully.
3. The visualizations should be intuitive enough for teaching.

The project is suitable for:

- classroom instruction
- introductory algorithm lab courses
- self-study for heuristic algorithms
- talks, lectures, or teaching demos

## Project Structure

The project currently includes 12 core heuristic algorithm notebooks. Directories are numbered so they can be taught in a natural sequence.

```text
.
├── PRD_Heuristic_Algorithms.md
├── README.md
├── pyproject.toml
├── 01_Hill_Climbing/
├── 02_Random_Restart_Hill_Climbing/
├── 03_Simulated_Annealing/
├── 04_Tabu_Search/
├── 05_Genetic_Algorithm/
├── 06_Evolution_Strategy/
├── 07_Differential_Evolution/
├── 08_Particle_Swarm_Optimization/
├── 09_Ant_Colony_Optimization/
├── 10_Artificial_Bee_Colony/
├── 11_GRASP/
└── 12_Iterated_Local_Search/
```

## Algorithm List

### Continuous Optimization and Local Search

1. `01_Hill_Climbing`
   Hill Climbing
   Classic example: Himmelblau function
2. `02_Random_Restart_Hill_Climbing`
   Random Restart Hill Climbing
   Classic example: Rastrigin function
3. `06_Evolution_Strategy`
   Evolution Strategy
   Classic example: Rosenbrock function
4. `07_Differential_Evolution`
   Differential Evolution
   Classic example: Ackley function
5. `08_Particle_Swarm_Optimization`
   Particle Swarm Optimization
   Classic example: Himmelblau function
6. `10_Artificial_Bee_Colony`
   Artificial Bee Colony
   Classic example: Ackley function

### Combinatorial Optimization and Path Search

1. `03_Simulated_Annealing`
   Simulated Annealing
   Classic example: TSP
2. `04_Tabu_Search`
   Tabu Search
   Classic example: TSP
3. `05_Genetic_Algorithm`
   Genetic Algorithm
   Classic example: TSP
4. `09_Ant_Colony_Optimization`
   Ant Colony Optimization
   Classic example: TSP
5. `11_GRASP`
   Greedy Randomized Adaptive Search Procedure
   Classic example: TSP
6. `12_Iterated_Local_Search`
   Iterated Local Search
   Classic example: TSP

## Shared Notebook Structure

Most notebooks follow the same teaching structure:

1. Learning objectives
2. Why this classic example was chosen
3. Algorithm intuition
4. From-scratch implementation
5. Single-run demonstration
6. Visualization of results
7. Statistics over multiple runs
8. Parameter sensitivity analysis
9. Classroom summary

The purpose is to let students switch between algorithms without having to adapt to a new reading pattern each time.

## Environment Setup

Python 3.11 or later is recommended.

### Install with `pyproject.toml`

If you use a toolchain that supports `pyproject.toml`, you can install dependencies from it directly.

For example, with `pip`:

```bash
pip install -e .
```

Or install the core dependencies directly:

```bash
pip install numpy pandas matplotlib seaborn jupyter nbconvert nbformat ipykernel
```

## Running the Notebooks

### Start Jupyter

```bash
jupyter notebook
```

or:

```bash
jupyter lab
```

### Suggested Teaching Order

If you plan to use this for teaching, the following order is recommended because it builds algorithm intuition more naturally:

1. `01_Hill_Climbing`
2. `02_Random_Restart_Hill_Climbing`
3. `03_Simulated_Annealing`
4. `04_Tabu_Search`
5. `05_Genetic_Algorithm`
6. `08_Particle_Swarm_Optimization`
7. `09_Ant_Colony_Optimization`
8. `06_Evolution_Strategy`
9. `07_Differential_Evolution`
10. `10_Artificial_Bee_Colony`
11. `11_GRASP`
12. `12_Iterated_Local_Search`

The logic behind this order is:

- start with the most intuitive local search methods
- then move to strategies that can escape local optima
- transition into population-based and swarm-intelligence methods
- finish with constructive and iterative-improvement approaches

## Teaching Suggestions

If you are using these notebooks for a course or lecture, each notebook should at least address the following questions:

1. What is the algorithm's core search move?
2. Why can it improve the current solution?
3. Why can it fail?
4. How does it balance exploration and exploitation?
5. Which parameter matters most, and what does it control?

### Focus Points for Continuous Optimization

For continuous optimization notebooks, it is recommended to pay special attention to:

- search trajectories on contour plots
- how the population distribution evolves
- the rate at which convergence curves decrease

### Focus Points for TSP Notebooks

For TSP notebooks, it is recommended to pay special attention to:

- the difference between the initial route and the final route
- how route structure changes during the process
- how different algorithms generate new candidate routes

## Visualization Notes

The charts in this project are designed to explain clearly rather than simply look attractive. As a result, most notebooks include at least:

1. a convergence curve
2. a search-process figure
3. a final-result figure

Some algorithms also include targeted visualizations:

- PSO: particle position evolution
- ACO: pheromone heatmap
- GA: population distribution or fitness distribution
- SA: acceptance rate changes
- GRASP / ILS: before-and-after comparisons for construction or perturbation

## Related Files

- Project-level design document: [PRD_Heuristic_Algorithms.md](./PRD_Heuristic_Algorithms.md)

## Notes

This material currently prioritizes teaching clarity. The implementations are designed to be readable in class rather than packaged as industrial-grade high-performance code. Possible future extensions include:

- more benchmark functions
- more complex TSP datasets
- animated visualizations
- interactive parameter controls
- a unified export set for lecture slides
