# Calcium Ion Interaction Analysis and Visualization

## Overview

This repository contains two Jupyter notebooks designed for the analysis and visualization of calcium ion interactions in protein structures. The tools provided focus on parsing molecular structure data, identifying ligand and receptor interactions around calcium ions, and graphically representing these interactions in 3D space.

- `calcium.ipynb`: Provides core functions to load, process, and analyze PDB/PDBQT molecular structure files, extract calcium ion interactions with surrounding atoms, and quantify interaction counts.
- `calcium_graphing.ipynb`: Focuses on visualizing the interaction data through both static and interactive 3D plots, including scatter plots and interactive coordinate transformations.

## Features

### calcium.ipynb
- File decompression for molecular structure files.
- Distance, angle, and dihedral angle calculations between atoms.
- Parsing and handling of PDB and PDBQT formatted files to extract atom and coordinate information.
- Identification of nearby atoms around calcium ions using spatial cutoffs.
- Differentiation of ligand and receptor atom interactions with calcium based on amino acid codes.
- Batch processing of structure files to gather interaction information in tabular form.
- Export interaction counts to CSV for downstream analysis.

### calcium_graphing.ipynb
- Generation of 3D scatter plots to visualize calcium ion interactions (both ligand and receptor atoms).
- Static plots with Matplotlib and dynamic interactive plots using Plotly.
- Functions to align molecular coordinates for consistent orientation.
- Heatmaps to display interaction counts between ligand and receptor atoms.
- Utilities for reading interaction data from CSV files and plotting interaction distributions.

## Installation

Ensure Python 3 with the following packages installed:

- numpy
- pandas
- matplotlib
- seaborn
- plotly

Install via pip if needed: pip install numpy pandas matplotlib seaborn plotly


## Usage

1. Place molecular structure files (.pdb, .pdbqt, or gzipped variants) into appropriate folders.
2. Run `calcium.ipynb` to decompress files, parse structures, and generate a CSV summarizing calcium ion interactions.
3. Use `calcium_graphing.ipynb` to load the resulting data and generate visualizations, including static 3D scatter plots and interactive HTML plots.
4. Customize plotting functions to explore specific calcium interactions or datasets.

## Example Workflow

- Load and decompress molecular data.
- Identify ligand and receptor atoms interacting spatially around calcium ions.
- Aggregate interaction counts for statistical summaries.
- Plot 3D interaction geometry using custom visualization routines.
- Generate heatmaps to analyze ligand vs receptor interaction distributions.

## Data

- Input: Protein structure files (.pdb, .pdbqt) often compressed with gzip (.gz).
- Output: CSV files containing calcium ion identifiers, interaction coordinates, atom types, and interaction counts.
- Visualizations saved as PNG images or interactive HTML files.
