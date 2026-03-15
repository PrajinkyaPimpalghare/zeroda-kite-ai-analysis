# Financial Metrics & Terminology Reference

This guide explains common financial terms and metrics used by the Kite Zeroda Portfolio Analyzer.

---

## Stock Performance Metrics

### Absolute Return & Percentage Return
```
Absolute Return = Current Price - Purchase Price
Percentage Return = (Absolute Return / Purchase Price) × 100

Example:
- Bought @ ₹100
- Current @ ₹150
- Absolute: ₹50
- Percentage: 50%
```
**Use**: Quick understanding of profit/loss in rupees and percentage terms.

### Maximum High & Minimum Low (Since Purchase)
```
Max High = Highest price stock reached since purchase date
Min Low = Lowest price stock traded at since purchase date

Example:
- Purchase: ₹100
- Max High: ₹180 (potential unrealized gain: +80%)
- Min Low: ₹65 (max drawdown experienced: -35%)
```
**Use**: Understand volatility and price range since you bought.

### CAGR (Compound Annual Growth Rate)
```
CAGR = (Ending Value / Beginning Value)^(1/Years) - 1

Example:
- Invested: ₹1,00,000 5 years ago
- Current: ₹2,50,000
- CAGR = (2,50,000/1,00,000)^(1/5) - 1 = 20% annually
```
**Use**: Compare returns across different time periods fairly.

### Days Held & Holding Period Return
```
Days Held = Current Date - Purchase Date
Holding Period Return = Percentage Return
Annualized Return = (1 + Return)^(365/Days Held) - 1
```
**Use**: Understand if returns are good relative to time invested.

---

## Valuation Metrics (Determining if Stock is Expensive or Cheap)

### Price-to-Earnings Ratio (P/E)
```
P/E Ratio = Stock Price / Earnings Per Share (EPS)

Example:
- Stock Price: ₹3,000
- EPS: ₹150
- P/E = 20x

Interpretation:
- P/E < 15x = Undervalued (cheap)
- P/E 15-25x = Fair valued
- P/E > 25x = Overvalued (expensive)
```
**Use**: See if a stock is expensive or cheap relative to its earnings.
**Watch Out**: High P/E can be justified if growth is high. Low P/E can be a value trap.

### PEG Ratio (P/E to Growth)
```
PEG = P/E Ratio / Expected EPS Growth Rate (%)

Example:
- P/E = 24x
- Expected growth = 12%
- PEG = 24/12 = 2.0x

Interpretation:
- PEG < 1.0 = Undervalued (cheap for growth)
- PEG 1.0-2.0 = Fair valued
- PEG > 2.0 = Overvalued (expensive for growth)
```
**Use**: Compare expensive stocks with high growth vs cheap stocks with low growth.

### Price-to-Book Ratio (P/B)
```
P/B = Stock Price / Book Value Per Share
Book Value = Total Assets - Total Liabilities

Example:
- Stock Price: ₹1,500
- Book Value: ₹200
- P/B = 7.5x

Interpretation:
- P/B < 1.0 = Trading below asset value (very cheap)
- P/B 1.0-3.0 = Fair valued
- P/B > 5.0 = Investors betting on growth
```
**Use**: Understand what you're paying for assets vs. growth.

### Dividend Yield
```
Dividend Yield = (Dividend Per Share / Stock Price) × 100

Example:
- Stock Price: ₹1,200
- Annual Dividend: ₹48
- Yield = (48/1,200) × 100 = 4%
```
**Use**: Understand income from your holding.
**Note**: Dividend yield + price appreciation = total return.

---

## Profitability Metrics

### Profit Margin (Net Margin)
```
Net Profit Margin = (Net Profit / Revenue) × 100

Example:
- Revenue: ₹1,00,000 Cr
- Net Profit: ₹20,000 Cr
- Margin = 20%

Interpretation:
- 10-15% = Average
- 15-20% = Good
- 20%+ = Excellent quality company
```
**Use**: See how efficient a company is at converting sales to profits.

### Return on Equity (ROE)
```
ROE = (Net Profit / Shareholder Equity) × 100

Example:
- Net Profit: ₹5,000 Cr
- Shareholder Equity: ₹20,000 Cr
- ROE = 25%

Interpretation:
- ROE < 10% = Poor capital allocation
- ROE 10-15% = Average
- ROE 15-20% = Good
- ROE 20%+ = Excellent (company makes money efficiently)
```
**Use**: Understand how well company uses shareholder money.

