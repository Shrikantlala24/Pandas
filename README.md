# 🐼 Pandas Learning Lab

Hands-on notebooks, curated drills, and dataset references for mastering `pandas` from the ground up. Start with the foundations, layer in Kaggle-style exercises, then stress-test yourself with practice notebooks and custom datasets.

## ✨ Highlights

- 📚 **Guided journey** from introductory Series/DataFrame concepts to advanced grouping and merging.
- 🧪 **Practice-first mindset** via topic notebooks (`adding_column.ipynb`, `group_by_.ipynb`, `Titanic_Pandas_Practice.ipynb`).
- 📂 **Curated datasets** under `Files/` plus inspiration in [perfect_practise_notebooks/practice-datasets.md](perfect_practise_notebooks/practice-datasets.md).
- 🔁 **Legacy archive** in `old file/` for reviewing earlier approaches and alternate solutions.

## 🗂️ Repository Layout

| Area | What's inside |
| --- | --- |
| Root notebooks | Bite-sized explorations such as `adding_column.ipynb`, `multi_df_concepts.ipynb`, `Series_summary.ipynb`, `group_by_.ipynb`, and `Titanic_Pandas_Practice.ipynb`. |
| `Kaggle NBs/` | Adapted notebooks from Kaggle's *30 Days of Pandas* (`1_creating-reading-and-writing.ipynb` → `4_exercise-grouping-and-sorting.ipynb`). |
| `perfect_practise_notebooks/` | Deeper dives like `Diamonds_practise.ipynb`, `merge_concat.ipynb`, plus supporting notes in `practice-datasets.md`. |
| `old file/` | Legacy series covering fundamentals (`1_Intro_to_Pandas.ipynb` through `9_merge_function.ipynb`). |
| `Files/` | Reusable CSV assets (currently `matches.csv`). Add more data sources here as you expand the lab. |

## 🚀 Quick Start

1. **Create a virtual environment**
	```bash
	python -m venv .venv
	.venv\Scripts\activate  # PowerShell on Windows
	```
2. **Install the essentials**
	```bash
	pip install pandas jupyterlab matplotlib seaborn
	```
3. **Launch Jupyter Lab**
	```bash
	jupyter lab
	```
4. **Open a notebook** that matches your current focus, skim the intro Markdown, then run cells top-to-bottom.

## 🧭 Suggested Learning Flow

1. **Refresh fundamentals** in `old file/` to revisit Series, DataFrames, indexing, and plotting.
2. **Build structured habits** with the sequential `Kaggle NBs/` exercises.
3. **Apply concepts deliberately** using the focused root notebooks (`group_by_.ipynb`, `multi_df_concepts.ipynb`).
4. **Take on mini-projects** inside `perfect_practise_notebooks/`, referencing the dataset ideas list for inspiration.
5. **Design your own drills**: copy `Files/matches.csv` or bring in new CSVs to recreate transformations from memory.

## 🧱 Practice & Self-Review

- Re-implement core transforms from each notebook in a scratch pad without peeking to prove retention.
- Summarize takeaways or open questions in a personal log so patterns and pitfalls stay top-of-mind.
- Challenge yourself to generalize repetitive logic into helper functions or reusable snippets.

## 🤝 Contributing & Extending

- Log every new dataset inside [perfect_practise_notebooks/practice-datasets.md](perfect_practise_notebooks/practice-datasets.md) for future reference.
- Keep notebook titles descriptive yet concise (`06_groupby_windows.ipynb`).
- Use Markdown headings and short commentary cells to explain intent before complex transformations.

Happy exploring, and keep iterating on the lab as your pandas fluency grows! 🧭
