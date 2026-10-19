# Day 0: Setup

## Done
- Enabled virtualization and installed WSL2 with Ubuntu (fixed error 0x80370114 and a DNS problem on the way)
- Installed Git, set up an SSH key, and linked my laptop to GitHub
- Created the bioinformatics-journey repo, README, and folders
- Installed Miniconda, added the conda-forge and bioconda channels, and created the bioinfo environment (Python 3.12)
- Installed VS Code with the WSL, Python, and Jupyter extensions
- Created accounts: GitHub, NCBI, Galaxy, Rosalind, Colab

## Problems and fixes
- WSL error 0x80370114: Windows features needed enabling and a full restart
- "Could not be resolved" when installing Ubuntu: network DNS problem, fixed by switching the DNS
- Terminal opened in /mnt/c/...: fixed with `cd ~`

## What I learned
- Most bioinformatics tools are built for Linux, so I installed WSL to run Linux inside Windows. Git saves snapshots of my files on my laptop, and GitHub is the online copy. A conda environment is a separate workspace, so installing one tool can’t break another.

## Next
- Week 1: Linux basics (Linux Journey), molecular biology refresher (Khan Academy)
