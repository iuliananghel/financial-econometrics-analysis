# Financial Econometrics Analysis: FTSE MIB Stylized Facts & Factor Models

This repository contains a comprehensive financial econometrics study conducted in Python. The analysis focuses on the statistical properties of the Italian stock market (FTSE MIB), the modeling of conditional volatility, and the implementation of asset pricing factor models.

## Project Overview

The project is structured into three main econometric pillars:

### 1. Analysis of Stylized Facts (FTSE MIB)
Detailed investigation of the statistical properties of the FTSE MIB returns, including:
* **Volatility Clustering:** Examination of the tendency of large changes in asset prices to be followed by large changes.
* **Fat Tails (Kurtosis):** Statistical testing for non-normality and leptokurtic distribution of financial returns.
* **Autocorrelation:** Analysis of return independence and squared return dependency.

### 2. Volatility Modelling (GARCH)
Implementation of **Generalized Autoregressive Conditional Heteroskedasticity (GARCH)** models to capture and forecast time-varying volatility. 
* Model selection based on Information Criteria (AIC/BIC).
* Residual diagnostics to ensure model adequacy.

### 3. CAPM and Fama-French 3-Factor Model
Application of the classic asset pricing framework to decompose portfolio returns:
* **Market Risk Premium:** Exposure to the overall market movement.
* **Size Premium (SMB - Small Minus Big):** Analysis of the market capitalization effect.
* **Value Premium (HML - High Minus Low):** Analysis of the book-to-market ratio effect.

## Tech Stack
* **Language:** Python 3.x
* **Libraries:** * `pandas` & `numpy` for data manipulation.
    * `matplotlib` & `seaborn` for advanced data visualization.
    * `statsmodels` for rigorous statistical testing and OLS regressions.
    * `arch` for GARCH process estimation.

## Key Insights
* The FTSE MIB shows significant evidence of **volatility clustering**, especially during periods of market stress.
* The returns distribution exhibits **excess kurtosis**, confirming that extreme events occur more frequently than predicted by a Normal distribution.
* The **Fama-French decomposition** provides insights into the risk factor exposures of the analyzed assets relative to global market benchmarks.

## Repository Structure
`data/`: Folder containing datasets (Fama-French factors).
* `LICENSE`: MIT License for open-source distribution.
* `requirements.txt`: List of Python dependencies (pandas, numpy, arch, statsmodels, yfinance).
* `"FTSE-MIB Financial Econometrics Project".ipynbIN`: The main Jupyter Notebook containing the full code, mathematical derivations, and visual results.

## Reproducibility
The analysis is designed to be fully reproducible:
* **Market Data:** Automatically downloaded via the `yfinance` API for the period 1997-2024.
* **Risk Factors:** The Fama-French 3-factor data (Market Premium, SMB, HML) is integrated into the workflow to analyze the risk drivers of the Italian market.
* **Statistical Rigor:** All findings, including the rejection of normality (Jarque-Bera) and the presence of unit roots (ADF), are supported by formal statistical testing.