### Return on Assets (ROA)
```
ROA = (Net Profit / Total Assets) × 100

Example:
- Net Profit: ₹5,000 Cr
- Total Assets: ₹50,000 Cr
- ROA = 10%
```
**Use**: See how efficiently company uses all its assets.

---

## Growth Metrics

### Revenue Growth
```
YoY Revenue Growth = ((Current Year Revenue - Previous Year Revenue) / Previous Year Revenue) × 100

Example:
- FY2024 Revenue: ₹1,00,000 Cr
- FY2025 Revenue: ₹1,15,000 Cr
- Growth = 15% YoY
```
**Use**: Understand if company is growing top-line.

### EPS Growth
```
EPS = Earnings Per Share = Net Profit / Number of Shares

YoY EPS Growth = ((Current Year EPS - Previous Year EPS) / Previous Year EPS) × 100

Example:
- FY2024 EPS: ₹150
- FY2025 EPS: ₹170
- Growth = 13.3% YoY
```
**Use**: See if profits are growing faster/slower than revenue.

---

## Risk Metrics

### Volatility (Standard Deviation)
```
Volatility shows how much price swings around the average.

Low Volatility = ±5% swings (stable, lower stress)
High Volatility = ±20% swings (exciting but risky)
```
**Use**: Understand price stability of your holding.

### Beta
```
Beta = 1.0: Moves exactly with market
Beta > 1.0: More volatile than market
Beta < 1.0: Less volatile than market

Examples:
- Beta 0.8: Swings 80% of market (defensive)
- Beta 1.5: Swings 150% of market (aggressive)
```
**Use**: See if stock amplifies market moves up or down.

### Debt-to-Equity Ratio
```
Debt-to-Equity = Total Debt / Shareholder Equity

Example:
- Total Debt: ₹50,000 Cr
- Equity: ₹100,000 Cr
- D/E = 0.5x

Interpretation:
- < 0.5x = Low debt (safe)
- 0.5-1.0x = Moderate debt (acceptable)
- > 1.0x = High debt (risky)
```
**Use**: See if company has borrowed too much money.

### Current Ratio (Liquidity)
```
Current Ratio = Current Assets / Current Liabilities

Example:
- Current Assets: ₹1,00,000 Cr
- Current Liabilities: ₹50,000 Cr
- Ratio = 2.0x

Interpretation:
- < 1.0x = Company may struggle with short-term payments
- 1.0-2.0x = Healthy
- > 3.0x = Excess cash (good, but may indicate underutilization)
```
**Use**: Understand company's ability to pay short-term obligations.

---

## Technical Analysis Terms

### Support Level
```
A price level where stock bounces up (buyers step in).

Example:
- Stock has tried dropping to ₹2,000 three times
- Each time it bounced up
- ₹2,000 = support level
```
**Use**: Good place to hold/accumulate. Sell stop if it breaks below.

### Resistance Level
```
A price level where stock reverses down (sellers step in).

Example:
- Stock has tried breaking ₹3,000 three times
- Each time it fell back
- ₹3,000 = resistance level
```
**Use**: Good place to take profits. Buy if it breaks above.

### Moving Averages
```
50-Day MA = Average price of last 50 days
200-Day MA = Average price of last 200 days

Interpretation:
- Price > 50D MA > 200D MA = Uptrend (bullish)
- Price < 50D MA < 200D MA = Downtrend (bearish)
```
**Use**: Understand trend direction.

### RSI (Relative Strength Index)
```
RSI ranges from 0 to 100.

Interpretation:
- RSI < 30 = Oversold (potential bounce up)
- RSI 30-70 = Normal range
- RSI > 70 = Overbought (potential pullback)
```
**Use**: Spot short-term extremes.

### MACD (Moving Average Convergence Divergence)
```
MACD compares fast and slow moving averages.

Bullish Signal = MACD crosses above signal line (buy)
Bearish Signal = MACD crosses below signal line (sell)
```
**Use**: Spot trend changes and momentum.

---

## Fundamental Analysis Terms

### P/E Growth (PEG)
```
Already explained above - compares P/E to growth rate.
```

### Free Cash Flow (FCF)
```
FCF = Operating Cash Flow - Capital Expenditure

Example:
- Operating Cash: ₹50,000 Cr
- CapEx: ₹15,000 Cr
- FCF = ₹35,000 Cr

Positive FCF = Company generates real cash (good)
Negative FCF = Company burns cash (concerning)
```
**Use**: See if company has real cash to pay dividends/invest.

