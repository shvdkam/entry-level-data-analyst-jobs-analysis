# 📊 Are Entry-Level Data Analyst Jobs Really Entry-Level?

## Project Overview

Many job postings are advertised as **Associate** or entry-level positions, but how accessible are they actually to candidates at the beginning of their careers?

This project analyzes Data Analyst job postings to explore whether advertised seniority levels reflect the actual requirements described by employers.

The analysis goes beyond basic exploratory analysis by extracting information from job descriptions and creating a custom **Entry-Level Friendliness Index (ELFI)** to estimate how accessible each vacancy appears to an early-career candidate.

---

## 🎯 Main Question

> **Are Data Analyst vacancies labelled as Associate genuinely entry-level?**

To explore this question, the analysis focuses on:

- required years of experience;
- number of requested technical skills;
- technical complexity of job requirements;
- differences between countries;
- differences between work arrangements;
- variation in entry-level accessibility across vacancies.

---

## 📂 Dataset

The original dataset contains **12,894 job postings** and includes information such as:

- job title;
- company;
- location;
- seniority level;
- work arrangement;
- job description;
- technical skills.

The dataset was cleaned and filtered to focus on relevant Data Analyst positions before performing the main analysis.

---

## 🔎 Analytical Workflow

The project follows a structured analytical process:

**Data Understanding → Data Cleaning → Filtering → EDA → Text Processing → Feature Engineering → ELFI → Comparison → Conclusions**

### 1. Data Understanding & Cleaning

The dataset was first inspected for:

- missing values;
- duplicated records;
- inconsistent text values;
- relevant Data Analyst job titles;
- seniority information.

The cleaned data was then prepared for exploratory analysis.

---

### 2. Exploratory Data Analysis

EDA was used to understand the structure of the Data Analyst job market represented in the dataset.

The analysis explores:

- distribution of job postings;
- Associate-level vacancies;
- employers;
- countries;
- work arrangements;
- experience requirements;
- technical skill expectations.

---

### 3. Text Processing & Feature Engineering

Job descriptions contain important information in unstructured text.

Using **Python and regular expressions**, I extracted and engineered analytical features including:

- years of experience;
- technical skill indicators;
- number of requested skills;
- selected indicators of technical complexity.

This transformed unstructured job descriptions into measurable variables that could be used for further analysis.

---

# 🧮 Entry-Level Friendliness Index (ELFI)

The main feature of the project is a custom **Entry-Level Friendliness Index (ELFI)**.

ELFI is designed to estimate how accessible each vacancy appears to an early-career candidate.

Each vacancy starts with a score of **100**.

The score is reduced based on detected entry barriers such as:

- explicit experience requirements;
- number of requested technical skills;
- selected indicators of technical complexity.

Higher scores indicate fewer detected entry barriers.

### Important

ELFI is a **heuristic analytical metric**, not an official recruitment standard.

It is designed for comparison within this dataset and should not be interpreted as a definitive measure of whether a candidate will qualify for a specific position.

---

## 📈 Key Findings

### Experience requirements

A large number of vacancies do not explicitly state the required years of experience.

However, among vacancies that do specify experience requirements, previous professional experience is frequently requested.

This suggests that the **Associate label alone does not necessarily guarantee that a vacancy is suitable for a candidate with no previous professional experience**.

---

### Entry-level accessibility varies considerably

ELFI scores show substantial variation between vacancies.

Some Associate positions contain relatively few detected barriers, while others combine stronger experience requirements with broader technical expectations.

This demonstrates that vacancies sharing the same advertised seniority level can differ significantly in their actual accessibility.

---

### Technical expectations matter

Experience is not the only potential barrier.

The number and type of requested technical skills can also make an Associate vacancy considerably more demanding for an early-career applicant.

This highlights the importance of analyzing the **complete job description rather than relying only on the advertised job level**.

---

### Country and work arrangement

Average ELFI scores were also compared across countries and work arrangements.

Differences appear between groups, although these results should be interpreted carefully because the number of vacancies is not equal across all countries and categories.

---

# 💡 Main Insight

The main conclusion of the project is:

> **“Associate” does not always mean truly entry-level.**

Job titles and seniority labels provide useful information, but they do not fully describe the barriers faced by early-career candidates.

Experience requirements, technical expectations, and the overall complexity of a vacancy should be considered together when evaluating how accessible a position really is.

---

## 🛠 Technologies & Skills

### Technologies

- **Python**
- **Pandas**
- **Matplotlib**
- **Regular Expressions**
- **Jupyter Notebook / Google Colab**

### Analytical Skills Demonstrated

- Data cleaning
- Exploratory Data Analysis
- Text processing
- Regular expressions
- Feature engineering
- Data aggregation
- Custom metric development
- Data visualization
- Analytical interpretation
- Communicating limitations
- Translating unstructured text into measurable features

---

## ⚠️ Limitations

Several limitations should be considered when interpreting the results:

- the dataset represents vacancies collected during a specific period;
- regular expressions may not detect every possible way employers describe experience requirements;
- ELFI is a heuristic metric rather than an official recruitment standard;
- the meaning of the Associate label may differ between companies and countries;
- job advertisements may not contain every requirement considered during the actual hiring process.

---

## 🚀 Future Improvements

Possible extensions of the project include:

- collecting a larger and more recent dataset;
- incorporating salary information;
- using Natural Language Processing instead of only rule-based text extraction;
- manually validating a sample of ELFI classifications;
- performing sensitivity analysis on ELFI scoring weights;
- developing an interactive dashboard based on the enriched dataset.

---

## 📁 Repository Structure

```text
entry-level-data-analyst-jobs-analysis/
│
├── README.md
├── Are_Entry_Level_Data_Analyst_Jobs_Really_Entry_Level.ipynb
└── LICENSE
```

---

## 📓 Full Analysis

The complete methodology, Python code, visualizations, ELFI calculations, results, and conclusions are available in:

**[`Are_Entry_Level_Data_Analyst_Jobs_Really_Entry_Level.ipynb`](Are_Entry_Level_Data_Analyst_Jobs_Really_Entry_Level.ipynb)**

---

## About This Project

This project was created as part of my **Data Analytics portfolio**.

My goal was not only to practice Python and exploratory data analysis, but also to take an ambiguous real-world question, transform unstructured data into measurable features, develop an analytical framework, and communicate the results together with their limitations.
