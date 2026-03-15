# Quick Start Guide - 2 Minutes Setup

Get started with the Kite Zeroda Portfolio Analyzer in just 2 minutes.

---

## ⚡ Option 1: FASTEST - Auto-Connect Kite Portfolio (MCP) - 1 Minute

### No Manual Data Entry!

1. **Ensure settings have Kite MCP:**
   - Open VS Code settings (Ctrl+, or Cmd+,)
   - Search "mcp" and add to settings.json:
   ```json
   {
     "mcp": {
       "servers": {
         "kite": {
           "url": "https://mcp.kite.trade/mcp"
         }
       }
     }
   }
   ```
   - Save and restart VS Code

2. **Open Copilot Chat and type:**
   ```
   @kite-zeroda-portfolio-analyser
   Get my portfolio analysis
   ```

3. **Click Authorize when prompted**
   - Login to Zerodha
   - Allow permissions
   - Agent fetches everything automatically

4. **That's it!** ✅
   - Agent shows your portfolio with live prices
   - No manual work needed
   - Use instantly anytime: `Get my portfolio analysis`

### Why Use MCP?
- ✅ **Real-time prices** from Kite
- ✅ **Zero manual entry** - just authorize once
- ✅ **Always accurate** - uses live transaction history
- ✅ **Fastest analysis** - instant access to your data

---

## ⚡ Option 2: SIMPLE - Manual Data Entry - 2 Minutes

### If MCP doesn't work or you prefer manual entry:

### If MCP doesn't work or you prefer manual entry:

### Step 1: Activate the Agent (30 seconds)
Open VS Code with GitHub Copilot Chat. Type:

```
@kite-zeroda-portfolio-analyser
```

(It will appear in the list - click to select)

### Step 2: Gather Your Portfolio Data (1 minute)
Collect information about your stocks:

```
Stock Name | Quantity | Purchase Date | Purchase Price
TCS        | 50       | 2021-06-15    | ₹3,100
Infosys    | 30       | 2020-01-01    | ₹950
HDFC Bank  | 25       | 2021-01-01    | ₹1,200
```

Or have handy:
- Kite terminal screenshot
- Excel portfolio file
- List of holdings from email

### Step 3: Share Your Portfolio (30 seconds)
In Copilot chat with agent selected, paste:

```
@kite-zeroda-portfolio-analyser

My portfolio stocks:
- TCS: 50 shares, bought 2021-06-15 @ ₹3,100
- Infosys: 30 shares, bought 2020-01-01 @ ₹950
- HDFC Bank: 25 shares, bought 2021-01-01 @ ₹1,200

Give me quick overview.
```

### Step 4: Review Quick Summary (30 seconds)
Agent returns portfolio table with:
- Current prices
- Gain/loss percentages
- Quick recommendations

### Step 5: Ask for Details (Optional, 0 seconds)
```
Give me detailed analysis on Infosys. Should I hold or sell?
```

**That's it! You're using the agent.**

---

## 🎯 Most Common Use Cases

### With Kite MCP (Easiest)
```
@kite-zeroda-portfolio-analyser
Get my portfolio analysis
```
*Time: 10 seconds*

### Portfolio Check (Every Morning)
```
@kite-zeroda-portfolio-analyser

What's my current portfolio P&L?
```
*Time: 20 seconds*

### Decision Making (Before Trading)
```
@kite-zeroda-portfolio-analyser

I'm thinking of selling TCS. Current price ₹3,850.
Should I sell now or wait? What's your target?
```
*Time: 1 minute*

### Market Panic Handling
```
@kite-zeroda-portfolio-analyser

Market is down 5%. Help me understand:
1. Should I panic sell?
2. Should I hold?
3. Should I buy more?
```
*Time: 2 minutes*

### Profit Taking
```
@kite-zeroda-portfolio-analyser

I'm up 80% on Infosys. Should I take profits?
If yes, how much? If no, what's your target?
```
*Time: 1 minute*

### Portfolio Rebalancing
```
@kite-zeroda-portfolio-analyser

My portfolio is 65% in IT. I want to rebalance.
What should I sell? What should I buy?
My timeline is 5 years.
```
*Time: 3 minutes*

---

## 📋 Checklist Before Each Analysis

Before asking the agent for analysis, have ready:

- [ ] Stock name or ticker (e.g., TCS, INFY, HDFC)
- [ ] Quantity of shares owned (e.g., 50 shares)
- [ ] Purchase date (e.g., 2021-06-15)
- [ ] Purchase price (e.g., ₹3,100)
- [ ] Your investment timeline (1 year? 5 years?)
- [ ] Your risk tolerance (aggressive/moderate/conservative)
- [ ] Current market context (if worried about crash, etc.)

**More details = Better analysis**

---

## 💡 Pro Tips

### Tip 1: Be Specific
❌ "Should I buy TCS?"
✓ "I have ₹1 lakh. Should I buy TCS @ ₹3,850 or wait for dip to ₹3,500?"

### Tip 2: Ask Follow-ups
After initial response:
```
What's your 1-year target?
Should I add more at lower prices?
Will this survive market crash?
```

