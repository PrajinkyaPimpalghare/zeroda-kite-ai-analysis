# Usage Examples - Kite Zeroda Portfolio Analyzer

This document contains real-world examples of how to use the portfolio analyzer agent for various analysis scenarios.

---

## Example 1: Quick Portfolio Overview

### Scenario
You want to quickly see how your entire portfolio is performing.

### Input
```
@kite-zeroda-portfolio-analyser

Quick overview of my portfolio:
- TCS: 50 shares, bought 2021-06-15 @ ₹3,100
- Infosys: 30 shares, bought 2020-01-01 @ ₹950  
- ITC: 100 shares, bought 2022-03-10 @ ₹190
- HDFC Bank: 25 shares, bought 2021-01-01 @ ₹1,200
- Reliance: 15 shares, bought 2023-01-15 @ ₹2,500
```

### Expected Output
The agent provides a table format:

```
PORTFOLIO SUMMARY - March 14, 2026
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Stock          Qty   Buy Date      Buy Price  Current   Gain/Loss    %Ret  Rec
TCS            50    2021-06-15    ₹3,100    ₹3,850    ₹37,500     +24.2% HOLD
Infosys        30    2020-01-01    ₹950      ₹1,820    ₹26,100     +91.6% BUY
ITC           100    2022-03-10    ₹190      ₹220      ₹3,000      +15.8% HOLD
HDFC Bank      25    2021-01-01    ₹1,200    ₹1,620    ₹10,500     +35.0% HOLD
Reliance       15    2023-01-15    ₹2,500    ₹2,850    ₹5,250      +14.0% HOLD

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Total Portfolio Value: ₹2,45,000 (approx)
Total Invested: ₹2,08,500
Total Gain: ₹36,500 | Return: +17.5%
```

### Follow-up Query
```
Should I book profits on Infosys right now or hold for more upside?
```

### Agent Response
```
INFOSYS - DETAILED VIEW
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Position: 30 shares
Entry: 2020-01-01 @ ₹950
Current: ₹1,820 | Gain: ₹26,100 (+91.6%)

SHORT-TERM (3-6 months):
Technical Analysis tells me stock is near intermediate resistance @ ₹1,850.
With IT sector showing mixed signals (Fed rate concerns), I'd:
- TAKE 40-50% PROFITS if price touches ₹1,900-₹2,000
- Keep 50-60% for long-term upside
- Set trailing stop loss @ ₹1,650 to protect gains

LONG-TERM (1-5 years):
Infosys remains compelling long-term:
- Digital spending growth continues
- Management guidance positive
- Valuation reasonable @ 22x PE
- Strong dividend track record (4.2% yield)

RECOMMENDATION: HOLD with partial booking strategy
- SELL 12-15 shares at ₹1,900-₹2,000 levels
- HOLD remaining 15-18 shares for 2-3 year appreciation
- This locks in ₹12,000-₹15,000 gains while keeping upside exposure
```

---

## Example 2: Detailed Single Stock Analysis  

### Scenario
You own TCS and want deep analysis about whether to hold for 5 years or exit sooner.

### Input
```
@kite-zeroda-portfolio-analyser

I need detailed analysis on TCS:
- 50 shares purchased on 2021-06-15 @ ₹3,100/share
- Current holding value ~₹1,92,500

Analysis needed:
1. Is TCS a good long-term hold?
2. What's your 1-year and 5-year target?
3. Should I add more or reduce position?
```

