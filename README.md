# Python Portfolio Analytics

[![status](https://img.shields.io/badge/Status-Running-green)](https://share.streamlit.io/simprecicchiani/pyportfolioanalytics/app/main.py)

A portfolio tracker featuring account transactions, historical allocation, dividends and splits management and endless performance metrics. [➡️ Go to web app](https://share.streamlit.io/simprecicchiani/pyportfolioanalytics/app/main.py)

![](/images/ppa-dashboard.jpg)

### Input example

| Date       | Ticker   | Order      | Price  | Quantity | Fee |
|------------|----------|------------|--------|----------|-----|
| 2019-10-01 | CASH.USD | deposit    | 1      | 100000   | 0   |
| 2019-10-11 | AAPL     | purchase   | 234.52 | 88       | 35  |
| 2019-11-25 | MSFT     | purchase   | 148.3  | 250      | 25  |
| 2019-12-04 | AAPL     | sale       | 262.08 | 50       | 20  |
| 2020-01-06 | FB       | purchase   | 208    | 100      | 10  |
| 2020-01-25 | CASH.USD | withdrawal | 1      | 30000    | 0   |

### Develop

Test locally in conda environment:
```
$ git clone https://github.com/simprecicchiani/iPortfolio.git
$ cd iPortfolio
$ conda env create -f .environment.yml
$ conda activate ppa
```

Alternatively with pip in a virtual environment (python>=3.9):
```
$ git clone https://github.com/simprecicchiani/iPortfolio.git
$ cd iPortfolio
$ pip install -r requirements.txt
```

Run the web app locally with
```
$ streamlit run app/main.py
```

Open either `/tests/yf_test.ipynb` (uses Yahoo Finance, slower, support multicurrency) or `/tests/av_test.ipynb` (requires a [free Alpha Vantage API key](https://www.alphavantage.co/support/#api-key)).

Newest version `/tests/pdr_test.ipynb` with pandas-datareader.

### Built with

Python 3.9 and additional packages (leveraging pandas DatetimeIndex feature)

## To Do

- [x] Migration to Alpha Vantage
- [x] Portfolio builder UI (not available)
- [x] Data sanity check (not available)
- [x] Portfolio dashboard (early stage)
- [ ] Multicurrency portfolio (done in yf variant)

## Further development

- Portfolio Technicals
- Lots of charts
- Indicators (Sharpe Ratio, Beta, VaR, etc)
- Sector Exposure (stocks only)