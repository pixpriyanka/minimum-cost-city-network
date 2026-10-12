# minimum-cost-city-network
A C implementation of Kruskal’s algorithm to find the minimum-cost spanning tree of a weighted city network using greedy edge selection and cycle prevention.
# Minimum-Cost City Network Planner Using Kruskal's Algorithm

## Overview
The Minimum-Cost City Network Planner is a console-based C mini project that connects multiple locations at the minimum possible total cost. It uses **Kruskal's Minimum Spanning Tree (MST) algorithm**, a greedy algorithm, to select the lowest-cost links without creating cycles.

Locations represent vertices, and roads or cables represent weighted, undirected edges.

## Objectives
- Implement Kruskal's greedy algorithm in C.
- Connect all locations at minimum total cost.
- Prevent cycles using Disjoint Set Union (DSU).
- Display accepted and rejected edges.
- Detect disconnected networks where a spanning tree is impossible.

## Technologies Used
- **Programming Language:** C
- **Concepts:** Graphs, Greedy Algorithms, Minimum Spanning Tree, Sorting, Disjoint Set Union
- **Data Structures:** Arrays, structures, parent and rank arrays

## Features
1. Accepts location names and available links.
2. Validates the number of locations, edges, endpoints, and costs.
3. Sorts links in nondecreasing order of cost.
4. Uses path compression and union by rank for cycle prevention.
5. Displays the stepwise accepted/rejected edge log.
6. Displays the selected MST edges and total minimum cost.
7. Reports when the network is disconnected and a spanning tree cannot be formed.

## Algorithm
1. Read the locations and available links.
2. Sort all edges by increasing cost.
3. Initialize each vertex as a separate component.
4. Select the lowest-cost edge that connects two different components.
5. Reject an edge if it creates a cycle.
6. Stop after selecting V − 1 edges.
7. Display the MST and its total cost, or report that a spanning tree is impossible.

## How to Compile and Run

### Using GCC
Compile the program:

```bash
gcc kruskal_city_network.c -o city_network
```

Run on Windows:

```bash
city_network.exe
```

Run on Linux or macOS:

```bash
./city_network
```

### Using an IDE
Open `kruskal_city_network.c` in Code::Blocks, VS Code with a C compiler, or another C IDE. Compile and run the program.

## Sample Test Case
For four locations with links of costs 100, 200, 50, 150, and 120, the minimum spanning tree selects links costing 50, 100, and 120.

**Expected minimum total cost: 270**

## Complexity Analysis
- **Sorting:** O(E log E)
- **DSU operations:** Approximately O(E α(V)) in total
- **Overall time complexity:** O(E log E)
- **Space complexity:** O(V + E)

Here, V is the number of locations, E is the number of links, and α(V) is the inverse Ackermann function.

## Applications
- Planning city road networks.
- Designing computer and communication networks.
- Connecting offices using minimum-cost cables.
- Infrastructure and utility network planning.

## Conclusion
This project demonstrates how Kruskal's greedy algorithm constructs a minimum-cost spanning tree by selecting safe, low-cost edges and avoiding cycles. It also identifies disconnected networks, making it useful for basic infrastructure network planning.

## Author
**Mini Project — Module 3: Greedy Method Approach**

<img width="1461" height="747" alt="Screenshot 2026-10-12 202702" src="https://github.com/user-attachments/assets/ec686095-5a18-4917-a2ae-18630c800375" />
<img width="1470" height="745" alt="Screenshot 2026-10-12 202730" src="https://github.com/user-attachments/assets/c147e606-d48e-4c5d-8bc2-2957df44fb4d" />