### Agent Response (Comprehensive)
```
TCS - TECHNOLOGY CONSULTING SERVICES LIMITED
Analysis Date: March 14, 2026
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

PORTFOLIO POSITION
Position: 50 shares
Entry: June 15, 2021 @ ₹3,100
Current: ₹3,850 | Gain: +24.2% (₹37,500)
Since Purchase: Up ₹750/share
5-Year Performance: TCS has delivered 18-22% CAGR (outperforming Nifty)
Max High: ₹4,200 (Oct 2024) - Could have gained +35.5%
Min Low: ₹2,850 (Mar 2023) - Maximum drawdown was -8%

MARKET CONTEXT (March 2026)
✓ Indian IT Sector: Recovering after 2-year slowdown
✓ Global Tech Spending: AI-driven digital transformation accelerating
✓ RBI Policy: Likely rate cuts in next 6 months (supportive)
✗ US Tech: Slowing growth, but India well-positioned
✗ Rupee: Strengthening (headwind for IT exports)

COMPANY ANALYSIS - LATEST UPDATES
Recent Developments (Last 6 months):
- Q3 FY2026 Results: Revenue ₹64,050 Cr (+15% YoY), Margins stable @ 21.5%
- New AI Practice: Launched major generative AI services division
- Headcount: Added 5,000 fresh hires (net addition)
- Client Wins: Deal wins up 35% vs last year - strong pipeline
- Dividend: Announced ₹32/share interim dividend (3.8% yield attractive)

Competitive Position:
- Market Leader: #1 in India IT services (₹ 3+ Lakh Cr revenue)
- Client Diversification: Excellent - #1 client only 8% of revenue
- Digital Revenue: Now 48% of total (up from 35% two years ago)
- Challenges: Rising talent costs, attrition @ 13% (manageable)

Management Outlook:
- CEO Guidance: +10-12% organic growth expected FY2027
- New Order Backlog: +22% YoY (highest in 5 years)
- Digital Spending Acceleration: 25-30% growth expected continuing

TECHNICAL ANALYSIS - 3-6 MONTH VIEW
Price Action:
- Current Trend: Uptrend since Nov 2025 +12%
- Support Levels: ₹3,650 (strong), ₹3,400 (intermediate)
- Resistance: ₹4,050 (near-term), ₹4,300 (intermediate)
- Trading Volume: Above average - healthy accumulation pattern

Momentum Indicators:
- RSI (14): 62 (approaching overbought but not extreme)
- MACD: Positive, but signal line crossover near
- 50-Day MA: ₹3,720 (price above - bullish)
- 200-Day MA: ₹3,480 (price well above - strong uptrend)

Short-Term Signals: MILD BULLISH, caution near ₹4,050

FUNDAMENTAL ANALYSIS - 1-5 YEAR VIEW
Valuation Metrics (as of March 14, 2026):
- Current P/E: 24x (vs 5-year average of 20x) - Slightly Premium
- Price-to-Book: 8.5x (vs sector median 7.2x) - Reasonable
- Forward P/E: 21x (for FY2027E growth) - Fair
- Dividend Yield: 3.8% + expected 10% capital appreciation = 13% total return potential
- PEG Ratio: 2.2x (Growth is there but valued fairly)

Growth Indicators:
- Revenue CAGR (5Y): 14% - Solid, below historical 18% (sector maturity)
- EPS CAGR (5Y): 12% - Conservative, profit growth slowing
- ROE: 18.5% (vs 12% for broader market) - Excellent capital efficiency
- Net Margin: 21.5% (vs 15% for sector) - Premium quality

Concerns:
- Slowdown in EPS growth (only 8-10% expected FY27)
- Talent inflation pressuring margins
- FX headwinds (strong rupee)

Tailwinds:
- AI services booming (TCS well-positioned)
- Deal velocity strong
- Capex going up (sign of confidence)

RISK ASSESSMENT
Downside Scenarios:
🔴 **Worst Case (20% probability)**: US recession hits hard → IT spending cuts
   - Fair Value Impact: Could fall to ₹3,200 (-17% from current)
   - Timeline: 6-12 months if triggered

🟡 **Below Scenario (40% probability)**: Slower growth, margins compress
   - Fair Value Impact: Could trade at ₹3,600-₹3,800 (-7% from current)
   - Timeline: Natural consolidation, not crisis

🟢 **Base Scenario (35% probability)**: Steady growth, valuations stabilize
   - Fair Value: ₹4,100-₹4,500 (+10% upside)
   - Timeline: 12-18 months

🟢 **Upside Scenario (5% probability)**: AI boom accelerates faster
   - Fair Value: ₹5,000+ (+30% upside)
   - Timeline: 24-36 months if AI becomes dominant revenue driver

KEY RISKS TO MONITOR:
1. **Quarterly Trends**: Watch revenue sequencing, if flat QoQ → concern
2. **Management Attrition**: Loss of key leadership could signal problems  
3. **Client Concentration**: If #1 client > 10% → elevated risk
4. **Dollar Weakness**: Each 5% rupee strength = 2-3% earnings headwind
5. **US Tech Layoffs**: Trend in ex-US hiring could signal spending freezes

RECOMMENDATION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

**OVERALL: HOLD with ACCUMULATE ON DIPS**

SHORT-TERM (3-6 months):
Action: HOLD current 50 shares
- Stock consolidating near resistance @ ₹4,050
- Wait for confirmed breakout above ₹4,100 before adding  
- Stop Loss: ₹3,400 (near intermediate support)
- Profit Taking: 20-30% at ₹4,200-₹4,300, then hold rest

MEDIUM-TERM (6-18 months):
Action: ACCUMULATE ON WEAKNESS
- If stock falls to ₹3,400-₹3,500 → ADD 25 more shares
- This increases position while reducing average cost to ₹3,300
- Target to reach 75-100 shares in next 18 months

1-YEAR TARGET: ₹4,200-₹4,500 (10-17% upside)
- Base Case: ₹4,300 (12% upside) - likely scenario
- Bull Case: ₹4,600 (19% upside) - if AI revenues accelerate
- Bear Case: ₹3,600 (6% downside) - only if growth disappoints

LONG-TERM (5 years):
Action: STRONG HOLD - This is core holding
- TCS is quality compounder in your portfolio
- Expect 13-15% annual returns (capital gains + dividends)
- Position should grow to 100+ shares by 2031
- 5-Year Target: ₹6,500-₹7,000 (70-85% total return including dividends)

WHY HOLD TCS:
✅ Market leader with fortress balance sheet
✅ AI positioning excellent (revenue ramp starting now)
✅ Dividend growing 6-8% annually (good for income)
✅ Geographically diversified (hedges rupee risk)
✅ Management credible and shareholder-friendly
✅ Valuation reasonable for quality + growth combo

ALLOCATION RECOMMENDATION:
- TCS: 20-25% of portfolio (currently at 26%, slightly high but acceptable)
- Can stay at current level as accumulation plans increase position
- Current 50 shares represents solid long-term holding

NEXT STEPS:
1. Continue holding current position
2. Reinvest dividends back into TCS
3. Monitor Q4 FY2026 results (due April 2026) - crucial for growth confirmation
4. If sharp dip to ₹3,400s → use as buying opportunity
5. Review again in 3 months or after earnings

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Analysis Confidence: HIGH (based on recent earnings, clear trends)
Data Sources: Latest earnings reports, web research, technical analysis
Last Updated: March 14, 2026
```

