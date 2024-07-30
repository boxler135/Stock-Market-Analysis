# Stock-Market-Analysis

---

## Overview
This project explores the historical data of the S&P 500 index to analyze its performance and trends. The S&P 500 is widely regarded as a stable and reliable benchmark of the U.S. stock market, encompassing 500 of the largest publicly traded companies. While the S&P 500 is generally considered stable, I have chosen this particular index with a goal of finding potential market lows to identify optimal buying opportunities. It should be noted that I personally invest in the Vanguard S&P 500 ETF (VOO), reflecitng my confidence in the stability of this index.

## Motivation
This project was undertaken as a personal challenge to try something new beyond my regular school work and to put my data analysis skills to the test. It is an exercise in exploring financial data and modeling stock market trends.

## Limitations and Disclaimer
While the S&P 500 is a stable index, this model is primarily for educational purposes and to identify potential buying opportunities during market lows. Replicating this work for other, more volatile stocks is possible, but it is not recommended due to the complexities and additional factors involved, especially unforseen ones such as:
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

---

## Journey:

#### Day 1:

- After some lit review, I have chosen to use SNP500 as my stock of choice.
- Note that the ticker code for SNP500 is `^GSPC`.
- I have also successfully loaded the data using yfinance package.
- From this very first day, I have come to realise that doing EDA on S&P500 is going to involve a lot of researching about the stock market and writing up on the findings (including historical events like dot-com bubble)

Files created/ worked on:
- EDA.ipynb
- README.md
- requirements.txt

---

#### Day 2:

- Plotted histograms for  `Open`, `High`, `Low`, `Close`, `Volume`.
- Conducted detailed analysis on each plot.
- Created `Rolling_Mean` and plotted closing price against Date to compare rolling mean curve against normal closing price.
- Plotted headmap to find out correlations between different features.
