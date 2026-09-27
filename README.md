# AVL Trees for Fast Searching

## Capstone / Research Exploration Project

This project explores **AVL Trees**, a self-balancing Binary Search Tree (BST) that maintains efficient searching by controlling tree height.

The project investigates how an ordinary BST can become unbalanced depending on insertion order and how AVL Trees address this problem using rotations.

## Problem

A Binary Search Tree can provide efficient searching when it is balanced.

However, inserting elements in ascending or descending order can make the BST highly skewed. In the worst case, its height can become O(n).

## Why AVL Trees?

An AVL Tree is a self-balancing Binary Search Tree.

For every node:

**Balance Factor = Height(Left Subtree) - Height(Right Subtree)**

The allowed balance factors are:

- -1
- 0
- +1

When the tree becomes unbalanced, rotations are performed.

## AVL Rotations

The project implements the four standard rotation cases:

- LL → Right Rotation
- RR → Left Rotation
- LR → Left Rotation + Right Rotation
- RL → Right Rotation + Left Rotation

## Project Objectives

- Understand why AVL Trees are needed.
- Implement BST and AVL Trees in C.
- Implement AVL rotations.
- Compare BST and AVL tree heights.
- Compare insertion performance.
- Compare search operations.
- Study different insertion orders.
- Analyze limitations and alternatives.

## Experimental Setup

The experiments were implemented in **C** and executed using **GCC in Google Colab**.

Dataset sizes:

- 100
- 500
- 1,000
- 5,000
- 10,000
- 20,000

Three insertion orders were tested:

- Random
- Ascending
- Descending

The experiment measured:

- BST height
- AVL height
- BST insertion time
- AVL insertion time
- Search comparisons

## Experimental Results

For 20,000 ascending elements:

| Metric | BST | AVL |
|---|---:|---:|
| Height | 20,000 | 15 |
| Insertion Time (seconds) | 1.273368 | 0.009854 |

For 20,000 descending elements:

| Metric | BST | AVL |
|---|---:|---:|
| Height | 20,000 | 15 |
| Insertion Time (seconds) | 1.177447 | 0.009601 |

For 20,000 random elements:

| Metric | BST | AVL |
|---|---:|---:|
| Height | 34 | 17 |
| Insertion Time (seconds) | 0.005605 | 0.012647 |

### Key Finding

The experiments show that AVL Trees maintained a much smaller height than ordinary BSTs for all tested insertion orders.

The results also show that AVL is **not always faster during insertion**. Maintaining balance introduces additional rotation and height-update overhead.

The main advantage observed in this project is maintaining controlled tree height and efficient search behavior.

## Time Complexity

| Operation | BST Average | BST Worst Case | AVL |
|---|---:|---:|---:|
| Search | O(log n) | O(n) | O(log n) |
| Insertion | O(log n) | O(n) | O(log n) |
| Deletion | O(log n) | O(n) | O(log n) |

## Technologies Used

- C
- Data Structures and Algorithms
- GCC
- Google Colab
- Python
- Pandas
- Matplotlib
- GitHub

## Repository Contents

- `AVL_Trees_Fast_Searching_C.ipynb` – Complete Google Colab notebook containing the C implementation and experiments.
- Experimental datasets and results
- Graphs
- Project report
- Project presentation

## Limitations

- AVL Trees require additional height/balance information.
- Rotations introduce update overhead.
- AVL maintenance can make insertion slower for some random datasets.
- Other data structures may be more suitable depending on the application.

## Future Scope

- Compare AVL Trees with Red-Black Trees.
- Test larger datasets.
- Add AVL deletion experiments.
- Use more realistic datasets.
- Compare actual search execution time.
- Explore applications in databases and software systems.

## Conclusion

This project demonstrates how AVL Trees address the loss of balance that can occur in ordinary Binary Search Trees.

For 20,000 ascending elements, the BST reached a height of 20,000, while the AVL Tree maintained a height of 15.

The experiment therefore demonstrates the importance of self-balancing for maintaining efficient tree-based searching.

## Author

**Yericharla Spurthi**

B.Tech – Computer and Communication Engineering  
Amrita Vishwa Vidyapeetham

Roll No.: CH.EN.U4CCE25037

## Academic Project

This repository was created as part of a Capstone / Research Exploration project on Data Structures and Algorithms.