---

## Example 3: Portfolio Rebalancing Decision

### Scenario
Your portfolio is concentrated in IT. You want to know what to reduce and what to add.

### Input
```
@kite-zeroda-portfolio-analyser

I notice my portfolio is 65% in IT sector:
- TCS: 50 shares (₹1,92,500)
- Infosys: 30 shares (₹54,600) 
- Other holdings: HDFC Bank, Reliance, ITC (~15% each)

Market is March 2026. Should I rebalance? What should I sell and buy?
My investment horizon: 5 years
Risk tolerance: Moderate (okay with 20-25% drawdowns)
```

### Agent Response
```
PORTFOLIO ANALYSIS & REBALANCING STRATEGY
March 14, 2026
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

CURRENT ALLOCATION (65% IT Risk):
IT Sector:       65%  → TOO HIGH (ideal: 25-30%)
Financials:      25%  → ACCEPTABLE
Consumption:      8%  → UNDERWEIGHT (ideal: 15-20%)
Energy/Others:    2%  → MINIMAL
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

REBALANCING PLAN

STEP 1: REDUCE IT CONCENTRATION (Target: 30%)
Option A - Gradual Sell:
SELL Infosys Partially:
- Current: 30 shares @ ₹1,820 = ₹54,600
- Action: SELL 12-15 shares (at ₹1,900-₹2,000 levels)
- Timing: Next 2-3 months as stock appreciates
- Proceeds: ~₹24,000-₹30,000
- Rationale: Lock in 90%+ gains, keep 15 shares for core holding

Keep TCS Fully:
- TCS remains quality core holding
- Don't reduce (reduce other positions instead)

Option B - Aggressive Sell (if you want faster rebalancing):
- SELL 8-10 Infosys shares immediately (even at current ₹1,820)
- Takes 3% of portfolio pressure off

STEP 2: INCREASE UNDERWEIGHTS (Target: 15-20%)
With ₹24,000-₹30,000 proceeds, ADD:

**Consumer Discretionary (8% → 15%):**
- Add: Titan Company (luxury, wedding demand strong)
- Entry: ₹2,600-₹2,800/share
- Quantity: 8-10 shares
- Rationale: India growth story, rising consumer spending

**Quality Financials (25% → 30%):**
- Add: Kotak Mahindra Bank (more aggressive than HDFC)
- Entry: ₹1,800-₹1,900/share  
- Quantity: 15-18 shares
- Rationale: Cost of capital declining, rate cuts coming

REVISED ALLOCATION (After Changes):
IT Sector:        30% ✓ Balanced
Financials:       30% ✓ Quality lending exposure
Consumption:      25% ✓ India consumption growth
Pharma/Other:     15% ✓ Diversification

EXPECTED OUTCOMES (5-Year):
Conservative: 11% CAGR (portfolio growth to ₹3.5L)
Base Case:    14% CAGR (portfolio growth to ₹4.2L)
Bull Case:    17% CAGR (portfolio growth to ₹5.1L)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
IMPLEMENTATION:
Month 1: SELL 12 Infosys (at ₹1,900+) → Proceeds: ₹23K
Month 2: BUY 8 Titan, 12 Kotak
Month 3: Hold and monitor

RISK: Lower if done gradually (dollar-cost averaging)
```

