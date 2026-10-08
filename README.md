# OTT Streaming Content Trend Analysis

## Project Overview

This project analyzes an OTT streaming content dataset to identify trends in content types, genres, ratings, release years, and countries.

The analysis was performed using Python, SQL, and Microsoft Excel to understand the composition of the streaming catalog and generate useful content strategy insights.

## Objective

The main objectives of this project are:

- Analyze Movies vs TV Shows distribution
- Identify the most popular content genres
- Analyze content rating distribution
- Study content trends by release year
- Identify major content-producing countries
- Generate actionable insights for OTT content strategy

## Dataset

The dataset used is the **Netflix Movies and TV Shows dataset**.

### Dataset Size

- Records: 8,807
- Columns: 12

### Important Columns

- `show_id`
- `type`
- `title`
- `director`
- `cast`
- `country`
- `date_added`
- `release_year`
- `rating`
- `duration`
- `listed_in`
- `description`

## Tools & Technologies

- Python
- Pandas
- Matplotlib
- Seaborn
- SQL
- SQLite
- Microsoft Excel
- Google Colab

## Data Cleaning

The following data-cleaning steps were performed:

- Checked dataset structure using `df.info()`
- Identified missing values
- Replaced missing values in important categorical columns
- Converted `date_added` into a date format
- Extracted the year from `date_added`
- Prepared genre and country data for analysis

## Exploratory Data Analysis

### 1. Movies vs TV Shows

Analyzed the distribution of Movies and TV Shows available in the Netflix catalog.

**Visualization:** Movies vs TV Shows on Netflix

### 2. Content Added by Year

Analyzed the number of titles added to Netflix over different years.

**Visualization:** Netflix Content Added by Year

### 3. Top 10 Genres

Analyzed the most frequently represented genres in the Netflix catalog.

**Visualization:** Top 10 Most Popular Genres on Netflix

### 4. Rating Distribution

Analyzed the distribution of Netflix content across different audience ratings.

**Visualization:** Netflix Content Rating Distribution

### 5. Content by Release Year

Analyzed the number of Netflix titles based on their original release year.

**Visualization:** Netflix Content by Release Year

### 6. Top Countries

Analyzed the countries contributing the largest amount of content to the Netflix catalog.

**Visualization:** Top 10 Countries by Netflix Content

## SQL Analysis

SQL was used to perform core aggregations such as:

- Movies vs TV Shows count
- Content count by genre/category
- Content count by rating
- Content count by release year

Example:

```sql
SELECT type, COUNT(*) AS total_titles
FROM netflix
GROUP BY type
ORDER BY total_titles DESC;
