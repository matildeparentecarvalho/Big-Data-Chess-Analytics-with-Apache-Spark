# Big Data Chess Analytics with Apache Spark
This project analyzes large-scale chess data using Apache Spark to identify patterns of weekly activity in international chess competitions. The goal is to cluster weeks of chess activity based on aggregated statistics derived from millions of individual games.

## Objective
Apply **Big Data processing and unsupervised learning** techniques to:
- Process large, heterogeneous datasets
- Engineer meaningful aggregated features
- Identify distinct profiles of chess activity using clustering

## Data
- Dataset: *This Week in Chess (TWIC) Archive* (Kaggle)
- Formats: `.pgn`, `.csv`, `.parquet`
- Size: ~2 million chess games
- Time period: 2012–2022

Due to computational constraints, the project was developed using a representative
sample and later scaled to larger portions of the dataset.

## ETL & Data Processing
- Data ingestion using Apache Spark
- Selection of Parquet format for efficient processing
- Cleaning and handling missing values
- Feature reconstruction (e.g. PlyCount derived from move sequences)
- Conversion of categorical variables using Spark ML pipelines

## Feature Engineering
Key features include:
- Average Elo rating per week
- Number of games per week
- Number of unique players
- Percentage of online games
- Game outcomes and opening information

Data was aggregated at **weekly level**, where each row represents one edition
of the TWIC bulletin.

## Clustering
- Algorithm: K-Means
- Framework: Spark MLlib
- Number of clusters: 4

Each cluster represents a distinct **profile of chess activity**, such as:
- Elite tournaments with high-rated players
- Large-scale open events
- Weeks with strong online presence
- Stable and moderate activity weeks

## Tools & Technologies
- Apache Spark
- PySpark
- Spark MLlib
- Parquet
- Python

## Key Learnings
- Designing scalable ETL pipelines
- Working with distributed data processing
- Aggregation strategies for unsupervised learning
- Interpretation of clustering results in a real-world context