### Enterprise Value (EV)
```
EV = Market Cap + Total Debt - Cash

Example:
- Market Cap: ₹3,00,000 Cr
- Debt: ₹50,000 Cr
- Cash: ₹30,000 Cr
- EV = ₹3,20,000 Cr
```
**Use**: Real value of company (accounting for debt).

### EV/Revenue Multiple
```
EV/Revenue = Enterprise Value / Annual Revenue

Example:
- EV: ₹3,20,000 Cr
- Revenue: ₹1,00,000 Cr
- Multiple = 3.2x

Interpretation:
- < 1x = Cheap
- 1-3x = Fair
- > 3x = Expensive
```
**Use**: Compare valuations across companies/industries.

---

## Market-Level Terms

### Sensex & Nifty
```
SENSEX = Index of top 30 companies in India (BSE)
NIFTY 50 = Index of top 50 companies in India (NSE)

Both represent overall market sentiment.
```

### Market Cap
```
Market Cap = Stock Price × Total Shares Outstanding

Example:
- Stock: ₹3,000 per share
- Shares: 50 Cr
- Market Cap = ₹1.5 Lakh Cr
```
**Use**: Understand company size. (Large Cap > ₹25K Cr, Mid Cap ₹5K-₹25K Cr)

### Sector Rotation
```
Moving money from one sector (falling) to another sector (rising).

Example: Moving from Financials (overgrowth) to IT (catching up)
```
**Use**: Portfolio rebalancing opportunity.

---

## Trading Timeline Definitions

### Short-Term (3-6 months)
- Focus on technical analysis, momentum, sentiment
- Action items: Buy/Sell at specific levels
- Risk: Higher due to volatility

### Medium-Term (6-18 months)
- Mix of technical and fundamental analysis
- Action items: Gradual accumulation/distribution
- Risk: Moderate

### Long-Term (1-5 years)
- Focus on fundamental analysis, business moats
- Action items: Build core positions, hold through cycles
- Risk: Lower, but cycle risk remains
- Reward: Highest compound returns

---

## Red Flags 🚩 (Warning Signs)

### Company Red Flags
- ❌ Negative Free Cash Flow (company burning money)
- ❌ Rising debt without rising profits
- ❌ Deteriorating margins (losing pricing power)
- ❌ Market share loss (competition winning)
- ❌ Management scandal/change (credibility loss)
- ❌ Failed guidance multiple times (execution issues)

### Valuation Red Flags
- ❌ P/E much higher than peers (paying too much)
- ❌ Negative growth with high P/E (growth story ending?)
- ❌ Dividend yield suddenly rising (stock falling = concern)

### Technical Red Flags
- ❌ Breaking below key support levels
- ❌ Breakdown below 200-day moving average
- ❌ Volume declining on rallies (weakness)

---

## Green Flags ✅ (Positive Signs)

### Company Green Flags
- ✅ Free Cash Flow increasing
- ✅ Margins expanding (operational efficiency)
- ✅ Market share gaining (competitive strength)
- ✅ New product launches seeing traction
- ✅ Management incentivized with stock ownership
- ✅ Beating guidance consistently (execution excellence)

### Valuation Green Flags
- ✅ P/E lower than peers but growth higher (undervalued)
- ✅ PEG ratio < 1.0 (cheap for growth)
- ✅ Trading near historical lows (good entry)

### Technical Green Flags
- ✅ Breaking above key resistance levels
- ✅ Rising above 50-day & 200-day moving averages
- ✅ Volume increasing on rallies (strength)

---

## Time-Based Analysis

### Month-Over-Month (MoM)
```
Sequencing matters. Example:
- Jun Revenue: ₹10,000 Cr
- Jul Revenue: ₹9,500 Cr
- Aug Revenue: ₹9,000 Cr

Negative MoM trend despite profitable = concern
```

### Quarter-Over-Quarter (QoQ)
```
Most important for quarterly results companies (banks, IT services).
```

### Year-Over-Year (YoY)
```
Most common measure. Removes seasonal variations.
```

---

## Important Caveats

⚠️ **These metrics are tools, not laws.**
- Good P/E stock can crash (sentiment change)
- Bad P/E stock can rally (sector rotation)
- Strong fundamentals take time to reflect in price

⚠️ **Market is uncertain, not stupid.**
- If metric shows "buy," others have seen it too
- Price reflects expectations, not reality
- Surprises (positive or negative) move stocks

⚠️ **Always diversify.**
- No single stock is "perfect"
- Even great companies have bad years
- Portfolio risk management > individual stock analysis

---

*Reference Guide - Kite Zeroda Portfolio Analyzer*
*Last Updated: March 14, 2026*
