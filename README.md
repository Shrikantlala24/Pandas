# Pandas Learning Lab

Hands-on notebooks, mini challenges, and reference material for mastering `pandas` from the ground up. The workspace mirrors a course-style journey: start with the foundational notebooks, move through the Kaggle exercises, then explore the practice files and datasets to cement the concepts.

## Repository Map

| Area | Purpose |
| --- | --- |
| `adding_column.ipynb`, `multi_df_concepts.ipynb`, `Series_summary.ipynb`, etc. | Short, topic-focused walkthroughs that introduce individual `pandas` patterns. |
| `practise_part_1.ipynb`, `group_by_.ipynb`, `asignment_real_analysis.ipynb` | Practice notebooks with progressively tougher prompts. |
| `Kaggle NBs/1_creating-reading-and-writing.ipynb` → `4_exercise-grouping-and-sorting.ipynb` | Adapted versions of Kaggle's *30 Days of Pandas* curriculum for structured drills. |
| `old file/` | Archive of legacy notebooks retained for reference; useful for seeing earlier approaches or alternative solutions. |
| `Files/matches.csv` | Sample dataset used across multiple notebooks; feel free to add more CSVs here. |
| [pandas-practice-datasets.md](pandas-practice-datasets.md) | Notes and links to additional public datasets to stretch your skills.

## Getting Started

1. **Install dependencies**
	```bash
	python -m venv .venv
	.venv\Scripts\activate  # PowerShell on Windows
	pip install pandas jupyterlab matplotlib seaborn
	```
2. **Launch Jupyter**
	```bash
	jupyter lab
	```
3. **Open a notebook** that matches the topic you are tackling. Most notebooks are self-contained and explain the dataset they rely on at the top.

## Suggested Learning Path

1. Warm up with the legacy notebooks under `old file/` to refresh the basics (Series, DataFrames, filtering).
2. Follow the Kaggle notebook sequence to build momentum with guided exercises.
3. Dive into the focused practice notebooks (e.g., `group_by_.ipynb`) and replicate the code without looking to test retention.
4. Use `Files/matches.csv` or datasets listed in [pandas-practice-datasets.md](./pandas-practice-datasets.md) to design your own mini-projects.


## Tips for Self-Review

- After finishing a notebook, rewrite the core transformations as reusable functions in a scratch notebook to check true understanding.
- Track questions or gotchas in `README.md` or a personal log so you can revisit them later.
- Pair each new concept with a real dataset (sports stats, finance, personal logs) to make the exercises memorable.

## Contributing / Extending

- Add new datasets to `Files/` and document them inside [pandas-practice-datasets.md](pandas-practice-datasets.md).
- Keep notebook names concise and descriptive (`10_window_functions.ipynb`).
- Prefer Markdown headings inside notebooks to explain the goal of each section before the code cell.

Happy exploring—feel free to iterate on the structure as your learning journey evolves!
