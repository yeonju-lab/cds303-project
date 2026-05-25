# Session 1 : Data Collection & Paper Understanding

## Data Description
I selected the dataset "Stock Portfolio Performance" from the UCI Machine Learning Repository.

(Dataset source : http://archive.ics.uci.edu/dataset/390/stock+portfolio+performance)

The Stock Portfolio Performance dataset contains portfolio performance data generated from different stock selection
strategies using historical U.S. stock market data. The dataset includes financial return variables,
risk-related variables, and investment style indicators that describe the characteristics and performance of
stock portfolios.

## Three Main Categories of Variables

### Return-related Variables
These describe the profitability and performance of stock portfolios.

- Annual Return : yearly portfolio return
- Excess Return : return above the market average
- Win Rate : how often the porfolio performs successfully
- Abs. Win Rate : absolute winning rate
- Rel. Win Rate : winning rate compared to other portfolios

### Risk-related Variables
These describe the level of market-related and overall investment risk.

- Systematic Risk : market-related investment risk
- Total Risk : overall investment risk
- Small Systematic Risk : portfolio with lower market risk

### Investment Style
These describe different stock selection and investment strategies.

- Large B/P :undervalued value stocks (Book-to-Price)
- Large ROE : company profitability (Return On Equity)
- Large S/P  : sales relative to stock price (Sales-to-Price)
- Large Market Value : portfolios focused on large companies
- Large Return Rate in the last quarter : stocks with high recent quarterly returns

## Research Motivation and Research Question
There are three disadvantages of weighted scoring stock selection models.
1. They cannot identify the relations between weights of stock-picking concepts and performances of portfolios.
2. They cannot systematically discover the optimal combination for weights of concepts to optimize the performances.
3. They are unable to meet various investors' preferences.

Therefore, this project aims to identify meaningful groups of stock portfolios based on financial return and risk
characteristics and explain the important features that distinguish different portfolio groups.

### Research Question
"How can stock portfolios be grouped based on return and risk characteristics,
and which variables make the portfolio groups different?

## Key Focus on this Paper
The paper focused on several important performance indicators: annual return, excess return, systematic risk,
total risk, absolute win rate, and relative win rate. The key focus on the study was that a successful portfolio should not be considered only by high returns. Instead, the study emphasized the importance of 
considering return, risk, and winning rate all together when evaluating portfolio performance.

The paper also assumed that investors have different preferences and investment goals.
Therefore, it used various investor preferences as optimization objectives in the stock selection models.
For example, some investors may prioritize high returns, while others may prefer lower risk or more stable performance. As a result, the paper suggests that there is no signle standard for defining the "best" portfolio.

## Summary of this Paper's Methodology
### Experimental Design & Implementation
A mixture experimental design is adapted, and it consists of 63 different weighting combintions. The performances of the 63 weighting combinations were obtained by simulating them with Standard and Poor's Compustat US database. The backtest period includes 80 quarters, from 1990/Q4 to 2010/Q3. Six performance indicators can be computed based on these quarterly return rates: the annualized return rate, the excess return rte, the absolute winning rate, the relative winning rate, total risk, and systematic risk.

1. Dividing data set with moving time-frame method

The study divided the dataset into training and testing sets before building the neural network models. Since the relationship between stock-picking concepts and portfolio performance indicators may change over time, the study used a moving time-frame approach to consider time factors when splitting the data.

<img width="466" height="114" alt="image" src="https://github.com/user-attachments/assets/d65d9811-e742-4a13-8e09-69e1cf5c0822" />

2. Normalization of performance indicators

The study normalized all performance indicators into the same scale before building the neural network models. The paper explained that stock market tendencies can affect absolute return rates, so normalization was necessary to build a precise performance prediction model. The normalized scale ranged from 0.2 to 0.8.

3. Building performance predictive model with neural networks and cross-validation

The study used neural networks to build performance prediction models and employed cross-validation to evaluate the models. The results showed that predicting future investment performance is difficult and unstable, although some performance indicators were more predictable than others.

<img width="448" height="260" alt="image" src="https://github.com/user-attachments/assets/3f72b451-550b-4cbb-bfcf-35fc7376f56b" />

4. Effects of weights of stock-picking concepts on performance indicators

The study explored the effects of different stock-picking concept weights on portfolio performance indicators using neural network-based prediction models.

<img width="625" height="534" alt="image" src="https://github.com/user-attachments/assets/2c79b605-6228-4b92-831d-f045aa6050f3" />


