# Arrow Puzzle — Solver and Generator

## Overview

Arrow Puzzle is a command-line puzzle generator and solver written in Python.

The puzzle consists of a grid containing directional arrows. The objective is to remove all arrows from the board by repeatedly removing arrows that can slide off the board in the direction they point without hitting another arrow.

This project includes:

- A puzzle generator that creates solvable boards
- A solver that finds the shortest sequence of valid removals
- A command-line interface for generating and solving puzzles
- Difficulty estimation based on solution length

---

## Puzzle Rules

Each cell in the grid contains either:

- An arrow (`^`, `v`, `<`, `>`)
- An empty space (`.`)

An arrow can be removed if:

1. It moves in the direction it points.
2. It reaches the edge of the board.
3. It does not collide with any other arrow along the path.

The goal is to remove all arrows from the board.

---

## Features

### Solver

The solver uses Breadth-First Search (BFS) to guarantee:

- The puzzle is solvable
- The solution found is the shortest possible sequence of moves

---

### Generator

The generator constructs puzzles using a reverse construction method:

1. Starts from an empty board
2. Places arrows that are immediately removable
3. Ensures that every generated board is solvable

This approach avoids inefficient random generation and rejection sampling.

---

### Difficulty Rating

Puzzle difficulty is defined as:

