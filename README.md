## Project Veritas

An ML-powered system to evaluate the quality and relevancy of Google location reviews. The project uses modern NLP to detect spam, advertisements, and policy violations, improving the reliability of review platforms.

### Key ideas

- **Objective**: Identify low-quality or policy-violating reviews while preserving useful user feedback.
- **Approach**: Iterative, day-by-day workflow across data collection, feature engineering, model training, and evaluation.
- **Deliverables**: Cleaned/combined datasets, engineered features, trained models, and evaluation artifacts (e.g., confusion matrix).

---

## Repository structure

- **Day1 Setup, Data Collection, and Exploratory Data Analysis (EDA)**

  - Notebook: `TechJam_Day1_Data_Collection_and_Integration.ipynb`
  - Inputs: `Day1 .../assets/downloaded_files/`
  - Outputs: `Day1 .../assets/output/ucsd_delaware_reviews_combined.csv`
  - Visuals: `Day1 .../assets/png/*.png`

- **Day2 Feature Engineering and Initial Model Development**

  - Notebook: `TechJam_Day2_Feature_Engineering_and_Initial_Model_Development.ipynb`
  - Input: `Day2 .../assets/input/ucsd_delaware_reviews_combined.csv` (from Day 1)
  - Output: `Day2 .../assets/output/final_augmented_reviews_for_day3.csv`

- **Day3 Model Refinement, Evaluation, and Iteration**
  - Notebook: `TechJam_Day3_Model_Refinement_Evaluation_and_Iteration.ipynb`
  - Input: `Day3 .../assets/input/final_augmented_reviews_for_day3.csv` (from Day 2)
  - Visuals: `Day3 .../assets/png/confusion_matrix_final_optimized_model.png`

---

## Setup instructions

### Prerequisites

- macOS (or Linux/Windows with minor path changes)
- Python 3.12+
- Disk space for datasets and intermediate artifacts

### Option A: Use the provided virtual environment (fastest)

```bash
# From the project root
source venv/bin/activate
python --version
```

If activation succeeds and Python is available, you can proceed to the notebooks.

### Option B: Create your own virtual environment

```bash
python3 -m venv venv
source venv/bin/activate
python -m pip install --upgrade pip
# Install common dependencies used by the notebooks (adjust as needed)
pip install jupyter pandas numpy scikit-learn matplotlib seaborn nltk tqdm transformers datasets
```

### Launch Jupyter

```bash
jupyter lab
# or
jupyter notebook
```

---

## How to reproduce results

Run the notebooks sequentially; each day’s output feeds the next day’s input.

1. Day 1 — Data collection and EDA

- Open: `Day1 Setup, Data Collection, and Exploratory Data Analysis (EDA)/TechJam_Day1_Data_Collection_and_Integration.ipynb`
- Run all cells. Key outputs:
  - Combined dataset: `Day1 .../assets/output/ucsd_delaware_reviews_combined.csv`
  - EDA plots: `Day1 .../assets/png/*.png`

2. Day 2 — Feature engineering and initial modeling

- Open: `Day2 Feature Engineering and Initial Model Development/TechJam_Day2_Feature_Engineering_and_Initial_Model_Development.ipynb`
- Ensure the Day 1 combined CSV is available at: `Day2 .../assets/input/ucsd_delaware_reviews_combined.csv`
- Run all cells. Key output:
  - Augmented dataset for Day 3: `Day2 .../assets/output/final_augmented_reviews_for_day3.csv`

3. Day 3 — Model refinement, evaluation, and iteration

- Open: `Day3 Model Refinement, Evaluation, and Iteration/TechJam_Day3_Model_Refinement_Evaluation_and_Iteration.ipynb`
- Ensure the Day 2 augmented CSV is available at: `Day3 .../assets/input/final_augmented_reviews_for_day3.csv`
- Run all cells. Key outputs:
  - Trained/refined model artifacts (as defined in the notebook)
  - Evaluation plots, including: `Day3 .../assets/png/confusion_matrix_final_optimized_model.png`

### Notes

- If any cell installs packages, re-run the cell after environment activation.
- Paths are relative to their respective `Day*` directories; the notebooks already reference the correct input/output locations shown above.
- For fully deterministic runs, set random seeds in the notebooks where applicable.

---

## Team member contributions

| Name | Key contributions |
| ---- | ----------------- |
|      |                   |


---

## License

This project is licensed under the MIT License