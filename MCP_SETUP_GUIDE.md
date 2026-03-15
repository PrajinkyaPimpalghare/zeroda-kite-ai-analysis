# Kite MCP Setup Guide

**Complete Instructions for Connecting Your Zerodha Kite Account to Portfolio Analyzer**

---

## What is Kite MCP?

Kite MCP (Model Context Protocol) creates a direct, secure connection between the Portfolio Analyzer agent and your Zerodha Kite trading account. 

### Benefits

✅ **No Manual Data Entry**: Agent fetches portfolio automatically  
✅ **Live Prices**: Real-time stock prices from Kite  
✅ **Exact Details**: Precise purchase dates and prices from transactions  
✅ **Instant Analysis**: Analysis available immediately after connecting  
✅ **Secure**: OAuth-based authentication, revocable anytime  
✅ **Fast**: Eliminates copy-paste workflow  

### What MCP Can Access

✅ Can Access:
- Current holdings and quantities
- Purchase dates and prices
- Transaction history
- Current market prices
- Portfolio P&L
- Watchlists

❌ Cannot Access:
- Bank account information
- Withdrawal/deposit details
- Trading permissions or execution
- Personal identity details beyond portfolio

---

## Prerequisites Checklist

Before starting setup, ensure you have:

- [ ] **Visual Studio Code** (latest version)
  - Check: Help → About (should show recent version number)
  - If outdated: Download from [code.visualstudio.com](https://code.visualstudio.com)

- [ ] **GitHub Copilot Chat Extension**
  - Open VS Code Extensions (Ctrl+Shift+X)
  - Search "GitHub Copilot Chat"
  - Should be installed and enabled
  - If missing: Click Install

- [ ] **Node.js** (LTS version)
  - Open Terminal: Ctrl+` (backtick)
  - Type: `node --version`
  - Should show version ≥ 18.x
  - If not installed: Download from [nodejs.org](https://nodejs.org)

- [ ] **Active Zerodha Account**
  - Kite login working at [kite.zerodha.com](https://kite.zerodha.com)
  - Portfolio with at least one holding (for testing)

- [ ] **Internet Connection**
  - Test: Visit any website
  - Must be stable for OAuth authorization

---

## Step-by-Step MCP Setup

### Step 1: Open VS Code Settings (1 minute)

1. **Open VS Code** (if not already open)

2. **Open Settings**
   - **Windows/Linux**: Press `Ctrl+,` (Ctrl and comma together)
   - **Mac**: Press `Cmd+,` (Cmd and comma together)
   
   Alternative: File → Preferences → Settings

3. **Search for "mcp"** in the settings search box (top left of Settings panel)

4. The search should show various MCP-related settings

### Step 2: Open settings.json File (1 minute)

In the Settings panel:

1. Look for "GitHub Copilot Chat" section or "MCP" setting
2. Click on the link that says **"Edit in settings.json"** 
   - This link usually appears next to MCP configuration areas

   Alternative method:
   - Press `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac)
   - Search for "Preferences: Open Settings (JSON)"
   - Press Enter

3. The `settings.json` file will open in the editor

### Step 3: Find or Create MCP Configuration (2 minutes)

In the `settings.json` file:

**Look for existing "mcp" section:**

```json
{
  "mcp": {
    "servers": {
      ...
    }
  }
}
```

If it exists, find the `"servers"` part and add Kite there.

**If "mcp" section doesn't exist:**

Add it at the root level of the JSON. Find a good spot between other settings.

### Step 4: Add Kite MCP Configuration (1 minute)

**Add this configuration inside the "servers" section:**

```json
"kite": {
  "url": "https://mcp.kite.trade/mcp"
}
```

### Step 5: Complete JSON Structure

Your final `settings.json` should look like one of these:

**Minimal (just MCP):**
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

**With other settings:**
```json
{
  // ... other settings you might have ...
  "editor.fontSize": 14,
  "editor.theme": "Dark",
  
  "mcp": {
    "servers": {
      "kite": {
        "url": "https://mcp.kite.trade/mcp"
      }
    }
  }
  
  // ... more settings ...
}
```

**With multiple MCP servers (if you have others):**
```json
{
  "mcp": {
    "servers": {
      "kite": {
        "url": "https://mcp.kite.trade/mcp"
      },
      "other-mcp": {
        "url": "https://other-mcp.example.com/mcp"
      }
    }
  }
}
```

### Step 6: Validate JSON Syntax (1 minute)

Check that your JSON is valid:

1. **Look for red squiggly lines** in settings.json
   - Red lines = JSON syntax error
   - Fix: Usually missing comma or bracket

2. **Common mistakes to avoid:**
   - Missing comma between properties
   - Extra commas at end of last property
   - Mismatched curly braces `{}` or brackets `[]`
   - Missing quotes around strings

3. **Test**: VS Code should not show any errors at the bottom of editor

### Step 7: Save Settings File (1 minute)

