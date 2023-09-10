## Genetic Algorithm for Solving the Traveling Salesman Problem (TSP)

<img src="pic.png" alt="Image Description" width="700"/>

## Introduction

This project implements a Genetic Algorithm in Python to solve the Traveling Salesman Problem (TSP). The TSP is a well-known NP-Hard problem that involves finding the shortest possible cycle that visits a set of cities exactly once and returns to the starting city.

## Algorithm Overview

### Data Input

The algorithm begins by reading input data from a file containing information about cities and the distances between them. It constructs an adjacency matrix to store the distances between each pair of cities.

### Population Initialization

A population of random permutations of cities is generated to represent potential solutions. The size of the population is configurable, but a typical value is 1000.

### Fitness Function

The fitness function calculates the total distance of the cycle for each solution in the population. The lower the total distance, the better the fitness of the solution.

### Genetic Operations

The algorithm employs genetic operations including selection, crossover (order recombination), and mutation to evolve the population over multiple generations.

#### Selection

Parents are selected from the current population based on their fitness. The selection process is biased towards better-performing solutions. Around 60% of the population is chosen as parents based on certain criteria.

#### Crossover (Order Recombination)

Pairs of parents are selected, and a random subset of cities is chosen from one parent while maintaining the order of those cities. The remaining cities are filled in the child solution using the other parent while preserving the order.

#### Mutation

Approximately 10% of the children undergo mutation. In mutation, four random cities in a child solution are selected, and their positions are swapped to introduce genetic diversity.

### Population Update

After genetic operations, the population is updated. The worst-performing solutions are replaced with the newly generated children.

### Termination

The algorithm continues for a fixed number of generations, in this case, 150 generations. After each generation, the best cycle found so far and its fitness are recorded.