---

## Example 4: Should I Book Profits?

### Scenario
You've made 90% gains on a stock and unsure if you should exit.

### Input
```
@kite-zeroda-portfolio-analyser

I've made fantastic returns on Infosys:
- 30 shares purchased 2020-01-01 @ ₹950/share (₹28,500 invested)
- Now trading @ ₹1,820 (₹54,600 value, +91% gain)

The gain is amazing but I'm worried about:
1. Market correction incoming
2. Giving back profits

Should I take profits? If yes, partially or fully?
How much should I sell?
```

### Agent Response
```
PROFIT-TAKING ANALYSIS - INFOSYS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Your Position:
- 30 shares @ ₹950 average cost = ₹28,500 invested
- Current value: ₹54,600
- Unrealized gain: ₹26,100 (+91%) ← Excellent returns!

THE PROFIT-TAKING DILEMMA (Common Question):

Fear of market corrections is understandable, but let's be logical:

INFOSYS VALUATION & MOMENTUM:
- P/E Ratio: 24x (fair, not overvalued)
- Growth Rate: 12-15% expected (matches growth)
- Resistance @ ₹1,900-₹2,000 (room for 10-12% more upside)
- Technical: Still in uptrend, not extended

Market Timing Reality:
❌ MISTAKE: "It's up 90%, must be due for correction"
   (Stocks can go 90% → 200% before correcting)

✅ TRUTH: Strong fundamentals + uptrend = can continue higher

RECOMMENDED STRATEGY: "SCALED EXIT"
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

THIS IS THE SMART WAY:

Tranche 1 - Immediate: SELL 8 shares
- Achieve: ₹14,560 proceeds
- Locks: ₹13,960 profit (98% REALIZED GAIN)
- Keeps: 22 shares for potential upside
- Action: Sell TODAY at market price

Tranche 2 - Medium (1-2 weeks): SELL 7 more shares
- Sell at: ₹1,900 or above
- Proceeds: ₹13,300 (if at ₹1,900)
- Locks in: ₹12,650 additional profit
- Keeps: 15 shares with cost base reduced below ₹300/share

Tranche 3 - Long-term: HOLD remaining 15 shares (forever?)
- Cost base: <₹600/share after selling 15 shares
- If reaches ₹2,500-₹3,000 = HUGE wealth creation
- Dividend income: ₹900-₹1,500/year on 15 shares
- "Free" holdings after profit-taking

RESULT:
✓ Booked ₹28,000 in profits (covered original investment + 100%)
✓ Still hold 15 shares = ₹27,300 value (continue upside)
✓ Totally eliminated downside risk
✓ Peace of mind achieved

IF MARKET CRASHES 30% TOMORROW:
- 15 shares worth: ₹12,700 (still 110% gain vs original ₹600 cost)
- You don't lose - you're still profitable!

IF MARKET SURGES 50% MORE:
- 15 shares worth: ₹40,950 (+450% total gain!)
- You participated in upside

WHAT TO DO WITH ₹27,000 PROCEEDS:
Option 1: Buy 2-3 other quality stocks (diversify)
Option 2: Add to underweight sectors (I recommended Titan + Kotak)
Option 3: Keep as 3-month emergency cash buffer
Option 4: Deploy gradually if market corrects (buy dip)

BOTTOM LINE:
📍 DON'T hold hoping for ₹2,500 while risking a ₹1,200 crash
📍 DO crystallize profits while staying invested
📍 This scaled approach gives you 80% profit + 80% exposure

ACTION ITEMS:
1. SELL 8 shares TODAY (market order) - lock in first tranche
2. Set limit orders for 7 shares @ ₹1,900-₹1,950
3. Hold 15 shares indefinitely (this is your core position)
4. Use proceeds to add underweight sectors

Your 91% gain is WELL DESERVED. Now PROTECT it while keeping upside.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Example 5: Emergency - Stock Falling, Should I Panic Sell?

### Scenario
Market correction and one of your stocks is falling hard. You're wondering if you should exit.

### Input
```
@kite-zeroda-portfolio-analyser

