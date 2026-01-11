# Real-World Pandas Practice Datasets & Questions

This guide provides multiple real-world datasets with comprehensive practice questions to strengthen your pandas data wrangling skills.

---

## Dataset 1: Diamonds Dataset

### Loading the Dataset
```python
import pandas as pd

diamonds = pd.read_csv('https://raw.githubusercontent.com/mwaskom/seaborn-data/master/diamonds.csv')
print(diamonds.head())
```

### Dataset Description
The diamonds dataset contains price and attributes of ~54,000 diamonds. Perfect for beginners learning data analysis and visualization.

| Column | Description |
|--------|-------------|
| price | Price in USD ($326–$18,823) |
| carat | Weight of diamond (0.2–5.01) |
| cut | Quality (Fair, Good, Very Good, Premium, Ideal) |
| color | Color grade (J worst → D best) |
| clarity | Clarity (I1 worst → IF best) |
| x, y, z | Length, width, depth in mm |
| depth | Total depth percentage |
| table | Width of top relative to widest point |

### Practice Questions

#### Basic Exploration
1. Read the CSV and display the first 5 and last 5 rows
2. Find the shape (rows & columns) and data types of the dataset
3. Get summary statistics for all numeric columns
4. Display unique values in the 'cut' column and count their occurrences
5. Calculate the mean price of diamonds for each cut type

#### Data Filtering & Selection
6. Filter diamonds with carat weight ≥ 0.3
7. Find diamonds that are either "Premium" or "Ideal" cut
8. Select rows where length (x) > 5, width (y) > 5, and depth (z) > 5
9. Get all diamonds with color "D" and clarity "IF"
10. Find the top 10 most expensive diamonds and show their attributes

#### Data Manipulation
11. Create a new column 'volume' = x * y * z for each diamond
12. Add a price_per_carat column (price / carat)
13. Rename columns: 'x' → 'length', 'y' → 'width', 'z' → 'depth'
14. Sort the dataframe by price in descending order
15. Remove the 'depth' and 'table' columns

#### Aggregation & Grouping
16. Calculate count, min, max, and mean price for each cut
17. Find average price grouped by both cut and color
18. Calculate the mean carat weight for each clarity level
19. Create a cross-tabulation between cut and color
20. Find which combination of cut and clarity has the highest average price

#### Missing Values & Data Cleaning
21. Check for missing values in each column
22. Create a boolean dataframe showing True where values are missing
23. Drop rows with any missing values (if any exist)
24. Fill missing values in numeric columns with the mean

#### Advanced Operations
25. Calculate percentile (25th, 50th, 75th) of price by cut type
26. Find diamonds in the top 5% by price
27. Create a column categorizing price into: 'budget', 'mid-range', 'premium', 'luxury'
28. Use .apply() to create a quality_score = (carat * 2) + price_per_carat
29. Group by cut and find the variance in price for each group
30. Create a sample of 1000 random diamonds and calculate stats on the sample

---

## Dataset 2: Titanic Dataset

### Loading the Dataset
```python
titanic = pd.read_csv('https://raw.githubusercontent.com/mwaskom/seaborn-data/master/titanic.csv')
print(titanic.head())
```

### Dataset Description
Passenger data from the Titanic with survival information. Great for data wrangling with missing values and categorical data.

| Column | Description |
|--------|-------------|
| survived | Whether passenger survived (0=No, 1=Yes) |
| pclass | Ticket class (1, 2, or 3) |
| sex | Gender (male/female) |
| age | Age in years |
| sibsp | Number of siblings/spouses aboard |
| parch | Number of parents/children aboard |
| fare | Ticket fare |
| embarked | Port of embarkation (C, Q, S) |
| class | Ticket class (name) |
| who | Adult man/woman or child |
| adult_male | Whether passenger is adult male |
| deck | Deck letter |
| embark_town | Port name |
| alive | Whether survived (yes/no) |
| alone | Whether alone aboard |

### Practice Questions

