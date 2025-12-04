# COMP 331 Final Project – Adult Income Data Quality & Bias

## Project Overview
In this project, I am analyzing a well-documented dataset known as the 'Adult Income' dataset, which is a curated selection of data from the original U.S. Census Bureau in 1994. It has become widely used as a benchmark for machine learning when studying classification, fairness, and predictive bias in data. The data wasn't initially collected for machine learning, so it has many of the hallmarks of real world data, including missing values, skewed distributions, and social inequalities encoded into the data. This project seeks to examine the quality and potential biases found in this dataset to show how these factors can influence the fairness and performance of a regression model that seeks to predict whether an individual from the dataset will make more than 50K per year.

---

## Dataset Source
Adult Income Dataset (UCI Machine Learning Repository):  
https://archive.ics.uci.edu/ml/datasets/adult

**Citation (APA):**  
Kohavi, R. (1996). *Adult Data Set*. UCI Machine Learning Repository. https://archive.ics.uci.edu/ml/datasets/adult

---

## Repository Structure

- `data/` – Raw UCI Adult dataset (`adult.data`, `adult.test`) and any cleaned versions. Note: Adult.test was not used in this project.
- `notebooks/`
  - `01_initial_profiling.ipynb` – basic profiling and data quality checks.
  - `02_dq_summary.ipynb` – summarized DQ findings and notes for the report.
  - `03_model_and_fairness.ipynb` – logistic regression model, performance, and fairness metrics.
- `results/` – exported tables / figures used in the report and slides.
- `src/` – any helper Python scripts (if I decide to add any).
- `requirements.txt` – python dependencies listed here for easy install
- `report/` – draft/final project report files.
  
## Environment & Dependencies

Project was run with:

- Python 3.x  
- `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `jupyter`
- Dependencies can be easily installed using the included requirements.txt 
  pip install -r requirements.txt


## How to Run

1. Open a terminal, clone the repository and enter the repository
```bash
git clone https://github.com/pumpkinguy31/COMP331-Final-Project-AdultIncome.git
cd COMP331-Final-Project-AdultIncome
```

2. Create and activate a Python virtual environment:

```bash
python -m venv venv
```
# If using Windows:
```bash
.\venv\Scripts\Activate.ps1
```
# If using macOS/Linux:
```bash
source venv/bin/activate
```
3. Install required packages:
```bash
pip install -r requirements.txt
```

4. Launch Jupyter notebook from a terminal
```bash
jupyter notebook
```
This will open the Jupyter interface in your web browser.

5. Navigate to the analysis notebooks in the notebooks/ folder. You should see:
notebooks/
 ├── 01_initial_profiling.ipynb
 ├── 02_data_cleaning_and_checks.ipynb
 └── 03_model_and_bias_analysis.ipynb

6. Open each notebook in order and 'restart and run all' to execute the cells:

    01_initial_profiling.ipynb
        -Loads the Adult Income dataset
        -Shows overall structure, missing values, and basic summary statistics

    02_data_cleaning_and_checks.ipynb
        -Cleans missing/invalid values
        -Performs deeper data quality checks (completeness, consistency, uniqueness)
        -Computes frequency tables and cross-tabs

    03_model_and_bias_analysis.ipynb
        -Uses one-hot encoding for the variety of categorical data columns
        -Trains a logistic regression model
        -Produces accuracy, confusion matrix, and classification report
        -Runs fairness/bias comparisons (sex, race)
        -Tests versions of the model with and without sensitive attributes 

7. Read the final report if you'd like in the report/ folder.
