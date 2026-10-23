# Personalized TED Talks Recommendation System Using Machine Learning

## Overview

The **Personalized TED Talks Recommendation System** is a machine learning project that aims to recommend relevant TED Talks based on their content and similarity to a talk selected by the user.

The project uses TED Talk metadata and transcripts to prepare textual information for a content-based recommendation system.

## Objectives

- Collect and understand TED Talk metadata and transcript data.
- Explore data quality, missing values, duplicates, and transcript coverage.
- Clean and combine relevant text fields.
- Convert textual information into numerical features using TF-IDF.
- Build a content-based recommendation engine using similarity scores.
- Evaluate the recommendation system using an appropriate evaluation strategy.

## Technology Stack

- **Language:** Python
- **Development Environment:** Visual Studio Code and Jupyter Notebook
- **Data Processing:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Version Control:** Git and GitHub

## Dataset

The project uses two TED Talk datasets:

- `ted_main.csv` — TED Talk metadata, including titles, speakers, descriptions, tags, and other attributes.
- `transcripts.csv` — TED Talk transcripts associated with their URLs.

The metadata dataset contains 2,550 talks. After duplicate transcript records were removed, 2,464 unique transcript records remained. The datasets were merged using normalized URLs, preserving all 2,550 metadata records.

**Dataset note:** The original datasets are not included in this repository. Obtain them from their original source and ensure that the applicable license and terms permit your intended use.

## Project Structure

```text
Personalized_TED_Talks_Recommendation_System/
├── data/
│   ├── raw/                 # Original datasets
│   └── processed/           # Prepared datasets
├── notebooks/
│   └── 01_eda_and_preprocessing.ipynb
├── src/                     # Reusable Python modules
├── models/                  # Saved model artifacts
├── reports/                 # Analysis and evaluation reports
├── .gitignore
├── requirements.txt
└── README.md
```

## Current Progress

### Module 1: Data Collection
- Loaded TED Talk metadata and transcript datasets.
- Inspected dataset structure and columns.

### Module 2: Exploratory Data Analysis and Preprocessing
- Examined missing values, duplicate URLs, numerical statistics, and transcript coverage.
- Removed duplicate transcript records after confirming identical transcript text.
- Merged metadata and transcripts using normalized URLs.
- Handled missing text values in the modeling dataset.
- Created a `combined_text` field using titles, descriptions, tags, and transcripts.
- Saved the prepared dataset as `data/processed/ted_processed.csv`.

### Planned Modules
- **Module 3:** Feature Engineering and TF-IDF Vectorization
- **Module 4:** Content-Based Recommendation Engine
- **Module 5:** Recommendation Evaluation

The recommendation engine and evaluation stages are still under development.

## Getting Started

### 1. Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd Personalized_TED_Talks_Recommendation_System
```

### 2. Create and activate a virtual environment

On Windows PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 4. Prepare the datasets

Place the source files in `data/raw/`:

- `ted_main.csv`
- `transcripts.csv`

Ensure that you have permission to use the datasets under their applicable terms.

### 5. Run the notebook

Open `notebooks/01_eda_and_preprocessing.ipynb` in VS Code and execute the cells in order.

If required, adjust relative file paths to match your notebook's working directory.

## Expected Outcome

The intended outcome is a content-based recommendation system that identifies TED Talks with similar textual content and recommends relevant talks to users.

## Project Status

**Current stage:** Data collection, exploratory data analysis, and preprocessing completed; TF-IDF vectorization and recommendation development are upcoming.