### Tip 3: Share Context
```
I'm bearish on market (inflation rising). Should I reduce exposure?
OR
I have 5 years to retirement. What stocks should I own?
```

### Tip 4: Use Web Search Feature
The agent can search latest news. Ask:
```
Check latest news on TCS and give updated view.
```

### Tip 5: Portfolio vs Single Stock
- **Portfolio View**: Share 5-10 stocks → get sector analysis + rebalancing guidance
- **Single Stock**: Dive deep on one holding → get detailed thesis

---

## 🚫 What NOT to Expect

❌ **Real-time prices** (verify with Kite)
❌ **Trading signals** (use technical indicators for that)
❌ **Guaranteed predictions** (markets surprise everyone)
❌ **Personal financial advice** (agent provides analysis, you decide)

---

## ✅ What TO Expect

✅ Professional in-depth analysis
✅ Clear buy/sell/hold recommendations
✅ Short-term AND long-term outlook
✅ Risk assessments
✅ Supporting data and reasoning
✅ Web-based latest news when you ask
✅ Portfolio optimization suggestions
✅ Honest opinions (good AND bad scenarios)

---

---

## 🆘 Troubleshooting

### MCP-Related Issues

| Problem | Solution |
|---------|----------|
| **"Kite MCP not found"** | Restart VS Code after adding settings. Wait 30 seconds for MCP to initialize. |
| **Authorization fails** | Clear browser cookies for kite.trade, then try authorization again. |
| **"Permission denied" error** | Ensure you're granting portfolio access permissions when authorizing. |
| **MCP stops working** | Try: Cmd/Ctrl+Shift+P → "Reload Window" to restart Copilot extension. |
| **Can't find mcp in settings** | Update VS Code to latest version (Settings → Check for Updates). |

### General Issues

### Agent says "Need more information"
**Solution**: Provide all details:
- Exact ticker (not just company name)
- Purchase date, not "2-3 years ago"
- Current price if possible

### Agent can't fetch latest prices
**Solution**: Check if MCP is active (it gives live Kite prices). Without MCP, tell it: "Current price is ₹X, analyze based on that"

### Analysis seems outdated
**Solution**: Ask: "Check latest news on [stock] and give updated analysis"

### Recommendation seems to conflict with your view
**Solution**: Remember - agent is data-driven. If conflict:
1. Share why you disagree
2. Ask agent to analyze your specific concern
3. Make final decision yourself (you're the investor)

---

## 📞 When to Use Agent vs When to Verify

| Situation | Use Agent For | Then Verify With |
|-----------|---|---|
| Stock recommendation | Analysis & thesis | Kite, NSE website |
| Current prices | Reference only | Kite terminal (real-time) |
| Latest news | Search & compile | Direct company announcements |
| Buy/sell decisions | Framework & options | Your own gut + recheck data |
| Portfolio allocation | Suggestions | Your financial advisor if you have one |

---

## 🎓 Learning Resources Inside Agent

The agent file includes:
- **Output Format**: How results are structured
- **Analysis Framework**: What gets analyzed
- **Key Instructions**: How the agent makes decisions

Read the .agent.md file to understand how analysis is done.

---

## 📊 Sample Responses You'll Get

### Quick Response (30 seconds)
```
TCS - STRONG HOLD
Holdings: 50 shares | Purchase: 2021-06-15 @ ₹3,100
Current: ₹3,850 | Change: +₹750 (+24.2%)
Recommendation: HOLD (wait for ₹4,100 breakout before adding)
```

### Detailed Response (3 minutes read)
Full analysis with:
- Market context
- Company analysis
- Technical + Fundamental views
- Short-term & long-term recommendation
- Risk assessment
- Specific price targets

---

## 🔄 Regular Usage Pattern

**Daily (2 min)**
- Check portfolio status
- See daily changes

**Weekly (5 min)**
- Review one key holding
- Update watch list

**Monthly (30 min)**
- Detailed analysis on 1-2 stocks
- Portfolio rebalancing check

**Quarterly (1 hour after earnings)**
- Major earnings analysis
- Portfolio performance review
- Adjustments for next quarter

---

## ⚙️ Customizing Agent for Your Needs

The agent can be customized further if you want:
- Real-time stock data integration (MCP servers)
- Custom portfolio tracking
- Automated alerts
- Export analysis as PDF

See `CONFIGURATION.md` for advanced setup.

---

## 🎯 Your First 3 Actions

1. **Right Now**: Collect your portfolio data (3 stocks minimum)
2. **Next 5 min**: Type `@kite-zeroda-portfolio-analyser` → share data
3. **After 1 day**: Ask follow-up question on top holding

**That's how you start.**

---

## 📝 Notes

- Agent gets better with more specific questions
- Use it for analysis, not predictions
- Combine with your research for best decisions
- Update portfolio data monthly
- Review recommendations after 3-6 months

---

**Ready? Open Copilot Chat and start with:**
```
@kite-zeroda-portfolio-analyser

Portfolio overview:
[Your stocks here]
```

*That's it. Agent does the rest.*

---

*Quick Start Guide - Kite Zeroda Portfolio Analyzer v1.0*
*Effective: March 14, 2026*