1. **Press `Ctrl+S`** (or `Cmd+S` on Mac) to save

2. **Verify save:**
   - The white dot next to filename should disappear
   - Status bar should show "Saved" message

3. **If save fails:**
   - Check you have permission to edit file
   - Make sure file is not corrupted
   - Close file and reopen

### Step 8: Restart VS Code (2 minutes)

1. **Close VS Code completely**
   - File → Exit (Windows/Linux)
   - Or close all windows (Mac)

2. **Wait 5 seconds**

3. **Reopen VS Code**

4. **Wait 30 seconds** for MCP server to initialize

   (You might see a notification: "Initializing MCP servers...")

### Step 9: Verify MCP Connection (2 minutes)

1. **Open Copilot Chat Panel**
   - Press `Ctrl+Shift+I` (or `Cmd+Shift+I` on Mac)
   - Or: Click Copilot icon in left sidebar

2. **Type this command:**
   ```
   /mcp list
   ```

3. **Look for output:**
   - Should show `kite` as one of the available MCP servers
   - If shown, MCP is successfully installed ✅

4. **If not shown:**
   - Check settings.json JSON syntax
   - Verify URL is exactly: `https://mcp.kite.trade/mcp`
   - Try restarting VS Code again

### Step 10: Authorize Your Kite Account (3 minutes)

1. **Ask agent for portfolio analysis:**
   ```
   @kite-zeroda-portfolio-analyser
   Get my portfolio analysis
   ```

2. **You'll see a message:**
   ```
   "Connecting to Kite MCP... Authorization required"
   ```

3. **Click the "Authorize" button** that appears

4. **You'll be taken to Kite login page:**
   - Email: Your Zerodha email
   - Password: Your Zerodha password
   - 2FA: Enter OTP if enabled

5. **Grant Permissions:**
   - A consent screen will ask to grant "Portfolio Access"
   - Review permissions (should only be portfolio data)
   - Click "Allow" or "Authorize"

6. **Automatic Redirect:**
   - You'll be redirected back to VS Code
   - Authorization is complete!

7. **First Analysis:**
   - Agent will now fetch your portfolio
   - Shows live positions, prices, and analysis

### Setup Complete! ✅

You've successfully connected Kite MCP. You can now:

```
@kite-zeroda-portfolio-analyser
Get my portfolio analysis
```

---

## Verification Checklist

After setup, verify everything works:

- [ ] `/mcp list` shows `kite` server
- [ ] Authorization succeeded without errors
- [ ] First portfolio analysis returned live data
- [ ] Stock prices shown match current Kite prices
- [ ] Quantities and holdings match Kite account

If any item is not working, refer to Troubleshooting section below.

---

## Troubleshooting

### Problem: "Kite MCP not found" in `/mcp list`

**Possible Causes:**
1. Settings not saved
2. VS Code not restarted after saving
3. JSON syntax error in settings.json
4. Incorrect URL in configuration

**Solutions:**
1. Verify settings.json is saved (Ctrl+S shows no white dot)
2. Completely close VS Code (including all windows)
3. Reopen VS Code and wait 30 seconds
4. Check for red squiggly lines in settings.json
5. Compare your URL with: `https://mcp.kite.trade/mcp` (exactly)
6. Try refreshing MCP: Type `/mcp refresh`

### Problem: Authorization Button Doesn't Appear

**Possible Causes:**
1. MCP server not properly initialized
2. Network connectivity issue
3. VS Code cache issue

**Solutions:**
1. Restart VS Code completely
2. Check internet connection
3. Clear VS Code cache: 
   - Quit VS Code
   - Go to `~/.config/Code/CachedData/` and delete oldest folders
   - Reopen VS Code
4. Try authorization request again

### Problem: Authorization Fails (Login Error)

**Possible Causes:**
1. Wrong Zerodha credentials
2. Browser cookies issue
3. Account security block

