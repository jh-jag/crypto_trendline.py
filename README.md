#module: pip install yfinance pandas numpy scipy matplotlib
# crypto_trendline.py
import yfinance as yf
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import linregress

#參數
TICKER = "BTC-USD"
DAYS = 180
SMA_WINDOW = 20

def fetcg_data(ticker, days):
    end = datetime.datetime.now()
    start = end - datetime.timedelta(days=days)
    df = yf.download(ticker, start=start.date(), end=end.date() progress=FALSE )
    df = df.dropna()
    return df

def add_sma(df, window):
  df{f"SMA{window}"} = df{'Close'}.rolling(window=window).mean()
  return df

def 
