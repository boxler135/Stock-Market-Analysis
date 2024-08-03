# Stock-Market-Analysis

---

## Overview
This project explores the historical data of the S&P 500 index to analyze its performance and trends. The S&P 500 is widely regarded as a stable and reliable benchmark of the U.S. stock market, encompassing 500 of the largest publicly traded companies. While the S&P 500 is generally considered stable, I have chosen this particular index with a goal of finding potential market lows to identify optimal buying opportunities. It should be noted that I personally invest in the Vanguard S&P 500 ETF (VOO), reflecting my confidence in the stability of this index.

## Motivation
This project was undertaken as a personal challenge to try something new beyond my regular school work and to put my data analysis skills to the test. It is an exercise in exploring financial data and modelling stock market trends.

## Limitations and Disclaimer
While the S&P 500 is a stable index, this model is primarily for educational purposes and to identify potential buying opportunities during market lows. Replicating this work for other, more volatile stocks is possible, but it is not recommended due to the complexities and additional factors involved, especially unforeseen ones such as:
- Economic Crises
- Political Events
- Market Sentiments
- Company-specific News

I do not take responsibility for any financial losses incurred by replicating this analysis. Investing in the stock market involves risks, and it is important to conduct thorough research and consult with financial advisors before making any investment decisions.

---

## Steps to run:
1. Ensure you are at the correct file path -> `./STOCK-MARKET-ANALYSIS`
2. Create virtual environment ``` python -m venv stockanalysis ```
3. Activate virtual environment, for Windows: `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser` , for MacOS/Linux: `source stockanalysis/bin/activate`
4. Install dependencies: `pip install -r requirements.txt`
5. Run `deployment.ipynb` cell by cell and check out final output.

---

## Detailed Explanation

### EDA.ipynb
In this notebook:

- Loaded the historical data of the S&P 500 index using the yfinance package.
- Conducted Exploratory Data Analysis (EDA):
- Plotted histograms of Open, High, Low, Close, and Volume to understand the distribution of these features.
- Created and visualized the Rolling_Mean to identify trends over time.
- Plotted a heatmap to explore correlations between different features.
- Engineered new features like lagged prices, returns, rolling statistics, and technical indicators (e.g., RSI, MACD).
- Documented observations and insights gained from the EDA.

### model.ipynb
In this notebook:

- Loaded the cleaned and preprocessed data.
- Explored various machine learning models:
- Started with Logistic Regression for its simplicity and interpretability.
- Tried Random Forest to leverage its ensemble learning capabilities.
- Settled on a Gradient Boosting Machine (GBM) after hyperparameter tuning, as it provided the best performance.
- Conducted feature importance analysis to understand which features were driving the model's predictions.
- Evaluated the model's performance using metrics like accuracy, ROC-AUC, precision, recall, and F1-score.

### deployment.ipynb
In this notebook:

- Imported the saved GBM model.
- Fetched live S&P 500 data using the yfinance package.
- Preprocessed the live data to calculate the necessary features.
- Scaled the features using the same scaler used during training.
- Used the trained GBM model to predict whether the S&P 500 price will go up or down the next day.
- Documented the steps for model deployment and provided scripts for loading the model and making predictions.

---

## Journey:

#### Day 1:

- After some lit review, I have chosen to use SNP500 as my stock of choice.
- Note that the ticker code for SNP500 is `^GSPC`.
- I have also successfully loaded the data using yfinance package.
- From this very first day, I have come to realise that doing EDA on S&P500 is going to involve a lot of researching about the stock market and writing up on the findings (including historical events like dot-com bubble)

#### Day 2:

- Plotted histograms for  `Open`, `High`, `Low`, `Close`, `Volume`.
- Conducted detailed analysis on each plot.
- Created `Rolling_Mean` and plotted closing price against Date to compare rolling mean curve against normal closing price.
- Plotted headmap to find out correlations between different features.

#### Day 3:

- Analyzed heatmap, noticed a lot of interesting correlations between features.
- Done feature engineering to introduce 4 new features.
- visualised new features to find trends, as well as generate summaries.
- Completed EDA.

#### Day 4:

- Loaded cleaned dataset into model.ipynb
- Explored various models and came to conclusion with hyperparameter-tuned GBM.
- Feature importance analysis completed
- model deployment done in new file `deployment.ipynb`

---

## Learnings and Reflections

### Key Learnings:
- Data Understanding: Gained a deeper understanding of the S&P 500 index and its historical trends. This involved researching major market events and understanding their impact on the index.
- Feature Engineering: Learned the importance of creating meaningful features from raw data. This includes lagged features, rolling statistics, and technical indicators that can significantly improve model performance.
- Model Selection and Tuning: Explored various machine learning models and learned the process of hyperparameter tuning to improve model performance. The exercise highlighted the importance of choosing the right model and tuning it appropriately.
- Model Evaluation: Developed skills in evaluating model performance using various metrics like accuracy, ROC-AUC, precision, recall, and F1-score. This is crucial for understanding the strengths and weaknesses of the model.
- Deployment: Gained experience in the end-to-end process of deploying a machine learning model. This includes saving the model, writing scripts for loading the model, and making real-time predictions with live data.

### Reflections:
- Challenges: One of the major challenges was understanding and implementing the feature engineering techniques. It required a lot of trial and error to find the features that significantly improved the model's performance.
- Insights: The process of hyperparameter tuning for the Gradient Boosting Machine was insightful. It showed how tweaking certain parameters can lead to noticeable improvements in model accuracy and robustness.
- Future Work: While this project focused on the S&P 500, the learnings and techniques can be applied to other indices or individual stocks. Future work could explore more advanced models like XGBoost or LightGBM, which might offer even better performance.
- Practical Application: This project underscored the importance of understanding the domain (stock market) and how different factors can influence predictions. It was a valuable exercise in applying data science techniques to a real-world problem.

---

Thank you for taking the time to read my very first project :)
