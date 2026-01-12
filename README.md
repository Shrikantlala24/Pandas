# 🐼 Pandas Learning Lab

Notebook-first practice repo for learning **pandas** (with a little plotting + EDA along the way). The structure is intentionally “course-like”: start from fundamentals, follow the Kaggle drill sequence, then apply concepts in practice notebooks.

## 🔎 At a glance

- ✅ **Beginner → intermediate path** (Series/DataFrame → filtering → groupby → merge/concat)
- 🧩 **Topic notebooks** for quick concepts + repetition
- 📁 **One shared dataset folder** (`Files/`) to keep data organized
- 🗃️ **Legacy notebooks** preserved for revision

## 🧭 Contents

- [Quick Start](#-quick-start)
- [Repository Map](#-repository-map)
- [Suggested Learning Path](#-suggested-learning-path)
- [Datasets](#-datasets)
- [Notes](#-notes)

## 🚀 Quick Start

1. **Create + activate a virtual environment (Windows / PowerShell)**
	```bash
	python -m venv .venv
	.venv\Scripts\activate
	```
2. **Install what you need**
	```bash
	pip install pandas jupyterlab matplotlib seaborn
	```
3. **Open notebooks**
	```bash
	jupyter lab
	```

Tip: If you're using VS Code, install the **Python** and **Jupyter** extensions and open `.ipynb` files directly.

## 🗺️ Repository Map

### 📌 Main notebook (root)

- [`✨group_by_.ipynb`](%E2%9C%A8group_by_.ipynb) — focused practice on grouping/aggregation patterns.

### 🧠 Fundamentals & revision (legacy)

Folder: [`old file/`](old%20file/)

- `1_Intro_to_Pandas.ipynb`
- `2_funcs and attrs.ipynb`
- `3_fetch r and c.ipynb`
- `4_filter + value count.ipynb`
- `5_series.ipynb`
- `6_Killer✨functions.ipynb`
- `7_Plotting graphs.ipynb`
- `8_isin_function.ipynb`
- `9_merge_function.ipynb`

### 🏋️ Kaggle-style drills

Folder: [`Kaggle NBs/`](Kaggle%20NBs/)

- `1_creating-reading-and-writing.ipynb`
- `2_indexing-selecting-assigning.ipynb`
- `3_summary-functions-and-maps.ipynb`
- `4_exercise-grouping-and-sorting.ipynb`

### 🧪 Practice notebooks (extra)

Folder: [`perfect_practise_notebooks/`](perfect_practise_notebooks/)

- `Diamonds_practise.ipynb`
- `merge_concat.ipynb`
- `Titanic_Pandas_Practice.ipynb`
- [`practice-datasets.md`](perfect_practise_notebooks/practice-datasets.md) — dataset ideas/links for more practice

### 🧺 Additional notebooks (optional)

Folder: [`not neccessary/`](not%20neccessary/)

- `adding_column.ipynb`
- `asignment_real_analysis.ipynb`
- `diamonds_trial.ipynb`
- `hello.ipynb`
- `Series_summary.ipynb`

## 🧭 Suggested Learning Path

1. **Start with** [`old file/`](old%20file/) to build comfort with Series/DataFrames, filtering, and basic plotting.
2. **Move to** [`Kaggle NBs/`](Kaggle%20NBs/) for structured exercises and repetition.
3. **Practice deeply** with [`✨group_by_.ipynb`](%E2%9C%A8group_by_.ipynb) (groupby + aggregation is a core skill).
4. **Level up** in [`perfect_practise_notebooks/`](perfect_practise_notebooks/) (joins, concat, and full workflows).
5. **Optional**: skim [`not neccessary/`](not%20neccessary/) for quick topic refreshers.

## 📦 Datasets

- Folder: [`Files/`](Files/)
- Current dataset: `matches.csv`

Suggestion: keep raw datasets in `Files/` and reference them via relative paths (e.g., `Files/matches.csv`) so notebooks run consistently.

## 📝 Notes

- If a notebook fails due to missing files, check whether it expects a dataset under `Files/` and update the path.
- Best self-check: redo a notebook section from memory, then compare outputs.

Happy learning — small daily practice beats occasional marathons. 🧭
