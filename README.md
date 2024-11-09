# Multi-Agent Patrolling System for Military Base Surveillance

This project focuses on designing a multi-agent system to solve a patrolling problem where multiple agents must patrol a military base represented as a graph. The goal is to ensure continuous surveillance by optimizing agent routes to minimize "idleness" (the time elapsed between successive visits to strategic zones). This project is in the planning phase and will be completed by January 2024.

Project Overview

Context

The patrolling problem involves coordinating multiple agents to regularly visit all strategic zones or points in a given environment (modeled as nodes on a graph). The objective is to maintain minimal idleness in these zones, ensuring that each location is monitored frequently. This problem becomes complex as it requires coordinating agent movement to maximize coverage without redundancy.

Use Case

For this project, the application is the surveillance of a military base. The base is modeled as a connected graph:

    Nodes represent strategic locations that require regular visits.
    Edges indicate paths between zones, with associated travel costs (representing time or difficulty).

Constraints

    1.Limited Agent Numbers: The number of agents is limited, necessitating efficient allocation to cover all zones.
    2.Mandatory Returns: Agents must return to a central node (e.g., command center) periodically, adding return trips and limiting mission autonomy.
    3.Environmental Factors: Weather conditions (rain, snow) may affect travel times and sometimes render areas inaccessible.

Optimization Criteria

The patrolling task seeks to minimize:

    Worst Idleness (WI): The maximum time any node goes unvisited at a given moment.
    Average Idleness (AI): The average time nodes go unvisited.

Planned Solution Approaches

Several strategies are being considered to address this patrolling problem. Each approach has distinct benefits and trade-offs, depending on the complexity and flexibility required.

    1.Eulerian Circuit: Each agent follows a predetermined path that ensures each edge in the graph is visited once.
        Pros: Reduces complexity by assigning each agent a fixed route.
        Cons: Lacks flexibility and adaptability to real-time conditions.

    2.Simulated Annealing: A stochastic optimization method that iteratively explores potential solutions, balancing exploration and convergence.
        Pros: Can avoid local minima and explore a wide range of solutions.
        Cons: Computationally intensive and may take time to converge.

    3.Reactive Agents (No Planning): Agents act independently, moving to the neighboring zone with the highest idleness.
        Pros: Simple to implement, no agent communication needed.
        Cons: Limited efficiency without inter-agent coordination.

    4.*Cognitive Agents (Dijkstra or A)**: Agents use pathfinding algorithms to reach high-idleness zones, coordinating with other agents to avoid overlap.
        Pros: Strategic patrolling with targeted movements to high-idleness nodes.
        Cons: High computational cost and communication overhead.

    5.Ant Colony Optimization: Inspired by real ants, agents (ants) lay pheromones on paths they travel. Agents prefer less-visited paths, while pheromone concentration decays over time to promote exploration.
        Pros: Balances exploration and exploitation, with dynamic adaptation to minimize idleness.
        Cons: Requires iterative optimization, which may be computationally demanding.

Tools and Technologies

To develop and evaluate the proposed solutions, the following tools will be used:

    Python: Main language for implementing the algorithms.
    NetworkX: Library for graph creation and manipulation, representing the military base as a weighted, undirected graph.
    Pygame: Library for creating an interactive visualization of agent movement, node coverage, and idleness.

Evaluation and Testing

Testing will involve various graph configurations to simulate different conditions within the military base. Evaluation will focus on each algorithm's ability to minimize idleness and ensure efficient coverage across these scenarios.

    1.Graph Diversity: Test with graphs of different sizes and densities to examine algorithm performance.
    2.Benchmark Resources: Validation against standard benchmarks for patrolling, including resources provided by project supervisors.

Future Goals

After initial implementation and testing, the project aims to explore further enhancements:

    Incorporating Real-World Constraints: Additional factors like energy limits or dynamic threats.
    Algorithmic Optimization: Develop hybrid solutions combining various algorithmic strengths.
    Scalability Testing: Extend to larger, more complex environments to assess robustness.
    Real-Time Adaptation: Enable agents to adjust routes dynamically in response to new obstacles or events.

Timeline

This project is under development and will be completed by January 2024. Progress updates and code implementations will be added periodically to the repository.
