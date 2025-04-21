# Netflix  Movies and TV Shows  Data Analysis Project

## Overview
This project analyzes the Netflix dataset containing information about movies and TV shows available on the platform. The dataset includes details such as titles, directors, cast, countries, release years, ratings, and more. The analysis explores patterns in content, cleans the data, and prepares it for further analytical insights.

## Dataset Description
The dataset contains 8,807 records with 12 original columns:
- `show_id`: Unique identifier for each show
- `type`: Movie or TV Show
- `title`: Title of the content
- `director`: Director of the content
- `cast`: Actors and actresses in the content
- `country`: Country where the content was produced
- `date_added`: Date when the content was added to Netflix
- `release_year`: Year when the content was released
- `rating`: Content rating (e.g., TV-MA, PG-13)
- `duration`: Length of the content (minutes for movies, seasons for TV shows)
- `listed_in`: Genres and categories
- `description`: Brief summary of the content

## Data Cleaning Process

### Handling Missing Values
1. **Director column**: 2,634 missing values replaced with "Unavailable"
2. **Cast column**: 825 missing values handled by creating a separate `cast_by` column with "unknown" for missing values
3. **Country column**: 831 missing values filled with the most common country
4. **Date_added column**: 10 missing values filled with the mode (January 1, 2020)
5. **Rating column**: 7 missing values (including improperly formatted ones with "min" suffix) replaced with the mode value "TV-MA"

### Data Transformation
1. **Date formatting**: Converted `date_added` to datetime format
2. **Country standardization**: Created a mapping to standardize country names (e.g., "United States" to "USA")
3. **Duration processing**: Split the duration column into:
   - `duration_min`: Extracted minutes for movies
   - `duration_season`: Extracted number of seasons for TV shows
4. **Column renaming**: Renamed `listed_in` to `categories` for clarity

### Data Improvement
1. Removed null values across all columns
2. Checked for and confirmed no duplicate rows exist in the dataset
3. Created separate columns for movie duration in minutes and TV show seasons
4. Final dataset contains 13 columns including the derived ones

## Key Insights
- Most common director in the dataset: Rajiv Chilaka (19 titles)
- The United States is the primary content producer, followed by India
- Most content on Netflix is rated TV-MA, followed by TV-14
- There's a mix of movies (with duration in minutes) and TV shows (with duration in seasons)

## Tools Used
- Python for data manipulation and analysis
- Libraries: pandas, numpy
- Data cleaning, transformation, and exploratory data analysis techniques


