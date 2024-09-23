# CS330_Project4_BFS_Linkedlist_SparseMatrix

## Project Overview

This project implements the Breadth-First Search (BFS) algorithm using two different approaches:
1. A linked-list-based adjacency list representation.
2. Sparse matrix-vector multiplication (SpMV) using an adjacency matrix.

The code is written in C and follows a modular structure, making it easy to extend and maintain. It has been tested with provided graph datasets and includes functionality for graph traversal, matrix manipulation, and result saving.

## Features

- **Two BFS Implementations**: 
  - Linked-list adjacency list-based BFS.
  - Sparse matrix-vector multiplication (SpMV) BFS for adjacency matrices.
  
- **Matrix Operations**: 
  - Functions to load adjacency matrices, perform matrix transposition, and save BFS results.

- **Efficient Graph Traversal**:
  - Optimized for sparse graphs using both adjacency list and matrix representations.

- **Modular and Extensible**: 
  - Clear separation of concerns, allowing for easy addition of new features or improvements.

## Getting Started

### Prerequisites

- **C compiler**: Ensure you have a C compiler (like GCC) that supports the C11 standard.
- **Development Environment**: This project was tested in the `ix-dev` environment.

### Compilation

To compile the project, use the following command in your terminal:
```bash
gcc -std=c11 -o bfs bfs.c
```

### Running the Program

1. Ensure the adjacency matrix files (`test1.txt`, `test2.txt`) are available in the working directory.
2. Run the BFS implementations, specifying the source vertex.

Example command:
```bash
./bfs test1.txt 0
```
Where `test1.txt` is the graph input file and `0` is the source vertex.

The program will output the shortest distances from the source vertex and save them into result files.

### Files

- **`bfs.c`**: Contains the main implementations for both linked-list BFS and SpMV BFS.
- **`matrix_utils.c`**: Functions for loading matrices, transposing them, and saving results.
- **`test1.txt`, `test2.txt`**: Example input files containing adjacency matrices for testing.
- **`ans_X.txt`**: Expected output files with distances from source vertices (used for validation).

## BFS Implementations

### Linked List BFS

This version uses an adjacency list for graph traversal. The adjacency matrix is converted into a linked-list format for efficient sparse graph traversal.

### SpMV BFS (Sparse Matrix-Vector Multiply)

This version directly operates on an adjacency matrix using matrix-vector multiplication, optimized for sparse graphs. It minimizes space usage by leveraging sparse matrix properties.

## Matrix Manipulation

- **Matrix Loading**: Graphs are loaded from files as adjacency matrices.
- **Matrix Transpose**: Includes a function to transpose matrices for advanced graph manipulations.
- **Result Saving**: BFS results (distances from the source) are saved to output files.

## Testing

The project has been tested with two sets of input files (`test1.txt` and `test2.txt`). For each input, the BFS implementations produce output files that contain the distances from a specified source vertex to all other vertices. These results can be compared with the expected output files (`ans_X.txt`).

### Example

- Input: `test1.txt` (Adjacency matrix of a graph).
- Output: A file containing distances from the source vertex to all other vertices.