Market is falling (Nifty down 8% in last 3 weeks).
My HDFC Bank position is down 12%:
- 25 shares purchased 2021-01-01 @ ₹1,200
- Now trading @ ₹1,185 (down from ₹1,620 just 2 months ago)
- Current loss: -₹875 (6.5% of my portfolio value)

Should I panic sell and move to cash? 
Or is this a buying opportunity?
```

### Agent Response
```
MARKET CORRECTION PANIC ANALYSIS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

HDFC Bank Situation:
- Original cost: ₹1,200
- Current price: ₹1,185 (down -1.3% from entry)
- Peak price: ₹1,620 (down -26.8% from peak)
- Current status: STILL PROFITABLE (bought at ₹1,200!)
- Panic level: MEDIUM (but NOT justified)

THE TRUTH ABOUT PANIC:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

❌ PANIC SELLS ARE HOW MONEY IS LOST
- You sell at lows (worst time)
- Market recovers (you're left in cash earning nothing)
- You FOMO buy back at highs (cycle repeats)

YOUR ACTUAL SITUATION:
✓ Still profitable (up from ₹1,200 entry)
✓ Dividend:₹26/share annual (2.2% yield while holding)
✓ Company fundamentals unchanged
✓ Banks ALWAYS recover after corrections

CONTEXT CHECK:
Market Correction = Normal! Happens every 1-2 years:
- May 2024: Nifty down 8% 
- Sep 2023: Nifty down 6%
- Recovered fully in 3-4 months

HDFC BANK ANALYSIS:
- ROE: 16.8% (excellent for banker)
- C-D Ratio: 78% (healthy)
- NIM: 3.2% (stable despite rate competition)
- Loan Growth: 10-12% annual

Worst-case scenario for HDFC:
- If India GDP growth slows from 5.5% to 3.5% → earnings fall 15%
- This would put stock at ₹1,000-₹1,100
- But you're still not underwater! (entry was ₹1,200)

SHOULD YOU SELL? 
NO. Here's why:
---
If you sell @ ₹1,185:
- You book ₹875 losses
- You move to "safety" (cash earns 0%)
- When market recovers in 3 months → you're sitting outside

What actually happens next 3-6 months:
- Nifty gains 12-15% (historical average recovery)
- HDFC Bank gains 15-18% (banking sector leads recovery)
- Your 25 shares @ ₹1,185 = could reach ₹1,350-₹1,400

Difference:
- If you HOLD: ₹33,750 - ₹29,625 = +₹4,125 gain (14%)
- If you SELL then BUY BACK: You miss the recovery entirely

WHAT YOU SHOULD DO INSTEAD:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

OPTION A - DO NOTHING (RECOMMENDED):
✓ Hold 25 shares
✓ This is a 5-year position for you
✓ Dividend keeps coming (₹26/share in March)
✓ Volatility is your friend, not enemy = you can buy more at ₹1,100

OPTION B - BE SMART & ADD (BEST IF YOU HAVE CASH):
✓ If this fall continues to ₹1,100 → BUY 25 MORE shares
✓ Average cost would drop to ₹1,150
✓ You'd benefit most when stock recovers to ₹1,400+

OPTION C - PARTIAL REBALANCE:
✓ Hold core 25 shares (never sell)
✓ Add 10-15 shares at ₹1,100-₹1,150 if correction deepens
✓ By 2031, 50 shares of HDFC = massive wealth

ACTION LIST:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

❌ DO NOT SELL at ₹1,185 (locking losses + missing recovery)

✓ DO HOLD and collect ₹650 dividend this quarter

✓ DO SET BUY LIMITS at ₹1,100 (add 25 shares if hits)

✓ DO CHECK again in 2 months - will likely be at ₹1,300+

✓ DO IGNORE daily noise - you're 5-year investor

✓ DO UNDERSTAND: Wealth is made during corrections, not booms
  (Buy when blood on streets, not when party is hot!)

WORST CASE vs BEST CASE (1-Year):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

If you HOLD:
- Worst: Stock stays at ₹1,200 (break-even) + ₹650 dividend = ₹30,275 total
- Best: Stock reaches ₹1,400 = ₹35,000 + ₹650 dividend = ₹35,650

If you PANIC SELL @ ₹1,185:
- You lock ₹25,875 realized
- In cash earning 0% = ₹25,875 in 1 year
- Miss ₹9,775 gain from recovery (LOST FOREVER)

REAL RETURNS:
HOLD: +₹4,375 in 1 year (13%)
PANIC SELL: -₹9,775 opportunity loss (versus recovery scenario)

CONCLUSION:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Do NOT let a 26% drawdown from peak fool you when you're:
- Still profitable from entry
- Receiving dividends
- Holding quality company with stable fundamentals

Market corrections are GIFTS to long-term investors.
Don't turn them into MISTAKES through panic selling.

Stay calm, hold strong, and remember: Every investor millionaire 
has held through at least 2-3 major corrections.

This is yours. Don't blow it.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

RISK ACKNOWLEDGMENT:
If India economy enters recession (low probability now) = could overshoot to ₹800-₹900
But: This is extreme tail risk, not expected scenario
Your diversification (TCS, Infosys, Reliance, ITC) hedges this

FINAL GUIDANCE: HOLD and BREATHE.
```

---

## Common Queries Reference

### Quick Command Examples

```
# Get quick portfolio view
@kite-zeroda-portfolio-analyser
My portfolio is [stocks list here]
```

```
# Deep dive on one stock
@kite-zeroda-portfolio-analyser  
Detailed analysis on [stock name]:
- Current holdings: [qty] shares
- Entry: [date] @ ₹[price]
- Should I buy/sell/hold?
```

```
# Sector analysis
@kite-zeroda-portfolio-analyser
Analyze my IT sector:
- TCS: 50 shares
- Infosys: 30 shares
Are these overweight? What else should I buy?
```

```
# Market volatility advice
@kite-zeroda-portfolio-analyser
Market just fell 5%. Should I:
1. Panic sell everything?
2. Keep holding?
3. Buy the dip?
What does technical and fundamental analysis suggest?
```

---

*Usage Examples - Kite Zeroda Portfolio Analyzer*
*Last Updated: March 14, 2026*
