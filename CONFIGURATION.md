# Portfolio Analyzer - Configuration Guide

## Agent Configuration Details

The Kite Zeroda Portfolio Analyzer is configured with the following specifications:

### YAML Configuration

```yaml
name: Kite Zeroda Portfolio Analyzer
description: Professional portfolio analysis agent for Indian and global stocks. Analyzes purchase history, current performance, market trends, and provides buy/sell/hold recommendations with short-term and long-term insights based on financial expertise and latest market news. Integrates with Kite/Zeroda MCP for real-time portfolio and market data.
tools: ["read", "search", "web", "edit", "kite/*"]
target: vscode
user-invocable: true
disable-model-invocation: false
mcp-servers:
  kite:
    type: local
    url: "https://mcp.kite.trade/mcp"
    tools: ["*"]
```

### Configuration Explanation

| Property | Value | Purpose |
|----------|-------|---------|
| **name** | Kite Zeroda Portfolio Analyzer | Display name in VS Code Copilot |
| **description** | Professional portfolio analysis... | Shows up when selecting agents |
| **tools** | read, search, web, edit, kite/* | Agent can read files, search workspace, fetch web content, create reports, access Kite MCP server |
| **target** | vscode | Primarily designed for VS Code (also works with GitHub Copilot) |
| **user-invocable** | true | Users can manually select this agent |
| **disable-model-invocation** | false | Agent can also be auto-suggested by Copilot |
| **mcp-servers** | kite config | Configures Kite/Zeroda MCP server for live portfolio access |

### MCP Server Configuration Details

```yaml
kite:
  type: local                           # Local MCP server type
  url: "https://mcp.kite.trade/mcp"    # Kite MCP endpoint
  tools: ["*"]                          # Enable all available Kite tools
```

**What This Enables:**
- Direct access to your Kite account
- Live portfolio holdings and prices
- Transaction history with exact purchase details
- Market data and indices
- Real-time P&L calculations
- Automatic data retrieval without manual entry

---

## Kite MCP Server Setup & Usage

### What is Kite MCP?

Kite MCP (Model Context Protocol) is a secure bridge between Copilot and your Zerodha Kite account. It enables:

✅ **Live Portfolio Data**: All holdings, quantities, purchase details  
✅ **Real-Time Prices**: Current prices directly from Kite  
✅ **Transaction History**: Exact purchase dates and prices  
✅ **Market Data**: Indices, sectors, watchlists  
✅ **Instant Analysis**: No manual data entry needed  
✅ **Secure Connection**: OAuth-based, encrypted communication  

### Quick MCP Setup (5 minutes)

1. **Open VS Code Settings** (Ctrl+, or Cmd+,)
2. **Search "mcp"** and click "Edit in settings.json"
3. **Add this configuration:**
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
4. **Save and Restart VS Code** (Ctrl+S, then close and reopen)
5. **Authorize**: Ask agent `Get my portfolio analysis` → Click authorize → Login
6. **Done!** Agent now has live access to your Kite account

### Verify MCP is Working

In Copilot Chat, type:
```
/mcp list
```

You should see `kite` in the output if properly configured.

### Using MCP Once Configured

Simply ask:
```
@kite-zeroda-portfolio-analyser
Get my portfolio analysis
```

Agent automatically:
- Fetches all your holdings from Kite
- Gets live prices and P&L
- Provides instant analysis without manual data entry

### Troubleshooting MCP

| Issue | Solution |
|-------|----------|
| Kite not in `/mcp list` | Restart VS Code completely, wait 30 seconds. Check JSON syntax. |
| Authorization fails | Clear browser cookies from kite.trade, try again. |
| MCP stops working | Run Cmd/Ctrl+Shift+P → "Reload Window" to restart extension. |
| Permission denied error | Re-authorize and grant all portfolio access permissions. |

### Security with Kite MCP

🔒 **What's Protected:**
- OAuth 2.0 authentication (no passwords stored)
- HTTPS encrypted connection
- Token-based access (revocable anytime)
- Limited to portfolio data only (no trading/withdrawals)
- Hosted on secure Kite infrastructure

❌ **Never:**
- Share authorization tokens
- Use MCP on public computers without logout
- Leave MCP connected unattended

### Revoking MCP Access Anytime

1. Login to Kite account
2. Settings → Connected Applications
3. Find and click "Revoke" next to Kite MCP app
4. All access is immediately revoked

---

### Available Tools Explained

#### 1. **read** (Reading Files)
- Read Excel portfolios (`.xlsx`, `.csv`)
- Parse PDF statements from Kite
- Extract portfolio data from shared documents

**Example:** When you share an Excel file with your portfolio, the agent reads it

#### 2. **search** (Search Files)
- Find portfolio files in workspace
- Locate previous analysis documents
- Search for saved recommendations

**Example:** `@kite-zeroda-portfolio-analyser find my previous portfolio files`

#### 3. **web** (Web Search & Fetch)
- Search for latest stock news
- Fetch company announcements
- Get current market data and indices
- Research sector trends
- Monitor global economic news

**Example:** Agent automatically searches for latest TCS news when analyzing the stock

#### 4. **edit** (Create Reports)
- Create detailed analysis documents
- Generate portfolio summary reports
- Save recommendations as markdown/PDF

**Example:** Agent creates a comprehensive analysis report and saves it

#### 5. **kite/*** (Kite MCP Access - When Configured)
- **Fetch holdings**: Get all your portfolio positions
- **Get prices**: Live prices for all holdings
- **Transaction history**: Exact purchase details and dates
- **Market data**: Indices, sectors, watchlist data
- **P&L tracking**: Real-time gains/losses

**When Available**: Only when Kite MCP is configured and authorized
**Requires**: Valid Zerodha account with active Kite access
**Security**: OAuth-based, token authentication, revocable access

**Example Usage:**
```
User: Get my portfolio analysis
Agent: [Using kite/* tools] Fetching from your Kite account...
Agent: Retrieved 8 holdings | Current value: ₹5.2L | Total gain: +18.5%
Agent: [Provides instant analysis using live data]
```

**When Kite MCP is NOT configured:**
- Agent still works with manual data entry
- Uses "read" tool for Excel/CSV files
- Uses "web" tool for market data & current prices
- Analysis takes slightly longer (requires manual inputs)

---

## Input Data Formats Supported

### 1. **Direct Chat Input**
```
@kite-zeroda-portfolio-analyser

My portfolio:
- TCS: 50 shares, bought 2021-06-15 @ ₹3,100
- Infosys: 30 shares, bought 2020-01-01 @ ₹950
- ITC: 100 shares, bought 2022-03-10 @ ₹190
```

### 2. **Kite Export Format**
The agent can parse Kite terminal exports:

```
Instrument	Quantity	Avg Cost	Current Price	Change
TCS	            50	      3100	      3500	        13.2%
Infosys	        30	      950	       1750	        84.2%
HDFC Bank	    50	      1200	      1600	        33.3%
```

### 3. **Excel Format**
```
Stock Name | Ticker | Qty | Purchase Date | Purchase Price | Current Price
TCS        | TCS    | 50  | 2021-06-15    | 3100          | 3500
Infosys    | INFY   | 30  | 2020-01-01    | 950           | 1750
```

### 4. **JSON Format**
```json
{
  "portfolio": [
    {
      "stock": "TCS",
      "ticker": "TCS",
      "quantity": 50,
      "purchase_date": "2021-06-15",
      "purchase_price": 3100
    },
    {
      "stock": "Infosys",
      "ticker": "INFY",
      "quantity": 30,
      "purchase_date": "2020-01-01",
      "purchase_price": 950
    }
  ]
}
```

---

## Analysis Output Structure

### Quick Analysis Output

The agent formats quick analysis in this structure:

```
STOCK NAME - TICKER
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Holdings: [Qty] × Purchase: [Date] @ ₹[Price]
Current:  [Current Price] | Change: ₹[Abs] ([%])
5Y Perf:  [Status]
Range:    Min ₹[Min] | Max ₹[Max] (since purchase)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Recommendation: [STRONG BUY / BUY / HOLD / SELL / STRONG SELL]
Thesis: [1-2 line summary]
```

### Detailed Analysis Output

For detailed analysis, the agent provides:

1. **Portfolio Position**: Current holdings and performance metrics
2. **Market Context**: Indian and global economic situation
3. **Company Analysis**: Latest news, financial health, competitive position
4. **Technical Analysis**: 3-6 month outlook with support/resistance levels
5. **Fundamental Analysis**: 1-5 year outlook with valuation metrics
6. **Recommendation**: Clear action items with price targets
7. **Risk Assessment**: Downside scenarios and warning signs

---

## Example Workflow

### Step 1: Share Portfolio
```
@kite-zeroda-portfolio-analyser

Here's my current portfolio from Kite:
[Paste portfolio data]
```

### Step 2: Get Quick Overview
Agent responds with table showing:
- Each holding
- Current price vs. purchase price
- Percentage gain/loss
- Max/min prices since purchase
- Quick recommendation

### Step 3: Request Detailed Analysis
```
Give me detailed analysis on the top 3 performing stocks. 
I want to know if I should book profits or continue holding.
What's your 1-year target for each?
```

### Step 4: Receive Deep Dive
Agent researches:
- Recent company news and announcements
- Earnings performance and guidance
- Peer comparison and valuation
- Technical chart analysis
- Risk factors and downside catalysts
- Specific buy/sell recommendations with price targets

### Step 5: Get Portfolio Recommendations
```
Based on current market conditions (March 2026), 
what changes should I make to my portfolio?
```

Agent provides:
- Concentration risks (e.g., 60% in IT)
- Sector rotation suggestions
- Dividend yield optimization
- New buying opportunities within your risk profile

---

## Agent Behavior Specifications

### Response Style
- ✅ Bold and unambiguous recommendations
- ✅ Data-driven with specific numbers
- ✅ Transparent about limitations
- ✅ Professional financial advisor tone
- ✅ Honest about risks and negatives

### Analysis Scope

**Short-Term (3-6 months):**
- Technical analysis and price action
- Support and resistance levels
- Momentum indicators and trading signals
- Profit-taking opportunities
- Stop-loss recommendations
- Entry/exit price targets

**Long-Term (1-5 years):**
- Company fundamental strength
- Revenue and earnings growth
- Dividend sustainability
- Industry positioning
- Wealth creation potential
- Position sizing for portfolio

### Market Context Considered
- **Indian Economic**: Sensex, Nifty, inflation, RBI policy
- **Global Economic**: Fed rates, global inflation, recession risk, geopolitical events
- **Sector Trends**: Industry-specific catalysts and headwinds
- **Company-Specific**: Management changes, product launches, regulatory issues

---

## Customization & Extensions

### Adding MCP Server Integration

To enhance the agent with real-time market data, you can add MCP servers:

```yaml
mcp-servers:
  kite-mcp:
    type: local
    command: kite-data-server
    args: []
    tools: ["*"]
    env:
      KITE_API_KEY: ${{ secrets.KITE_API_KEY }}
```

### Extending Tools

To add more capabilities:

1. **Option 1**: Extend the `tools` list in the YAML
2. **Option 2**: Configure repository-level MCP servers
3. **Option 3**: Create related agents that specialize in sub-tasks

---

## Performance Metrics Calculated

The agent automatically calculates:

| Metric | Definition | Use Case |
|--------|-----------|----------|
| Absolute Return | Current Price - Purchase Price | See profit/loss in rupees |
| Percentage Return | (Return / Purchase Price) × 100 | Compare against other investments |
| Maximum Gain | (Max Price - Purchase Price) / Purchase Price | What was best profit potential |
| Maximum Loss | (Min Price - Purchase Price) / Purchase Price | Worst drawdown experienced |
| Days Held | Current Date - Purchase Date | Understand holding period |
| Annualized Return | Return ^ (1/Years Held) × 100 | Fair comparison with other assets |
| Volatility | Price standard deviation | Understand risk level |

---

## Troubleshooting

### Issue: Agent says "Cannot fetch real-time prices"
**Solution:** Web search is working but prices may not update instantly. Verify with Kite terminal or NSE website for current prices.

### Issue: Portfolio data not being parsed correctly
**Solution:** Ensure you provide clear structure with: Stock name, Quantity, Purchase date, Purchase price. Use one of the supported formats above.

### Issue: Agent recommends holding, but I want to know about selling
**Solution:** Ask specifically: "What's the best price level to exit this position?" or "If you had to sell tomorrow, what target would you set?"

### Issue: Analysis seems outdated
**Solution:** Request the agent to search for latest news: "Check latest news on TCS and update your recommendation"

---

## Tips for Best Results

1. **Complete Data**: Provide exact purchase dates and prices
2. **Current Prices**: Share current prices when available for accurate analysis
3. **Your Goals**: Tell the agent your investment horizon (1 year, 5 years, etc.)
4. **Risk Profile**: Ask recommendations suitable to your risk tolerance
5. **Portfolio Size**: Let the agent know your approximate portfolio size for position sizing advice
6. **Market Timing**: Ask about current market conditions before making decisions

---

*Configuration Guide - Kite Zeroda Portfolio Analyzer v1.0*
