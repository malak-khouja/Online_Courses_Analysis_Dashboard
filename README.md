# 📘 Online Courses Analytics Dashboard

## 📝 Project Overview

This project analyzes the *Kaggle Online Courses Dataset* to explore
trends in online learning, course performance, pricing patterns, and
instructor quality.\
Using *Python* for data cleaning and *Power BI* for visualization,
the project delivers a multi-page interactive dashboard with key
insights.

Dataset source:\
🔗 https://www.kaggle.com/datasets/khaledatef1/online-courses

## 📂 Project Structure

    📁 Online-Courses-Analytics/
    │
    ├── dataset/
    │   └── Online_Courses_raw.csv
    │
    ├── online_courses_cleaned.csv
    │
    ├── preprocessing
    │
    ├──List of calculated fields
    │
    ├──Summary
    │
    ├── Dashboard_Power_BI.pbix
    │
    ├── images/
    │   ├── Dashboard_Power_BI_cap1.png
    │   ├── Dashboard_Power_BI_cap2.png
    │   └── Dashboard_Power_BI_cap3.png
    │
    └── README.md

## 🧹 Data Cleaning (Python)

### ✔ Missing values

-   Filled missing categories, languages, and skills with "Unknown"
-   Removed rows missing essential fields such as Rating or Course Title
-   Cleaned inconsistent null formats (empty strings, "--", spaces)

### ✔ Numeric conversion

-   Converted Rating, Price, Duration, Number of Viewers into
    numeric formats
-   Standardized duration into *hours*

### ✔ Outliers processing
-   Ensured ratings remain within 0--5 range

## 📊 Dashboard Content (Power BI)

### 🔹 Page 1 -- Overview

-   KPIs:
    -   Total Courses
    -   Average Rating
    -   Median Price
    -   Average Duration
    -   \% Free Courses
-   Top 10 Categories (Number of Courses & Average Rating)
-   Rating distribution by Category

### 🔹 Page 2 -- Course Relationships

-   Price vs Rating scatter plot
-   Duration vs Rating scatter plot
-   Courses by Rating & Category (stacked)
-   Most common Skills + Average Rating per Skill

### 🔹 Page 3 -- Instructors & Program Types

-   Top 10 Instructors by Average Rating
-   Number of Courses per Course Type (Course, Specialization,
    Certificate, etc.)

### 🔹 Filters

-   Category\
-   Language\
-   Level\
-   Platform\
-   Price Range\
-   Program Type

## 🧮 Key DAX Measures

    Total Courses = COUNTROWS(Courses)

    Average Rating = AVERAGE(Courses[Rating])

    Median Price = MEDIAN(Courses[Price])

    Average Duration = AVERAGE(Courses[DurationHours])

    FreeCoursesPercent =
        DIVIDE(
            CALCULATE(COUNTROWS(Courses), Courses[Price] = 0),
            [Total Courses]
        )

    Skill Count = COUNTROWS(Skills)

## 🔍 Key Insights

1.  **Data-related fields dominate in both popularity and rating.**\
    Categories like Data Science, Computer Science, and IT show
    strong supply and high satisfaction.

2.  *Majority of ratings lie between 4.4--4.8*, suggesting a positive
    bias or consistently good course quality.

3.  *Price median = 0*, meaning at least half of courses are free,
    making online learning widely accessible.

4.  *Skills such as Python, Machine Learning, Data Analysis* are the
    most common and highest rated---indicating high market demand.

5.  *Some instructors consistently outperform others*, showing strong
    personal branding and teaching effectiveness.

## 🚀 Tools Used

-   *Python (Pandas, NumPy, Regex)*
-   *Power BI Desktop*
-   *DAX for calculated measures*
-   *Excel/CSV preprocessing*

## 📄 Author
**Malak Khouja**\
Online Learning Analytics Project -- 2025