# AI-Powered Algorithmic Trading Strategy

An AI-enhanced trading algorithm that combines Large Language Model sentiment analysis with momentum factors to generate superior risk-adjusted returns.

[Strategy Performance]
<Figure size 1000x500 with 1 Axes><img width="846" height="470" alt="image" src="https://github.com/user-attachments/assets/28c28571-059b-44db-abd0-314679c72b0d" />

## 🎯 Project Overview

This project demonstrates the integration of modern AI (Google Gemini LLM) with traditional quantitative finance techniques to create a profitable trading strategy.

## 🛠️ Technical Stack

- **Python 3.10+**: Core programming language
- **Pandas & NumPy**: Data manipulation and numerical computing
- **Google Gemini 2.0 Flash**: LLM for sentiment analysis
- **Matplotlib & Seaborn**: Data visualization
- **yfinance**: Benchmark data retrieval

## 📊 Strategy Components

### 1. Sentiment Analysis (Part 1)
- Processed **390 daily news summaries** using Gemini LLM API
- Extracted normalized sentiment scores (-3 to +3 scale)
- Batch processing with rate limiting and error handling

### 2. Trading Strategy (Part 2)
- **Multi-factor model**: 30% sentiment + 70% momentum signals
- **Dynamic position sizing**: Concentrated allocation (80/40 split)
- **Risk management**:
  - 10% stop-loss triggers
  - Trend filters (20/50-day MA crossover)
  - Volatility-adjusted sizing

### 3. Hyperparameter Optimization (Part 3)
- Grid search across **25 parameter combinations**
- Optimized sentiment vs. momentum weights
- Improved Sharpe ratio

## 🚀 Quick Start

### Installation
```bash
# Clone the repository
git clone https://github.com/yourusername/llm-trading-strategy.git
cd llm-trading-strategy

# Install dependencies
pip install -r requirements.txt
```

### Setup

1. **Get Gemini API Key** (free): https://aistudio.google.com/app/api-keys
2. **Add your key** to `part1_sentiment_analysis.ipynb`:
```python
   GOOGLE_API_KEY = "your-api-key-here"
```

### Usage

Run the notebooks in order:
```bash
# 1. Generate sentiment scores
jupyter notebook notebooks/part1_sentiment_analysis.ipynb

# 2. Run backtest
jupyter notebook notebooks/part2_backtest.ipynb

# 3. Optimize parameters
jupyter notebook notebooks/part3_optimization.ipynb
```

## 📁 Project Structure
```
├── data/                          # Market data and news
├── notebooks/                     # Jupyter notebooks
│   ├── sentiment_analysis.ipynb
│   ├── backtest.ipynb
│   └── optimization.ipynb
├── results/                       # Generated plots and metrics
├── README.md                      # This file
└── requirements.txt               # Python dependencies
```

## 🔍 Methodology

### Signal Generation
```
Combined Score = 0.30 × Sentiment + 0.45 × Momentum(5d) + 0.25 × Momentum(20d)
```

### Position Sizing
- Top-ranked stock: 80% allocation
- Second-ranked stock: 40% allocation
- Apply 1.5x leverage to amplify returns

### Risk Controls
1. **Stop Loss**: Exit at -10% drawdown from recent peak
2. **Trend Filter**: Reduce positions 70% in downtrends
3. **Volatility Scaling**: Adjust sizing for constant risk

## 📊 Key Findings

1. **Momentum > Sentiment**: 45% weight on 5-day momentum vs 30% sentiment proved optimal
2. **Risk Management Critical**: Stop-losses reduced max drawdown by 8 percentage points
3. **Leverage Enhances Returns**: 1.5x leverage improved returns 42% with acceptable volatility
4. **Parameter Sensitivity**: Grid search revealed Sharpe ratio improved 52% with optimal parameters

## 🎓 Skills Demonstrated

- **Quantitative Finance**: Factor models, backtesting, performance attribution
- **Machine Learning**: LLM API integration, prompt engineering, structured output
- **Data Science**: Time series analysis, feature engineering, hyperparameter tuning
- **Python Development**: API integration, data pipelines, error handling
- **Risk Management**: Stop-loss implementation, position sizing, drawdown control

## 🔮 Future Enhancements

- [ ] Add more alternative data sources (social media, earnings calls)
- [ ] Implement reinforcement learning for dynamic position sizing
- [ ] Expand to more assets (sector rotation strategy)
- [ ] Add transaction cost modeling
- [ ] Build real-time monitoring dashboard
- [ ] Test on different time periods (robustness check)

## 📚 References

- Google Gemini API Documentation: https://ai.google.dev/docs

## 👤 Author

**Daiphy Lee**
- LinkedIn: https://www.linkedin.com/in/daiphylee/
- Email: daiphy.lee@uwaterloo.ca

## ⚠️ Disclaimer

This project is for educational purposes only. Past performance does not guarantee future results. Do not use this strategy for actual trading without thorough testing and risk assessment. The author is not responsible for any financial losses.

---

*Built with ❤️ using Python and Google Gemini AI*
