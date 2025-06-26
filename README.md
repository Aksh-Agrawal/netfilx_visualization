# Netflix Movie Database Analysis & Visualization

A comprehensive data analysis and visualization project exploring movie trends, genres, ratings, and popularity patterns using a Netflix-like movie database.

## 📊 Project Overview

This project analyzes a movie database containing nearly 10,000 movies to uncover insights about:

- Genre distribution and popularity
- Movie rating patterns
- Release date trends
- Popularity metrics
- Vote average categorization

## 🗂️ Dataset

**File:** `mymoviedb.csv`

- **Size:** 9,827 movies
- **Original Columns:** 9 features
- **Key Features:**
  - Release Date
  - Title
  - Overview
  - Popularity
  - Vote Count
  - Vote Average
  - Original Language
  - Genre
  - Poster URL

## 🛠️ Technologies Used

- **Python 3.x**
- **Libraries:**
  - `pandas` - Data manipulation and analysis
  - `numpy` - Numerical computing
  - `matplotlib` - Data visualization
  - `seaborn` - Statistical data visualization

## 📋 Data Processing Pipeline

### 1. Data Loading & Initial Exploration

- Load dataset from CSV file
- Examine data structure and types
- Check for duplicates and missing values

### 2. Data Cleaning & Transformation

- **Date Processing:** Convert release dates to datetime format and extract year
- **Column Removal:** Drop unnecessary columns (Overview, Original_Language, Poster_Url)
- **Missing Data:** Handle null values by dropping incomplete records
- **Genre Processing:** Split multi-genre entries and explode into separate rows
- **Data Type Optimization:** Convert Genre to categorical type

### 3. Feature Engineering

- **Vote Average Categorization:**
  - Implement quartile-based binning function
  - Categories: 'poor', 'below_avg', 'average', 'popular'
  - Based on statistical distribution (min, 25%, 50%, 75%, max)

## 📈 Visualizations & Analysis

### 1. Genre Distribution Analysis

- **Visualization:** Horizontal count plot of movie genres
- **Insights:** Shows the most popular genres in the dataset
- **Styling:** Custom color scheme (#48275f)

### 2. Vote Average Distribution

- **Visualization:** Count plot of rating categories
- **Categories:** Poor, Below Average, Average, Popular
- **Styling:** Custom color scheme (#4827f5)

### 3. Popularity Analysis

- **Maximum Popularity:** Identify the most popular movie(s)
- **Minimum Popularity:** Identify the least popular movie(s)

### 4. Release Date Trends

- **Visualization:** Histogram of movie releases by year
- **Analysis:** Distribution of movies across different time periods

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn
```

### Running the Analysis

1. Clone this repository
2. Ensure `mymoviedb.csv` is in the project directory
3. Open and run `project.ipynb` in Jupyter Notebook/Lab or VS Code

### File Structure

```
netfilx_visualization/
│
├── mymoviedb.csv          # Dataset file
├── project.ipynb          # Main analysis notebook
└── README.md             # Project documentation
```

## 🔍 Key Findings

### Data Quality

- **Original Dataset:** 9,827 movies with 9 features
- **No Duplicates:** Clean dataset with unique entries
- **Data Completeness:** Handled missing values appropriately

### Feature Engineering

- Successfully categorized vote averages into meaningful segments
- Exploded multi-genre entries for granular analysis
- Optimized data types for better performance

### Visualization Insights

- Genre distribution reveals content preferences
- Rating categorization shows quality distribution
- Release date analysis shows temporal patterns
- Popularity metrics identify standout content

## 📊 Data Schema (Post-Processing)

| Column       | Type     | Description                                         |
| ------------ | -------- | --------------------------------------------------- |
| Release_Date | int64    | Year of movie release                               |
| Title        | object   | Movie title                                         |
| Popularity   | float64  | Popularity score                                    |
| Vote_Count   | int64    | Number of votes received                            |
| Vote_Average | category | Categorized rating (poor/below_avg/average/popular) |
| Genre        | category | Individual movie genre                              |

## 🎯 Future Enhancements

- [ ] Add interactive visualizations with Plotly
- [ ] Implement sentiment analysis on movie overviews
- [ ] Create a dashboard with filters and drill-down capabilities
- [ ] Add statistical correlation analysis
- [ ] Implement machine learning models for recommendation
- [ ] Include temporal trend analysis with time series
- [ ] Add comparison with industry benchmarks

## 📝 Notes

- The analysis focuses on data exploration and visualization
- Genre data was exploded to enable individual genre analysis
- Vote averages were categorized using quartile-based binning
- Visualizations use a consistent color scheme for professional appearance
