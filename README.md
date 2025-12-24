# Traveling Salesman Problem – Spaceship Signal Routing

This project explores a variant of the Traveling Salesman Problem (TSP) in a 3D space setting, where an alpha spaceship must transmit a signal to a set of other ships located at unique (x, y, z) coordinates and return to its origin. The signal must visit every spaceship exactly once, and each leg of the route is based on the Euclidean distance between ships. The goal is to determine the shortest possible route that starts and ends at the alpha ship. The notebook implements and analyzes three approaches: Brute Force, Dynamic Programming (Held-Karp), and Greedy Heuristic. The brute force method evaluates all (n−1)! route permutations and computes total distances, resulting in O(n × (n−1)!) time and O(n) space complexity. The dynamic programming solution builds a state table using bitmasking and minimizes subproblem overlap, achieving O(n² × 2ⁿ) time and space complexity. The greedy method approximates the solution by selecting the nearest unvisited spaceship at each step, completing the route in O(n²) time and O(n) space. All methods are compared in terms of accuracy and efficiency. Brute Force and Dynamic Programming yield optimal results for small and medium input sizes, respectively, while the Greedy method provides a fast, near-optimal route for larger datasets. The notebook includes implementation code, test cases, and performance analysis for each algorithm.

# Minimum Landing Pads Scheduler

This project solves a scheduling problem inspired by a spaceport scenario: determining the minimum number of landing pads required so no spaceship has to wait. Given a list of landing and departure times, the goal is to calculate peak pad usage using three algorithmic approaches — Brute Force, Greedy, and Divide & Conquer.

Each solution includes:
- Pseudocode and Python implementation
- Test drivers with sample inputs
- Execution time benchmarking and complexity analysis

**Approaches Implemented:**
- **Brute Force**: Iterates minute-by-minute and checks overlaps; O(n × 2401)
- **Greedy**: Sorts landing/departure times and sweeps through them efficiently; O(n log n)
- **Divide and Conquer**: Recursively splits event windows to track peak pad usage; O(n log n)

To run the project, open the Jupyter notebook and execute each cell in sequence. All dependencies are standard and included in Google Colab.

This repository is ideal for comparing algorithm efficiency and correctness in interval scheduling problems. Insights into performance scaling across input sizes are included at the end of the notebook.