#### Exploratory Analysis
1. Load the dataset and display basic info (.info(), .describe())
2. How many passengers were aboard? How many survived?
3. What percentage of passengers survived?
4. Count missing values in each column
5. What was the average age of passengers? (Handle missing values appropriately)

#### Data Cleaning
6. Drop rows with missing 'age' values
7. Fill missing 'embarked' values with the most common port
8. Handle missing values in 'deck' column (decide on strategy)
9. Identify and count duplicate rows
10. Create a clean version of the dataset with sensible missing value handling

#### Filtering & Categorization
11. Filter passengers who paid more than $100 for their ticket
12. Get all female passengers who survived
13. Find passengers in first class (pclass=1) who didn't survive
14. Create an age_group column: 'child' (0-12), 'teen' (13-19), 'adult' (20-65), 'senior' (65+)
15. Find all passengers traveling alone (sibsp=0 and parch=0)

#### Grouping & Aggregation
16. Group by sex and calculate survival rate
17. Group by pclass and find mean age and fare
18. Create a pivot table of pclass vs survived (count of passengers)
19. Find survival rate by age group
20. Calculate median fare for each combination of class and sex

#### Advanced Wrangling
21. Create a title column by extracting from passenger names (use .str operations)
22. Calculate total family size (sibsp + parch + 1)
23. Create a family_size_category: 'single', 'small', 'large'
24. Find which family groups had 100% survival rate
25. Use .apply() to create a risk_category based on multiple factors

#### Complex Questions
26. For each pclass, find the age range (min-max) of survivors vs non-survivors
27. Calculate the correlation between numeric features
28. Find passengers whose fares are outliers (beyond 3 standard deviations)
29. Create a survival probability score for each passenger group
30. Merge survival data with embarked_town to analyze by origin

---

## Dataset 3: Netflix Movies & TV Shows

### Loading the Dataset
```python
netflix = pd.read_csv('https://raw.githubusercontent.com/datasets/netflix-titles/master/data/netflix_titles.csv')
print(netflix.head())
```

### Dataset Description
Netflix content catalog with details about movies and TV shows.

| Column | Description |
|--------|-------------|
| show_id | Unique identifier |
| type | Movie or TV Show |
| title | Title of content |
| director | Director name(s) |
| cast | Cast member name(s) |
| country | Country of origin |
| date_added | Date added to Netflix |
| release_year | Year of release |
| rating | Content rating |
| duration | Duration (minutes for movies, seasons for shows) |
| listed_in | Genre(s) |
| description | Plot description |

### Practice Questions

#### Basic Exploration
1. How many movies vs TV shows are in the dataset?
2. What are the most common ratings for movies and shows separately?
3. Find the distribution of content by release year
4. List all unique genres
5. What year had the most content added?

#### Data Cleaning
6. Handle missing values in 'director', 'cast', and 'country' columns
7. Extract numeric duration values and create separate columns for movies and shows
8. Parse the 'date_added' column into datetime format
9. Find and handle any inconsistencies in the data
10. Create a clean subset with no missing values in critical columns

#### String Operations
11. Extract all director names and create a series of unique directors
12. Count how many titles have the word "Christmas" in them
13. Split the 'cast' column and find the most common actors
14. Extract the first listed genre for each show
15. Create a column indicating if the content is a documentary (based on listed_in)

