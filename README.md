"# Online Courses Analysis & Dashboard

## Project Overview
This project provides comprehensive data analysis and preprocessing for online courses data. It includes data cleaning, transformation, and preparation steps to create a clean dataset ready for visualization and analysis.

## Dataset
The project uses the `Online_Courses.csv` dataset containing information about various online courses from different platforms.

## Features

### Data Preprocessing
The preprocessing pipeline includes:
- **Missing Value Handling**: Intelligent imputation strategies for different column types
- **Data Cleaning**: 
  - Removal of columns with less than 30% valid data
  - Handling of empty strings and spaces
  - Type conversions and standardization
- **Feature Engineering**:
  - Duration conversion to standardized hours format
  - Rating extraction and cleaning
  - Viewer count normalization
  - Category-based missing value imputation

### Cleaned Dataset Columns
- Title
- Category
- Rating
- Price
- Duration (in hours)
- Skills
- Number of viewers
- Instructors
- Language
- Site
- Course Type
- Courses

## File Structure
```
├── dataset/
│   └── Online_Courses.csv          # Raw dataset
├── image/                           # Project images/visualizations
├── preprocessing.ipynb              # Data cleaning and preprocessing notebook
├── online_courses_cleaned.csv       # Cleaned dataset output
├── List of calculated fields.txt    # Documentation of calculated fields
└── README.md                        # Project documentation
```

## Requirements
- Python 3.x
- pandas
- numpy
- re (regular expressions)

## Installation
```bash
pip install pandas numpy
```

## Usage

1. **Run the preprocessing notebook**:
   Open `preprocessing.ipynb` and run all cells to clean the data

2. **Output**:
   The cleaned data will be saved to `online_courses_cleaned.csv`

## Data Cleaning Steps

1. **Import Libraries**: pandas, numpy, re
2. **Load Dataset**: Read the raw CSV file
3. **Handle Missing Values**:
   - Fill Price with 0 for free courses
   - Replace missing Skills with "Unknown"
   - Fill Rating with median value
   - Category-based imputation for Duration
4. **Data Transformation**:
   - Convert duration to hours (from various formats)
   - Extract and normalize viewer counts
   - Clean rating values (remove "stars" text)
5. **Column Management**:
   - Drop irrelevant columns
   - Reorder columns for better readability
6. **Export**: Save cleaned data with proper encoding (UTF-8 with BOM)

## Output Format
The cleaned CSV file uses:
- Separator: `;`
- Encoding: `utf-8-sig`
- Decimal: `,`
- Float format: 1 decimal place

## Contributing
Feel free to fork this project and submit pull requests for any improvements.

## License
This project is open source and available for educational purposes." 
