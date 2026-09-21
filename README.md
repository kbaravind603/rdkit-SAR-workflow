RDKit Chemoinformatics SAR Workflow

A small Python/RDKit workflow for analysing analogue libraries and combining molecular similarity with docking results for exploratory structure–activity relationship (SAR) analysis.

What the workflow does

Reads and validates molecular structures from SDF files

Calculates physicochemical descriptors including molecular weight, cLogP, TPSA, H-bond donors and acceptors

Generates Morgan fingerprints (radius 2, 2048 bits)

Calculates Tanimoto similarity to a selected reference compound

Integrates Glide XP docking scores using compound identifiers

Compares compound pairs and flags structurally similar analogues with notable differences in docking score

Exports compound-level results and flagged SAR pairs as CSV files

Tools

Python, RDKit, pandas

Input

The workflow requires:

An SDF file containing the compound library

A CSV file containing compound identifiers and Glide XP docking scores

Example input files are provided in example_data/.

Output

Results are written to SAR_results/:

compound_SAR_results.csv

flagged_SAR_pairs.csv

Example

The included example dataset demonstrates the complete workflow using a sample compound and corresponding docking score.

The SAR-pair output is empty for the example dataset because only one compound is included; pairwise SAR analysis requires multiple compounds.

Purpose

This project was developed to turn molecular descriptor, fingerprint and docking data into a simple reusable workflow for analysing analogue series during structure-based lead optimisation.
