# Board Game Analysis Project

## Overview

This project analyzes board game data from the Board Games Geek dataset to identify trends and correlations in game popularity, complexity, and ratings. It includes data preprocessing, quality checking, and analysis scripts written in Bash.

## Scripts

### `empty_cells`

Checks data quality by counting empty cells in each column of the dataset.

```bash
./empty_cells <input_file> <separator>
```

*Example:*
```bash
./empty_cells bgg_dataset.txt ";"
```

### `preprocess`

Cleans the input data by:

- Converting semicolon separators to tab characters
- Standardizing line endings to Unix format
- Converting decimal commas to decimal points
- Removing non-ASCII characters
- Generating unique IDs for entries missing them

```bash
./preprocess <input_file>
```

*Example:*
```bash
./preprocess bgg_dataset.txt
```

### `analysis`

Analyzes the cleaned data to answer research questions:

- Identifies the most popular game mechanics and domains
- Calculates correlation between publication year and average rating
- Calculates correlation between game complexity and average rating

```bash
./analysis <input_file>
```

*Example:*
```bash
./analysis bgg_dataset.tsv
```

## Data

The project is designed to work with the Board Games Geek dataset, which contains information about 20,000+ board games including ratings, complexity, mechanics, and domains.

## Sample Output

When analysis is run on the cleaned input file `sample.tsv`:

```bash
./analysis sample.tsv
```

The output is:

```
The most popular game mechanics is Hand Management found in 48 games
The most game domain is Strategy Games found in 77 games

The correlation between the year of publication and the average rating is 0.226
The correlation between the complexity of a game and its average rating is 0.426
```

## Requirements

- Bash shell
- Standard Unix utilities: `awk`, `tr`, `sort`, `cut`, etc.

## Notes

To run the scripts, ensure you have the necessary permissions. You can set executable permissions using:

```bash
chmod u+x empty_cells preprocess analysis
```

## Author

Tyrone Tran  
Student ID: 24814799  
CITS4407: Open Source Tools and Scripting  
Assignment 2, May 2025

---

*This project was developed as part of CITS4407 at UWA. For any questions or feedback, please contact the author.*
