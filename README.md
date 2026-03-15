# Personal AI Agents

This repository contains custom GitHub Copilot agents designed for specialized tasks. These agents are configured to work with VS Code and can be used to automate and enhance various analytical and programming workflows.

## Available Agents

### Kite Zeroda Portfolio Analyzer

A professional financial analysis agent for equity portfolio management with expertise in Indian and global stock markets.

**Location:** `.copilot/kite-zeroda-portfolio-analyser.agent.md`

**Purpose:** Comprehensive portfolio analysis including stock performance tracking, buy/sell/hold recommendations, and detailed financial insights.

**Key Features:**
- 🔗 **Kite MCP Integration**: Direct live portfolio access from your Zerodha account (real-time prices & transaction history)
- 📊 Portfolio data ingestion from Kite, Excel, or chat
- 📈 Historical performance analysis (5-year trends)
- 🔍 Real-time market intelligence via web research
- ✅ Short-term (3-6 month) and long-term (1-5 year) analysis
- 🎯 Professional financial recommendations with bold, clear insights
- 📋 Portfolio overview and detailed deep-dives

**Input Methods:**
- NSE/BSE stock tickers
- Kite portal exports
- Excel/CSV portfolio files
- Manual stock input via chat

**Output:**
- Quick portfolio summary view
- Detailed analysis reports with recommendations
- Risk assessments
- Specific action items (Buy/Sell/Hold with price targets)

---

## Custom Agent Configuration

This workspace uses GitHub Copilot's custom agent feature. Agents are stored in the `.copilot/` directory and follow this structure:

```
.copilot/
├── [agent-name].agent.md    # Agent profile with YAML config
└── [other-agents].agent.md
```

### Agent File Format

Each agent uses Markdown with YAML frontmatter for configuration:

```yaml
---
name: Agent Display Name
description: Brief description of the agent's capabilities
tools: ["read", "search", "web", "edit"]
target: vscode
user-invocable: true
disable-model-invocation: false
---

# Agent Instructions and Behavior

[Detailed instructions for the agent]
```

### Available Tools

- **read**: Read file contents (documents, Excel, CSV)
- **search**: Search for files and text patterns
- **web**: Fetch content from URLs and web search
- **edit**: Create and edit files
- **execute**: Run shell commands (when needed)

---

## How to Use the Portfolio Analyzer Agent

### Voice/Chat Interface

1. **Switch to the Kite Zeroda Portfolio Analyzer:**
   - Use the "@" symbol to mention the agent: `@kite-zeroda-portfolio-analyser`

2. **If Kite MCP is Configured (Recommended):**
   - The agent automatically fetches your live portfolio from Kite
   - Just ask: `Get my portfolio analysis` or `Show my holdings and P&L`
   - All data comes directly from your trading account - no manual entry needed!

3. **If Kite MCP is NOT Configured:**
   - Provide Your Portfolio manually as CSV, Excel, or chat input
   - See "Setup Instructions" section below for MCP setup

4. **Get Analysis:**
   - Quick overview: "Give me a summary of my portfolio"
   - Detailed analysis: "Give me a detailed analysis on TCS and ITC stock"
   - Specific questions: "Should I sell TCS or hold? What's the 1-year target?"

### Example Interactions

#### Quick Portfolio Overview
```
@kite-zeroda-portfolio-analyser

Portfolio analysis for:
- TCS (500 shares)
- Infosys (100 shares)
- HDFC Bank (50 shares)
```

**Agent Response:** Quick summary table with current prices, gains/losses, and recommendations

#### Detailed Stock Analysis
```
@kite-zeroda-portfolio-analyser

I want detailed analysis on Infosys. I bought 100 shares on 2024-01-15 at ₹1,800. 
Should I hold long-term or take profits? What's happening with the stock in the current market?
```

**Agent Response:**
- Current market price and gain/loss
- Latest news about Infosys (layoffs, partnerships, earnings)
- Technical analysis for short-term
- Fundamental analysis with valuation metrics
- Specific recommendation with price targets
- Risk assessment

#### Portfolio Rebalancing
```
@kite-zeroda-portfolio-analyser

Here's my portfolio (attached Excel file). 
My investment horizon is 5 years. What should I do - BUY, SELL or HOLD each stock?
```

---

## Setup Instructions

### For VS Code Users - Option 1: With Kite MCP (Recommended ⭐)

**Benefits of Kite MCP:**
- ✅ Live portfolio data directly from your Kite account
- ✅ Real-time stock prices and P&L
- ✅ No manual data entry required
- ✅ Instant analysis after authorization

