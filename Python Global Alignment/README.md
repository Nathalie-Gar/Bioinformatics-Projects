# Needleman–Wunsch Global Alignment
A Python implementation of the classic global sequence alignment algorithm with configurable match, mismatch, and gap scores.

## Background
Needleman–Wunsch is a foundational dynamic-programming algorithm used in bioinformatics to find the optimal end-to-end alignment between two biological sequences. This implementation was created as both a learning exercise and a lightweight, reusable script for small-to-medium-scale alignments.

## Features
- Customizable scoring: match score, mismatch penalty, and gap penalty
- Dynamic-programming matrix construction with O(n·m) time
- Traceback to reconstruct the optimal alignment
- Command-line interface accepting raw sequences or FASTA files
- Unit tests covering edge cases (all gaps, identical sequences, etc.)

## Prerequisites
- Python 3.7 or higher
- [NumPy](https://numpy.org/) (for matrix handling)
- (Optional) pytest for running unit tests