**Solutions:**
1. Verify your Zerodha login at [kite.zerodha.com](https://kite.zerodha.com) works
2. Clear browser cookies:
   - Open private/incognito window
   - Try authorization again
3. Check if account has login restrictions (2FA, IP blocks)
4. Contact Zerodha support if issue persists

### Problem: "Permission Denied" After Authorization

**Possible Causes:**
1. Permissions not fully granted on consent screen
2. Account doesn't have portfolio access
3. DEMAT account not activated

**Solutions:**
1. Revoke and re-authorize:
   ```
   /mcp refresh
   ```
   Then ask for portfolio analysis again
2. Ensure consent screen shows full permissions checked
3. Verify DEMAT account is active on Kite website
4. Try authorizing after a few minutes (sometimes delayed)

### Problem: MCP Stops Working After Working Initially

**Possible Causes:**
1. Token expired
2. Copilot extension crashed
3. Network connection lost
4. Zerodha API maintenance

**Solutions:**
1. **Restart extension:**
   - Press Ctrl+Shift+P (Cmd+Shift+P on Mac)
   - Search "Reload Window"
   - Press Enter

2. **Re-authorize:**
   - Ask for analysis: `@kite-zeroda-portfolio-analyser Get my portfolio`
   - Re-authorize if prompted

3. **Check status:**
   - Type `/mcp status` to see server health
   - Check for degraded services message

4. **Wait if maintenance:**
   - Kite sometimes does maintenance
   - Try again in a few minutes

### Problem: Data Doesn't Match Kite

**Possible Causes:**
1. Portfolio updated recently
2. MCP cache not refreshed
3. Time zone difference

**Solutions:**
1. Refresh MCP: `/mcp refresh`
2. Ask agent: "Refresh and get latest portfolio data"
3. Allow 5 minutes for sync if you just made trades
4. Verify you're looking at same time period

### Problem: MCP Works But Agent Says "Need Manual Data"

**Possible Causes:**
1. Agent doesn't recognize MCP is connected
2. MCP permissions incomplete

**Solutions:**
1. Type: `/mcp list` to verify kite is shown
2. Ask: `@kite-zeroda-portfolio-analyser Connect to my Kite account`
3. If still manual: Provide data as CSV or Excel

---

## Security Best Practices

### ✅ DO:

- ✅ Use strong, unique Zerodha password
- ✅ Enable 2FA on Zerodha account
- ✅ Revoke MCP access when not using
- ✅ Log out after using MCP on shared computers
- ✅ Keep VS Code updated
- ✅ Review MCP permissions regularly

### ❌ DON'T:

- ❌ Share your authorization token with anyone
- ❌ Leave MCP authorized on public computers
- ❌ Use MCP on unsecured/public WiFi networks
- ❌ Share screenshots showing sensitive data
- ❌ Give your Zerodha password to anyone
- ❌ Leave VS Code unattended while authorized

### Revoking MCP Access (Anytime)

If you want to disconnect Kite MCP:

1. **Method 1: Via Kite Dashboard**
   - Login to [kite.zerodha.com](https://kite.zerodha.com)
   - Settings → Connected Applications / OAuth
   - Find "Kite MCP" or "Copilot MCP"
   - Click "Revoke" or "Disconnect"
   - Immediate effect

2. **Method 2: Via VS Code**
   - Remove or comment out Kite from settings.json
   - Restart VS Code
   - Authorization revoked

3. **If Compromised:**
   - Immediately revoke via Kite Dashboard
   - Change Zerodha password
   - Contact Zerodha support

---

## Advanced Configuration

### Using Multiple MCP Servers

If you have other MCP servers (not just Kite):

```json
{
  "mcp": {
    "servers": {
      "kite": {
        "url": "https://mcp.kite.trade/mcp"
      },
      "other-server": {
        "url": "https://other-mcp.example.com/mcp"
      },
      "another-service": {
        "url": "https://another.example.com/mcp"
      }
    }
  }
}
```

All servers will initialize on VS Code startup.

### Kite MCP with Custom Proxy (Advanced)

If behind corporate proxy:

```json
{
  "mcp": {
    "servers": {
      "kite": {
        "url": "https://mcp.kite.trade/mcp",
        "proxy": "http://proxy.company.com:8080"
      }
    }
  }
}
```

### Debugging MCP Issues (Advanced)

Enable debug logging:

1. Press Ctrl+Shift+P
2. Search "Developer: Toggle Developer Tools"
3. Look in Console tab for MCP debug messages
4. Share error messages with Kite support if needed

---

## Getting Help

### If Setup Still Doesn't Work:

1. **Check Kite Status**: [status.kite.trade](https://status.kite.trade)
   - Verify Kite services are operational

2. **Review Error Messages**: Copy exact error from console
   - Press Ctrl+Shift+P → "Developer: Toggle Developer Tools"
   - Check Console tab for detailed errors

3. **Contact Support**:
   - **Kite MCP Issues**: Zerodha support
   - **VS Code Issues**: GitHub Copilot support
   - **Agent Issues**: Error messages in chat

4. **Fallback Option**: Use manual data entry
   - MCP optional, agent works with manual imports
   - Share portfolio as CSV or manual input

---

## Reference

### Useful Commands

```
/mcp list         → Show all MCP servers
/mcp status       → Detailed server status
/mcp refresh      → Force reconnection
```

### Kite MCP URL

```
https://mcp.kite.trade/mcp
```

Always use this exact URL.

### Kite Account Login

```
https://kite.zerodha.com
```

### Support Contacts

- **Kite Support**: support@zerodha.com
- **Zerodha Help**: [support.zerodha.com](https://support.zerodha.com)

---

## Success Indicators

You'll know MCP is working when:

✅ Portfolio analysis runs instantly (no manual data needed)  
✅ Current prices match live Kite prices  
✅ Holdings quantities match exactly  
✅ No "data not found" errors  
✅ Agent can analyze without asking for stock info  

---

**MCP Setup Complete! You're ready to use live, real-time portfolio analysis.**

*Last Updated: March 14, 2026*
