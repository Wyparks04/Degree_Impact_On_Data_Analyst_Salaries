## 1. Project Setup Instructions 
 
Follow these steps to download, install, and run the project: 
 
1. **Clone the repository** 
   ```bash 
   git clone https://github.com/wyparks04/Degree_Impact_On_Data_Analyst_Salaries
   cd Degree_Impact_On_Data_Analyst_Salaries


Create a virtual environment: 

    python -m venv venv 
 

Activate the virtual environment: 

    a. On Windows: venv\Scripts\activate 
 

    b. On macOS/Linux: source venv/bin/activate 
 

Install dependencies: 

    pip install -r requirements.txt 
 

Run the project: 

    a. Open the Jupyter Notebook: jupyter notebook 
 

    b. Navigate to the notebook file and run all cells. 


### 2. Project Overview 
```markdown 
## Project Overview 
 
This project analyzes job postings to compare salaries and requirements for positions with and without degrees.   
The goal is to provide clear, data‑driven insights into how degree requirements affect job opportunities and compensation.   
 
Once the project is running, users will see: 
- Cleaned datasets prepared for analysis 
- Visualizations showing salary distributions and trends 
- A narrative explanation of findings in plain language 
 
No coding background is required to understand the results — all outputs are explained clearly and supported by visuals. 

## Datasets 
Ai_jobs_dataset.csv - This dataset provides a number of roles including data analyst jobs from the artificial intelligence job market with over 15,000 real job postings collected from major job platforms worldwide. It includes detailed salary information, job requirements, company insights, and geographic trends. This dataset includes detailed information such as job titles, salaries, employment type, company location, remote status, required skills, and education requirements.

Data_analyst_jobs.csv - This dataset was manipulated from the data_jobs dataset created by Luke Barousse containing hundreds of thousands of real-world job postings related to data analytics, data engineering, and data science roles. It was manipulated to include only data analyst jobs. This dataset includes detailed information such as job titles, salaries, employment type, company location, remote status, required skills, and education requirements. The dataset supports analysis of hiring trends, skill demand, and salary patterns across the data industry.

## Data Summary
Salary Levels: Degree vs. No Degree

1. Mean (Average) Salary

Category	Mean Salary
Degree-required	157,416
No-degree	91,438
Degree roles average 66k more, but remember:
The degree dataset includes Master’s and PhD outliers, and the max value confirms that.

2. Outlier Alert: The Degree Salaries Are Inflated

Look at the degree_salary max:

Max degree salary: 349,508

Max no-degree salary: 125,000

That 349k value is way outside normal entry-level ranges. This shows how advanced-degree roles inflate the upper range.

The standard deviation confirms this:

Degree std: 92,158 - extremely wide spread

No-degree std: 33,923 - much tighter, more consistent

3. Medians Tell the Real Story

Medians are more robust to outliers:

Category	Median Salary
Degree-required	158,378
No-degree	100,000
The real difference is closer to 58k, not 66k.
Still meaningful, but not extreme.

4. Salary Ranges

Degree-required
Min: 47,558

25%: 75,085

50%: 158,378

75%: 176,235

Max: 349,508 (outlier)

No-degree
Min: 41,446

25%: 55,000

50%: 100,000

75%: 125,000

Max: 125,000

## Data Dictionary 

job_title

salary_usd

employment_type

company_location

is_remote

employee_location

job_skills

degree_required

posting_date

company_name

has_target

salary_tier

degree_flag

## 3. Technologies Used 
 
- Python: Core programming language for data analysis 
- Pandas: Used to clean and manipulate the dataset (handling missing values, feature engineering) 
- SQL: Applied for joins and structured queries to combine datasets 
- Matplotlib: Created visualizations to highlight salary trends and degree requirements 
- Jupyter Notebook: Provided a narrative‑driven environment to present both code and results 
- Git/GitHub: Version control and collaboration, ensuring reproducibility and transparency


## 4. Results / Findings

This project analyzed two datasets to compare salary patterns for data analyst roles.

degree_jobs — positions requiring a formal degree (primarily bachelor’s‑level roles)