#### Filtering & Categorization
16. Find all movies released after 2015
17. Get all content added in the last 5 years (from today's date)
18. Filter for movies with rating 'PG' or 'TV-Y'
19. Find TV shows with more than 5 seasons
20. Get all content from India

#### Grouping & Aggregation
21. Group by type and find average release year
22. Count content by country (note: multiple countries per row)
23. Find the most common rating for each content type
24. Calculate average number of actors per movie vs TV show
25. Find which director has the most content on Netflix

#### Advanced Analysis
26. Create a year_added column and analyze trend of additions over time
27. For each rating, calculate the number of movies vs shows
28. Find content that has been on Netflix the longest
29. Create a duration_category for movies: 'short' (<90 min), 'standard' (90-150), 'long' (>150)
30. Analyze the relationship between release_year and date_added

---

## Dataset 4: Employee HR Analytics

### Loading the Dataset
```python
# Dataset from seaborn or kaggle
employees = pd.read_csv('https://raw.githubusercontent.com/mwaskom/seaborn-data/master/penguins.csv')
# OR use a HR dataset from Kaggle
```

### Sample Dataset (Create your own or find one)
| Column | Description |
|--------|-------------|
| emp_id | Employee ID |
| name | Employee name |
| department | Department |
| salary | Annual salary |
| hire_date | Hiring date |
| performance_score | Performance rating |
| years_tenure | Years at company |
| left_company | Whether employee left |

### Practice Questions

#### Data Exploration
1. Total employees and basic demographics
2. Salary distribution by department
3. Average tenure and turnover rate
4. Department-wise employee count
5. Performance score statistics

#### Data Cleaning & Transformation
6. Handle any missing values in salary or performance_score
7. Convert hire_date to datetime format
8. Create a seniority_level column based on years_tenure
9. Identify and flag salary outliers
10. Create wage_grade categories (low, medium, high, executive)

#### Filtering & Selection
11. Find employees with salary > 100,000
12. Get employees who left with performance_score >= 4.0
13. Filter for employees in 'Sales' department hired in last 2 years
14. Find top 10 highest-paid employees by department
15. Identify employees with unusual salary/performance combinations

#### Grouping & Analysis
16. Average salary by department
17. Turnover rate by department and seniority level
18. Department-wise performance distribution
19. Correlation between tenure and performance score
20. Average salary by hire year

#### Advanced Operations
21. Calculate salary percentile for each employee within their department
22. Create a retention_risk_score based on tenure, performance, and salary
23. Find departments with highest turnover and analyze why
24. Calculate salary gap between entry-level and management
25. Identify top performers in each department (top 10%)

---

## Dataset 5: E-commerce Sales Data

### Sample Structure
```python
# You can find similar datasets on Kaggle or create sample data
# Columns: order_id, customer_id, product, category, price, quantity, 
#          order_date, shipping_cost, discount, region, payment_method
```

### Practice Questions

#### Sales Analysis
1. Total revenue and number of orders
2. Average order value
3. Top 10 best-selling products
4. Sales by category
5. Revenue by region

#### Temporal Analysis
6. Monthly revenue trend
7. Identify seasonal patterns
8. Compare sales across different days of the week
9. Customer acquisition trend over time
10. Identify peak shopping seasons

#### Customer Analysis
11. Repeat customer percentage
12. Average customer lifetime value
13. Customer segmentation by purchase frequency
14. Geographic analysis of customers
15. Payment method preferences

#### Data Wrangling
16. Calculate profit margin by product
17. Identify outlier transactions
18. Handle missing or invalid discount values
19. Create product_performance_tier (top, middle, bottom performers)
20. Analyze shipping costs vs order value correlation

---

## Tips for Practicing

1. **Start Simple**: Begin with basic exploration questions before moving to complex aggregations
2. **Use Documentation**: Reference pandas docs for unfamiliar operations
3. **Chain Operations**: Practice method chaining for cleaner code
4. **Experiment**: Don't just answer the question—try different approaches
5. **Visualize**: After analysis, create plots to visualize findings
6. **Performance**: For large datasets, compare performance of different methods

## Key Pandas Skills to Practice

- Reading/writing files (`.read_csv()`, `.to_csv()`)
- Data selection (`.loc[]`, `.iloc[]`, boolean indexing)
- Data cleaning (handling missing values, duplicates)
- String operations (`.str` accessor)
- DateTime operations (`.dt` accessor)
- Grouping and aggregation (`.groupby()`, `.agg()`)
- Merging/joining datasets
- Pivot tables and cross-tabulations
- Method chaining
- Custom functions with `.apply()`
- Memory optimization

---

## Resources for Further Learning

- W3Resource Pandas Exercises: Comprehensive exercise sets with solutions
- Kaggle Datasets: Thousands of real-world datasets with community discussions
- Real Python: In-depth pandas tutorials
- DataCamp: Interactive pandas courses
- GeeksforGeeks: Pandas problem solutions with explanations
