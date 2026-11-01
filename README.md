# Are Entry-Level Data Analyst Jobs Really Entry-Level? | Python

**"Associate" barely means easier. Associate data analyst vacancies scored 86.3 on my entry-level index, almost the same as all analyst vacancies together (84.0).**

I was looking for my first analyst job myself and kept seeing "Associate" roles that asked for years of experience. So I tested it on real job postings.

[Open the notebook in Colab](https://colab.research.google.com/github/shvdkam/entry-level-data-analyst-jobs-analysis/blob/main/Are_Entry_Level_Data_Analyst_Jobs_Really_Entry_Level.ipynb)

## Data

- 12,894 job postings, 11 columns (title, company, location, job level, work type, job summary, skills)
- After cleaning: 12,851 postings (43 without a job description removed, no duplicates)
- After filtering by title (data analyst, BI analyst, reporting analyst and similar): **3,480 analyst postings**, of which **692 are labelled Associate**

## What I did

1. **Cleaned and filtered** the data in Pandas.
2. **Extracted features from text with regular expressions:** years of experience and 11 technical skills (SQL, Python, Excel, Tableau, Power BI, statistics, ETL and others).
3. **Built the Entry-Level Friendliness Index (ELFI).** Each vacancy starts at 100 points and loses points for:
   - required experience (1 year: -8, 2 years: -15, 3+ years: -25)
   - more than 5 requested skills (-2 for each extra skill)
   - advanced requirements (Python -2, statistics -2, ETL -3)
4. **Compared ELFI** by job level, country and work arrangement.

## Key findings

**1. Most postings that mention experience ask for 2+ years.** 37% of analyst postings don't state any experience number. Of those that do, 92% ask for 2 years or more, and 5 years is the most common single value (608 postings).

**2. The Associate label changes little.** Associate postings average 86.3 ELFI vs 84.0 for all analyst postings. Scores range from 62 to 100, so some Associate jobs are truly open to beginners and some are not.

**3. Country differences are small, the UK scores highest.**

| Country | Associate postings | Average ELFI |
|---|---:|---:|
| United Kingdom | 81 | 90.6 |
| Australia | 25 | 86.2 |
| United States | 558 | 85.8 |
| Canada | 28 | 83.6 |

**4. Work arrangement hardly matters.** Onsite 87.3, remote 86.0, hybrid 85.3.

## What this means for a job seeker

Don't filter by the "Associate" label alone. Read the requirements: the experience line and the number of tools tell you more about how open the job really is.

## Limitations

- Regex can miss experience written in unusual ways ("a couple of years").
- ELFI weights are my own choice, not an industry standard.
- Groups like Australia and Canada are small, so their averages are less reliable.
- The postings come from one period and mostly from the US.

**Tools:** Python, Pandas, Matplotlib, regular expressions, Google Colab
