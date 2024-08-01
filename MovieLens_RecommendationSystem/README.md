# MovieLens 20M Dataset Recommendation System

## Project Overview

This project involves building a movie recommendation system using the MovieLens 20M dataset. The dataset contains ratings and tagging activities from MovieLens, a movie recommendation service. The goal of this project is to leverage this data to provide movie recommendations using collaborative filtering techniques.

## About the Dataset

The MovieLens 20M dataset includes:
- **20000263 ratings** and **465564 tag applications**
- **27278 movies** rated by **138493 users**
- Data collection period: **January 09, 1995** to **March 31, 2015**
- Dataset generated on **October 17, 2016**

Users were randomly selected for inclusion, and all selected users had rated at least 20 movies.

For more details and to download the dataset, visit the [Kaggle dataset page](https://www.kaggle.com/datasets/grouplens/movielens-20m-dataset).

## Project Components

1. **Data Loading and Preprocessing**
   - Load the ratings and movies data from CSV files.
   - Perform basic data cleaning and preprocessing.

2. **Exploratory Data Analysis (EDA)**
   - Visualize the distribution of movie ratings.
   - Analyze the top-10 most rated movies using boxplots.

3. **Model Building**
   - Use the Surprise library to build a recommendation system.
   - Implement the SVD (Singular Value Decomposition) model for collaborative filtering.

4. **Model Evaluation**
   - Evaluate the model using RMSE (Root Mean Squared Error).
   - Round predicted ratings to the nearest acceptable values.
   - Compare the distribution of predicted ratings with true ratings.
   - Visualize the prediction errors.

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-surprise

## Installation

To install the required libraries, you can use the following command:

```bash
pip install pandas numpy matplotlib seaborn scikit-surprise
```

## Usage

1. **Load the data**:
   - Ensure that the `ratings.csv` and `movies.csv` files are available at the specified paths.

2. **Run the analysis**:
   - Execute the Python script to perform EDA, build the recommendation model, and evaluate its performance.

3. **Visualize the results**:
   - Check the generated plots for insights into rating distributions, model predictions, and errors.

## Contributing

Feel free to contribute to this project by submitting issues or pull requests. For any questions or suggestions, please contact me.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
