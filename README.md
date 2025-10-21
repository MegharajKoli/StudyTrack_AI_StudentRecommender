# StudyTrack_AI_StudentRecommender

## 🎯 Project Objective
The primary objective of this milestone was to perform comprehensive **Exploratory Data Analysis (EDA)** and **Data Preprocessing** on a student habits dataset. The goal is to identify strong correlations between student lifestyle/study habits and academic performance, laying the foundation for building a personalized study track recommendation system in the next milestone.

---

## 💾 Dataset Source
Dataset Name - Student Habits and Academic Performance Dataset 
Source URL [https://www.kaggle.com/datasets/aryan208/student-habits-and-academic-performance-dataset](https://www.kaggle.com/datasets/aryan208/student-habits-and-academic-performance-dataset) 
Nature- Synthetic (Simulated) 
Size ~80,000 student records 

---

🛠️ Tools Used
* **Python:** Programming Language
* **Pandas:** Data manipulation, cleaning, and preprocessing (split, join, encoding).
* **NumPy:** Numerical operations and array handling.
* **Matplotlib & Seaborn:** Data visualization and graphical analysis.

---

## ⚙️ Steps Followed (Preprocessing & EDA)

### 1. Data Loading and Conceptual Join
* The single consolidated CSV file was loaded.
* **Conceptual Splitting:** The data was logically separated into two tables (e.g., **`Student_Profile`** and **`Academic_Outcomes`**) using the **`student_id`** column as the primary key.
* **Join Operation:** The tables were successfully rejoined using the Pandas `pd.merge()` method to form the final working DataFrame.

### 2. Data Cleaning and Preprocessing

| **Missing Values/Duplicates** | Checked and confirmed data was clean (no missing values, no duplicates). | Ensured data quality and integrity. |
| **Feature Engineering** | Created **`net_study_hours`** (`study_hours_per_day` - `social_media_hours`) and **`screen_to_study_ratio`**.
| **Encoding** | Ordinal encoding for **`dropout_risk`** (Low, Medium, High). One-hot encoding for nominal features like **`major`** and **`gender`**. 


### 3. Exploratory Data Analysis (EDA)
## 🔑 Key Insights and Graphs

The EDA revealed several strong, actionable relationships critical for the recommendation system:

### Key Insights
1.  **High Correlation (Actionable):** The strongest positive predictors of `exam_score` are **`study_hours_per_day`** and **`mental_health_rating`**. The engineered **`net_study_hours`** (study time minus social media time) is a particularly effective predictor.
2.  **Risk Factors:** Excessive **`social_media_hours`** is strongly correlated with lower exam scores and higher `dropout_risk`.
3.  **Time Management:** Students in the **High Dropout Risk** category consistently display lower median **`time_management_scores`**.
4.  **Interaction Effects:** The benefit of **`extracurricular_participation`** is highly dependent on whether a student is already "Efficient" (positive net study hours).


