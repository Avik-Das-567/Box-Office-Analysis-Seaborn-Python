# Analyze Box Office Data with Seaborn and Python

This project performs **exploratory data analysis (EDA)** on the TMDB Box Office dataset using Python. The goal is to uncover relationships between movie metadata (such as budget, language, and text-based features) and **box office revenue**.

The project combines **statistical visualization**, **feature engineering**, and **text analysis** to transform raw movie data into meaningful insights. It highlights how financial, linguistic, and textual attributes influence movie revenue, demonstrating how data transformations reveal patterns in real-world datasets.

## Dataset
**Files:**
- **`train.csv`** → Training dataset with revenue labels
- **`test.csv`** → Test dataset for prediction tasks

**Source:** TMDB Box Office Prediction Dataset (Kaggle)

**Link:** https://www.kaggle.com/c/tmdb-box-office-prediction/data

**Size:** ~7400 movies

**Features include:**
- Budget
- Revenue (target variable)
- Original language
- Movie titles and descriptions
- Homepage presence
- Release and production metadata

The dataset is approached as a **regression problem**, where the objective is to understand and eventually predict movie revenue.

## Project Workflow

### Task 1: Data Loading and Exploration
- Imported essential libraries (`numpy`, `pandas`, `seaborn`, `matplotlib`)
- Loaded datasets using pandas
- Inspected dataset structure and previewed initial records
- Identified key variables and data characteristics

### Task 2: Visualizing the Target Distribution
- Plotted **revenue distribution** using Seaborn
- Observed heavy right-skew in revenue data
- Applied **log transformation** (`np.log1p`) to normalize the distribution
- Compared raw vs transformed distributions

### Task 3: Budget vs Revenue Analysis
- Visualized **budget distribution**
- Applied log transformation to budget and revenue
- Created scatter plots to analyze:
  - Relationship between budget and revenue
  - Impact of scaling on interpretability
- Observed clearer linear trends after transformation

### Task 4: Impact of Official Homepages
- Engineered a binary feature indicating homepage presence
- Used categorical plots to compare:
  - Movies **with homepage**
  - Movies **without homepage**
- Analyzed how online presence correlates with revenue

### Task 5: Language-Based Revenue Distribution
- Examined distribution of movie revenues across languages
- Used **box plots** for comparison
- Tested the assumption that English-language films dominate revenue
- Identified variations and outliers across different languages

### Task 6: Text Analysis with Word Clouds
- Extracted textual features:
  - Movie titles
  - Movie descriptions
- Generated **word clouds** to visualize:
  - Frequently occurring words
  - Dominant themes in high-revenue films
- Provided intuitive understanding of textual trends

### Task 7: Text Features and Revenue Prediction
- Performed:
  - Tokenization
  - Vectorization (text → numerical features)
- Trained a **linear regression model** on text data
- Used **ELI5** to:
  - Interpret model coefficients
  - Identify words with the strongest impact on revenue
- Highlighted key terms contributing positively/negatively to predictions

## Key Insights
- Revenue distribution is **highly skewed**, requiring log transformation for analysis.
- Budget shows a **positive correlation** with revenue after scaling.
- Movies with official homepages tend to have **higher median revenues**.
- Language influences revenue distribution, but not always as expected.
- Certain keywords in titles/descriptions have **measurable predictive power**.

## Tech Stack
- **Python**
- **NumPy** – numerical computations
- **pandas** – data manipulation and analysis
- **Seaborn** – statistical data visualization
- **matplotlib** – plotting and figure control
- **scikit-learn** – modeling and feature processing
- **ELI5** – model interpretability
- **WordCloud** – text visualization

## What This Project Demonstrates
- Performing end-to-end exploratory data analysis on real-world datasets.
- Handling skewed distributions using log transformations.
- Engineering features from both structured and unstructured (text) data.
- Applying text vectorization techniques for regression modeling.
- Interpreting model outputs using ELI5.
