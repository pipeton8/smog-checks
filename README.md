# smog-checks
*(c) Felipe del Canto (PUC-Chile)*

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/pipeton8/smog-checks/blob/main/SMOG_Checks.ipynb)

This script is designed to recognize matching brands and models of cars from a Chilean fleet database. Both models and brands are written differently in the base because of typos (i.e. NISSSAN instead of NISSAN), abbreviations (i.e. KIA instead of KIA MOTORS) or mispellings (i.e. SSANG YON instead of SSANGYONG).

The script implements a comparison between each pair of strings in each database, based on the Jaro distance (link). This metric was chosen since it is does not penalize typos and small misspellings as much as the Hamming distance; and is inmediatly normalized between 0 and 1 as opposed to other metrics.

The output of this script is a txt file containing replace commands for the Stata statistical software. The goal is to make brand and model strings uniform throughout the database.

