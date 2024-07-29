# Stock-Market-Analysis
This is my first time trying to work with real-time data, I will be analysing a chosen stock from the US stock market and attempt to conduct an EDA on it, followed by creating a model to predict its future direction (increase or decrease). Hope it'll be fun and successful!

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
