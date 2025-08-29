# 🔍 Project Veritas

An ML-powered system to evaluate the quality and relevancy of Google location reviews. Project Veritas uses modern Natural Language Processing (NLP) techniques to detect spam, advertisements, and policy violations, improving the reliability of review platforms.

## ✨ Project Overview

### 🎯 Objective
Identify low-quality or policy-violating reviews while preserving useful user feedback to enhance the trustworthiness of online review platforms.

### 🛠️ Approach
Our solution follows an iterative, day-by-day workflow across:
- 📊 Data collection and integration from multiple sources
- 📈 Comprehensive exploratory data analysis (EDA)
- 🧩 Feature engineering to extract relevant signals
- 🤖 Model development using state-of-the-art NLP techniques
- 📝 Rigorous model evaluation and optimization

### 🌟 Key Features
- 🔄 Multi-source data integration (UCSD and Delaware datasets)
- 📚 Linguistic feature extraction and sentiment analysis
- 🚫 Detection of spam patterns and policy violations
- ✅ Preservation of genuine user feedback

## 📂 Repository Structure

- **Day1: Setup, Data Collection, and Exploratory Data Analysis (EDA)**
  - Notebook: `TechJam_Day1_Data_Collection_and_Integration.ipynb`
  - Inputs: `Day1 .../assets/downloaded_files/` (meta-Delaware.json.gz, review-Delaware_10.json.gz, reviews.csv)
  - Outputs: `Day1 .../assets/output/ucsd_delaware_reviews_combined.csv`
  - Visuals: `Day1 .../assets/png/*.png`

- **Day2: Feature Engineering and Initial Model Development**
  - Notebook: `TechJam_Day2_Feature_Engineering_and_Initial_Model_Development.ipynb`
  - Input: `Day2 .../assets/input/ucsd_delaware_reviews_combined.csv` (from Day 1)
  - Output: `Day2 .../assets/output/final_augmented_reviews_for_day3.csv`

- **Day3: Model Refinement, Evaluation, and Iteration**
  - Notebook: `TechJam_Day3_Model_Refinement_Evaluation_and_Iteration.ipynb`
  - Input: `Day3 .../assets/input/final_augmented_reviews_for_day3.csv` (from Day 2)
  - Visuals: `Day3 .../assets/png/confusion_matrix_final_optimized_model.png`

## 🚀 Setup Instructions

### 📋 Prerequisites
- Python 3.12+
- 4GB+ free disk space for datasets and intermediate artifacts
- Compatible with macOS, Linux, and Windows (with minor path adjustments)

### 🔧 Environment Setup

#### Option A: Use the provided virtual environment (fastest)
```bash
# From the project root
source venv/bin/activate  # On Windows: venv\Scripts\activate
python --version  # Verify Python activation
```

If activation succeeds and Python is available, proceed to the notebooks.

#### Option B: Create your own virtual environment
```bash
# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Update pip and install dependencies
python -m pip install --upgrade pip
pip install jupyter pandas numpy scikit-learn matplotlib seaborn nltk tqdm transformers datasets torch
```

### 🖥️ Launch Jupyter
```bash
jupyter lab
# or
jupyter notebook
```

## 🔁 How to Reproduce Results

Follow these steps to reproduce our results by running the notebooks sequentially:

### 1️⃣ Day 1 — Data Collection and EDA
- Open: `Day1 Setup, Data Collection, and Exploratory Data Analysis (EDA)/TechJam_Day1_Data_Collection_and_Integration.ipynb`
- Run all cells to:
  - Load and preprocess the UCSD and Delaware datasets
  - Perform data cleaning and integration
  - Conduct exploratory data analysis with visualizations
  - Generate the combined dataset: `Day1 .../assets/output/ucsd_delaware_reviews_combined.csv`
  - Create EDA plots: `Day1 .../assets/png/*.png`

### 2️⃣ Day 2 — Feature Engineering and Initial Modeling
- Open: `Day2 Feature Engineering and Initial Model Development/TechJam_Day2_Feature_Engineering_and_Initial_Model_Development.ipynb`
- Ensure the Day 1 combined CSV is available at: `Day2 .../assets/input/ucsd_delaware_reviews_combined.csv`
- Run all cells to:
  - Extract linguistic features from review text
  - Perform feature selection and transformation
  - Develop initial classification models
  - Generate the augmented dataset: `Day2 .../assets/output/final_augmented_reviews_for_day3.csv`

### 3️⃣ Day 3 — Model Refinement and Evaluation
- Open: `Day3 Model Refinement, Evaluation, and Iteration/TechJam_Day3_Model_Refinement_Evaluation_and_Iteration.ipynb`
- Ensure the Day 2 augmented CSV is available at: `Day3 .../assets/input/final_augmented_reviews_for_day3.csv`
- Run all cells to:
  - Fine-tune model hyperparameters
  - Evaluate model performance with various metrics
  - Generate evaluation visualizations: `Day3 .../assets/png/confusion_matrix_final_optimized_model.png`

### 💡 Tips for Successful Reproduction
- If any cell installs packages, restart the kernel after installation
- Set random seeds when prompted for reproducibility (default seeds are provided)
- For large datasets, ensure sufficient memory is available
- All paths in notebooks are relative to their respective directories

## 👥 Team Members

- Nguyen Tran Thanh Lam
- Pham Hong Phuc
- Pham Tran Tuan Minh
- Dinh Quang Anh
- Nguyen Le Tam

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.