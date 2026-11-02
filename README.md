# Are Entry-Level Data Analyst Jobs Really Entry-Level? | Python

**"Associate" barely means easier. Associate data analyst postings score 88.3 on my entry-level index, Mid senior postings 84.9. 30% of Associate postings ask for 3+ years of experience, and 19% have "Senior" or "Lead" in the title.**

I was looking for my first analyst job myself and kept seeing "Associate" roles that asked for years of experience. So I tested it on real job postings.

[Open the notebook in Colab](https://colab.research.google.com/github/shvdkam/entry-level-data-analyst-jobs-analysis/blob/main/Are_Entry_Level_Data_Analyst_Jobs_Really_Entry_Level_.ipynb)

## Data

- 12,894 LinkedIn job postings for analyst roles in the US, UK, Canada and Australia, all collected on 20 December 2023, 11 columns (title, company, location, job level, work type, job description, skills)
- After cleaning: 12,851 postings (43 without a job description removed, no duplicates)
- After filtering by title (data analyst, BI analyst, reporting analyst and similar) and removing 7 unpaid volunteer roles: **3,473 analyst postings**, of which **685 are labelled Associate**

## What I did

1. **Cleaned and filtered** the data in Pandas.
2. **Extracted features