**Quick Setup (5 minutes):**

1. **Open VS Code Settings**
   - Press `Ctrl+,` (Windows/Linux) or `Cmd+,` (Mac)
   - Search for "mcp" in the settings search

2. **Edit settings.json**
   - Click "Edit in settings.json" link
   - Or: File → Preferences → Settings → Open Settings (JSON)

3. **Add Kite MCP Configuration**
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

4. **Save and Restart VS Code**
   - Press `Ctrl+S` to save
   - Restart VS Code completely

5. **Authorize Kite Account**
   - Open Copilot Chat
   - Ask: `@kite-zeroda-portfolio-analyser Get my portfolio analysis`
   - Agent will prompt for Kite authorization
   - Click authorize and log in with your Zerodha account
   - Allow portfolio access permissions

6. **You're Done!**
   - Agent now has live access to your portfolio
   - Use it anytime: `Get my portfolio analysis`

**Troubleshooting MCP:**
- Can't find MCP settings? → Update VS Code to latest version
- Authorization fails? → Clear kite.trade cookies and try again
- MCP not showing up? → Restart VS Code completely and wait 30 seconds

### For VS Code Users - Option 2: Manual Data Entry (Alternative)

If you prefer not to use MCP or have connection issues:

1. **Clone or download this repository** to your workspace
2. **Share your portfolio data manually:**
   ```
   @kite-zeroda-portfolio-analyser
   
   My portfolio:
   - TCS: 50 shares, bought 2021-06-15 @ ₹3,100
   - Infosys: 30 shares, bought 2020-01-01 @ ₹950
   - ITC: 100 shares, bought 2022-03-10 @ ₹190
   ```

3. **Upload portfolio file (Excel/CSV):**
   - Export from Kite
   - Attach to chat
   - Agent will parse and analyze

4. **The agent is automatically discovered** from the `.copilot/` directory
5. **Activate the agent** by using `@kite-zeroda-portfolio-analyser` in Copilot chat
6. **Start analyzing** your portfolio

### For GitHub.com Users

If setting up at the repository level:

1. Store agent profiles in `.github/copilot/` directory
2. Configure repository MCP servers if needed for real-time market data
3. The agent will be available in GitHub Copilot chat context

### Additional Resources

For detailed MCP setup instructions, see: [MCP_SETUP_GUIDE.md](MCP_SETUP_GUIDE.md)

---

## Agent Behavior Details

### What The Agent Does Well

✅ Analyzes stock purchase vs. current price  
✅ Provides 5-year historical performance context  
✅ Searches web for latest news and company updates  
✅ Gives bold, professional financial recommendations  
✅ Distinguishes between short-term (3-6 month) and long-term (1-5 year) strategies  
✅ Considers Indian and global market context  
✅ Calculates gains/losses from purchase date  
✅ Identifies support/resistance and technical levels  

### Limitations

⚠️ Data is as current as the agent's knowledge cutoff + web searches  
⚠️ Not real-time pricing (recommend cross-checking with Kite/NSE)  
⚠️ Historical analysis limited to publicly available information  
⚠️ Recommendations are based on technical and fundamental analysis, not trading signals  
⚠️ Always verify recommendations with current market data before executing trades  

---

## Best Practices

1. **Provide Complete Data**: Include purchase dates and prices for accurate analysis
2. **Be Specific**: Ask about specific stocks or scenarios rather than vague questions
3. **Trust but Verify**: Cross-check recommendations with current market data
4. **Understand Your Risk**: The agent provides analysis, but you make final decisions
5. **Regular Updates**: Request analysis updates as market conditions change
6. **Portfolio Perspective**: Share your entire portfolio for better allocation recommendations

---

## Creating Additional Agents

To create more custom agents:

1. Create a new `.agent.md` file in the `.copilot/` directory
2. Add YAML frontmatter with agent configuration
3. Write detailed instructions for the agent's behavior
4. Reference the [GitHub Custom Agents Configuration Documentation](https://docs.github.com/en/copilot/reference/custom-agents-configuration)

---

## Resources

- [GitHub Copilot Custom Agents Documentation](https://docs.github.com/en/copilot/how-tos/use-copilot-agents)
- [Custom Agents Configuration Reference](https://docs.github.com/en/copilot/reference/custom-agents-configuration)
- [VS Code Copilot Documentation](https://code.visualstudio.com/docs/copilot)

---

## Notes

- Agents use the latest available model in your environment
- Web search capability requires internet connectivity
- Market data comes from public sources and web searches
- For real-time Kite data integration, you may want to set up MCP servers

---

*Last Updated: March 14, 2026*