no_degree_jobs — positions requiring no formal degree (portfolio‑based or entry‑level)

The goal was to understand how education requirements influence salary ranges for early‑career data analyst positions.

1. Education Levels in the degree_jobs Dataset:

Although the degree_jobs dataset includes a wide range of education requirements, the focus of this project is on bachelor’s‑level / entry‑level roles.

However, the dataset also contains:

202 listings requiring a Master’s degree

175 listings requiring a PhD

These advanced‑degree roles are not representative of the bachelor’s‑level job market and were treated as outliers when comparing salaries between degree and no‑degree positions.

Their presence explains why the raw salary distribution for degree_jobs initially appears higher — the advanced‑degree roles inflate the upper salary range.

2. Salary Comparison: Degree vs. No Degree:

Degree-required (Bachelor’s / Entry-Level)
 After excluding Master’s and PhD outliers, bachelor’s‑level roles show a clear, consistent salary range typical of early‑career data analyst positions.
 These roles generally offer higher median salaries than no‑degree roles, but not dramatically higher.

No-degree roles
Salaries remain competitive, especially for positions emphasizing skills, tools, and portfolio work.
The salary range is slightly lower on average, but still viable for entry‑level candidates.

3. Data Quality Insight
The presence of data analyst roles requiring Master’s and PhD listings were from an AI Jobs Dataset. Identifying and treating these advanced‑degree roles as outliers was essential for producing a fair comparison between bachelor’s‑level and no‑degree roles.


## 5. Key Takeaway

When comparing entry‑level data analyst roles:
    - Bachelor’s‑required positions tend to offer moderately higher salaries.
    - No‑degree positions remain competitive and accessible, especially for candidates with strong portfolios.

Advanced‑degree listings (Master’s/PhD) where included in the visualizations for transparency, but they should not be interpreted as typical for entry‑level roles. For the core comparison, these listings were excluded to avoid skewing the results.


## 6. Conclusion

This analysis shows that entry‑level data analyst roles are accessible through multiple pathways. While bachelor’s‑required positions tend to offer moderately higher salaries, the difference is not so large that it creates a barrier for candidates entering the field without a formal degree. No‑degree roles remain competitive, especially for applicants who demonstrate strong technical skills and a solid portfolio.

The presence of Master’s and PhD listings in the AI Jobs Dataset highlights how mixed education levels can distort salary comparisons. Treating these advanced‑degree roles as outliers allowed for a clearer, more accurate comparison between bachelor’s‑level and no‑degree positions. Overall, the findings suggest that both pathways—degree and no‑degree—can lead to viable, well‑paying opportunities in data analytics, with skills and demonstrable experience playing a major role in employability.

---

## 7. Limitations

- Mixed education levels in the AI Jobs Dataset:
  The degree_jobs dataset included roles requiring Bachelor’s, Master’s, and PhD degrees. Although advanced‑degree roles were treated as outliers for the core comparison, their presence still influenced the overall salary distribution and required additional filtering.

- Dataset source variability:  
  Job‑posting datasets often contain inconsistencies in how employers label education requirements, experience levels, and salary ranges. These inconsistencies may affect the precision of the comparisons.

- Entry‑level focus: 
  This analysis specifically targeted entry‑level data analyst roles. Findings may not generalize to mid‑level or senior positions, which follow different salary patterns and education expectations.

- Salary reporting differences: 
  Some listings provided exact salary values, while others offered ranges or estimates. These differences can introduce variation in the aggregated salary metrics.

- Geographic and industry factors not included:
  Salaries can vary significantly by region, company size, and industry sector. These factors were not isolated in this analysis and may influence salary outcomes.

### Data Source
This project uses two publicly available datasets:

1. Global AI Job Market & Salary Trends 2025  
Citation:
Sajjad, B. (2025). Global AI Job Market & Salary Trends 2025. Kaggle.
Available at: https://www.kaggle.com/datasets/bismasajjad/global-ai-job-market-and-salary-trends-2025

2. Data Jobs Dataset  
Citation:
Barousse, L. (2023). Data Jobs Dataset. Hugging Face Datasets.
https://huggingface.co/datasets/lukebarousse/data_jobs