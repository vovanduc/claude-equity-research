# Paper Trading Portfolio Guide

Complete guide to using the Claude Equity Research paper trading system for learning and practicing investment strategies.

## What is Paper Trading?

**Paper trading** is simulated stock trading using virtual money. You practice buying and selling stocks without risking real capital.

**Benefits:**
- Learn investing mechanics risk-free
- Test strategies before committing real money
- Build confidence and experience
- Make mistakes that teach without costing money
- Track performance and refine approach

**Important:** Paper trading success doesn't guarantee real trading success. Real money involves emotional challenges, taxes, and fees not present in simulation.

## Getting Started

### Initial Setup

Your paper trading portfolio starts with **$100,000 in virtual cash**.

No configuration needed - just start trading!

### First Steps

1. **Learn the basics** (recommended for beginners)
   ```
   /learn basics
   ```

2. **Research a stock**
   ```
   /trading-ideas AAPL
   ```

3. **Make your first trade**
   ```
   /paper-buy AAPL 10
   ```

4. **Check your portfolio**
   ```
   /portfolio
   ```

## Commands Overview

### `/portfolio` - View Portfolio

Display your current positions, profit/loss, and performance metrics.

**Usage:**
```
/portfolio              # Summary view
/portfolio --summary    # Same as above
/portfolio --detailed   # Detailed view with transaction history
```

**What You'll See:**
- Total portfolio value
- Cash balance
- Current positions with P&L
- Best/worst performers
- Allocation percentages

**Example Output:**
```
📊 PAPER TRADING PORTFOLIO

Portfolio Value: $105,450 | Cash: $45,000 | P&L: +$5,450 (5.45%)

CURRENT POSITIONS (3 holdings)

Ticker | Shares | Avg Cost | Current | Market Value | P&L    | P&L % | Allocation
-------|--------|----------|---------|--------------|--------|-------|------------
AAPL   | 100    | $225.00  | $235.00 | $23,500      | +$1,000| +4.4% | 22.3%
MSFT   | 50     | $380.00  | $395.00 | $19,750      | +$750  | +3.9% | 18.7%
GOOGL  | 100    | $140.00  | $157.00 | $15,700      | +$1,700| +12.1%| 14.9%
```

### `/paper-buy` - Buy Stocks

Execute simulated stock purchases.

**Usage:**
```
/paper-buy <TICKER> <SHARES> [PRICE]
```

**Examples:**
```
/paper-buy AAPL 25              # Buy 25 shares at current market price
/paper-buy MSFT 10 380.50       # Buy 10 shares at $380.50
/paper-buy GOOGL 5              # Buy 5 shares at current price
```

**Parameters:**
- **TICKER** (required): Stock symbol (e.g., AAPL, MSFT, TSLA)
- **SHARES** (required): Number of shares to buy
- **PRICE** (optional): Specific price per share (uses current price if omitted)

**What Happens:**
1. System fetches current stock price
2. Calculates total cost (shares × price)
3. Checks if you have sufficient cash
4. Deducts cash from your balance
5. Adds position to your portfolio
6. Records transaction in history

**Important Notes:**
- Commission-free (no trading fees in paper trading)
- If you already own the stock, adds to existing position and recalculates average cost
- System warns if position becomes too large (>15% of portfolio)

### `/paper-sell` - Sell Stocks

Execute simulated stock sales.

**Usage:**
```
/paper-sell <TICKER> <SHARES> [PRICE]
/paper-sell <TICKER> ALL        # Sell entire position
```

**Examples:**
```
/paper-sell AAPL 25            # Sell 25 shares at current price
/paper-sell MSFT ALL           # Sell all MSFT shares
/paper-sell GOOGL 5 175.50     # Sell 5 shares at $175.50
```

**Parameters:**
- **TICKER** (required): Stock symbol you own
- **SHARES** (required): Number of shares to sell, or "ALL"
- **PRICE** (optional): Specific price per share

**What Happens:**
1. Verifies you own the stock
2. Fetches current price
3. Calculates proceeds and realized P&L
4. Adds cash to your balance
5. Updates or removes position
6. Records transaction with profit/loss

**Realized P&L Calculation:**
```
Realized P&L = (Sell Price - Average Cost) × Shares Sold

Example:
Bought 100 shares @ $200 = $20,000 total cost
Selling 50 shares @ $230
Realized P&L = ($230 - $200) × 50 = +$1,500 (+15%)
```

**Note:** Your average cost doesn't change when you sell (only when you buy more).

## Portfolio Data Storage

Your portfolio is stored in JSON files in your home directory:

```
~/.claude/equity-research/
├── portfolio.json       # Current positions and cash balance
├── transactions.json    # Complete trade history
└── performance.json     # Performance metrics (future feature)
```

### Portfolio.json Structure

```json
{
  "cash": 75000.00,
  "initial_cash": 100000.00,
  "positions": [
    {
      "ticker": "AAPL",
      "company_name": "Apple Inc.",
      "shares": 100,
      "average_cost": 225.00,
      "purchase_date": "2025-01-15",
      "total_cost": 22500.00,
      "last_updated": "2025-01-15"
    }
  ],
  "created": "2025-01-10",
  "last_updated": "2025-01-15"
}
```

### Transactions.json Structure

```json
{
  "transactions": [
    {
      "type": "BUY",
      "ticker": "AAPL",
      "company_name": "Apple Inc.",
      "shares": 100,
      "price": 225.00,
      "total_amount": 22500.00,
      "cash_after": 77500.00,
      "date": "2025-01-15T14:30:00Z",
      "notes": ""
    },
    {
      "type": "SELL",
      "ticker": "AAPL",
      "shares": 50,
      "price": 235.00,
      "total_amount": 11750.00,
      "cost_basis": 225.00,
      "realized_pl": 500.00,
      "realized_pl_percent": 4.44,
      "cash_after": 89250.00,
      "date": "2025-01-20T10:15:00Z",
      "notes": "Partial profit take"
    }
  ]
}
```

## Best Practices

### 1. Research Before Trading

Always analyze stocks before buying:

```
/trading-ideas [TICKER]
```

Look for:
- BUY/SELL/HOLD recommendation
- Price targets (bull/base/bear scenarios)
- Key catalysts and risks
- Valuation metrics vs peers

### 2. Position Sizing

Follow professional risk management:

**Guidelines:**
- Start with 3-5% per position for beginners
- High conviction: 5-8% of portfolio
- Medium conviction: 3-5%
- Speculative: 1-2%
- Keep 10-20% cash for opportunities

**Example $100,000 Portfolio:**
```
High Conviction (3 stocks): $20,000 each = $60,000
Medium Conviction (4 stocks): $5,000 each = $20,000
Cash Reserve: $20,000
```

### 3. Use Stop-Losses

Protect against large losses:

**Mental Stop-Loss Process:**
1. When you buy, decide your stop-loss level (e.g., 8% below entry)
2. Track it mentally or in a note
3. If price hits stop, execute: `/paper-sell [TICKER] [SHARES]`
4. This builds discipline for real trading

**Example:**
```
Buy AAPL at $230
Set mental stop at $212 (8% below)
If AAPL drops to $212: /paper-sell AAPL ALL
```

### 4. Take Profits Strategically

Don't be greedy - take profits when targets hit:

**Strategies:**
- **Full exit:** Sell entire position at target
- **Partial exit:** Sell 50% at target, let rest run
- **Trailing stop:** Raise stop-loss as price rises

**Example:**
```
/trading-ideas MSFT shows $420 target
Buy at $380, current price reaches $420
Option 1: /paper-sell MSFT ALL (lock in +10.5%)
Option 2: /paper-sell MSFT 50 (take 50% profits, let 50% run)
```

### 5. Diversify

Don't put all eggs in one basket:

**Diversification Guidelines:**
- **10-15 stocks** (sweet spot for most investors)
- **Multiple sectors** (tech, healthcare, finance, consumer, energy)
- **Different market caps** (70% large-cap, 20% mid-cap, 10% small-cap)

**Check Your Diversification:**
```
/portfolio --detailed
```

Look for:
- No single position >15%
- No single sector >30-40%
- Mix of growth and value stocks

### 6. Learn from Mistakes

Every losing trade is a lesson:

**After a Loss, Ask:**
- Did I research properly?
- Was position size appropriate?
- Did I use a stop-loss?
- What would I do differently?

Paper trading is the perfect place to make mistakes and learn!

## Common Scenarios

### Scenario 1: Starting Your First Position

```bash
# Step 1: Learn basics
/learn basics

# Step 2: Research
/trading-ideas AAPL

# Step 3: Analyze output
# - BUY recommendation?
# - Price target shows upside?
# - Risks manageable?

# Step 4: Calculate position size
# Portfolio: $100,000
# Allocate 5% = $5,000
# AAPL at $225 = $5,000 / $225 ≈ 22 shares

# Step 5: Execute
/paper-buy AAPL 22

# Step 6: Set mental stop-loss
# Entry $225, stop at $207 (8% below)

# Step 7: Track
/portfolio
```

### Scenario 2: Adding to Winner

```bash
# You own 20 MSFT @ $380 (up 10%)

# Step 1: Re-analyze
/trading-ideas MSFT

# Step 2: If thesis still valid, add more
/paper-buy MSFT 10

# Note: This increases average cost and position size
# New average: (20×$380 + 10×$418) / 30 = $392
```

### Scenario 3: Cutting a Loser

```bash
# You own 50 TSLA @ $250 (now $225, down 10%)
# Hit your 10% stop-loss

# Step 1: Honor the stop
/paper-sell TSLA ALL

# Step 2: Review what went wrong
# Re-read /trading-ideas TSLA analysis
# What did you miss? Overvalued? Weak technicals?

# Step 3: Learn and move on
# Use freed capital for better opportunity
```

### Scenario 4: Taking Partial Profits

```bash
# You own 100 GOOGL @ $140 (now $170, up 21%)
# Target was $165, exceeded expectations

# Option: Take 50% profits, let 50% run
/paper-sell GOOGL 50

# Realized: 50 × ($170 - $140) = +$1,500
# Remaining: 50 shares (house money)
# Raise stop on remaining 50 shares to $160
```

## Performance Tracking

### Key Metrics to Monitor

Check `/portfolio` regularly to track:

**1. Total Return**
```
Total P&L: $5,450 (+5.45%)
```
Are you beating the market? (S&P 500 benchmark)

**2. Win Rate**
```
Winning Positions: 7 out of 10 (70% win rate)
```
Professional traders often have 50-60% win rates but make money through risk management.

**3. Best/Worst Performers**
```
Best: NVDA +35%
Worst: PLTR -18%
```
Understand why winners won and losers lost.

**4. Position Allocation**
```
Tech: 40%
Healthcare: 20%
Finance: 15%
...
```
Is one sector too concentrated?

## Tips for Success

### ✅ Do's

1. **Research thoroughly** - Use `/trading-ideas` before every trade
2. **Start small** - Begin with 3-5 positions
3. **Size appropriately** - Follow 3-7% position sizing
4. **Use stop-losses** - Limit losses to 7-12%
5. **Take profits** - Don't be greedy at targets
6. **Diversify** - Multiple stocks and sectors
7. **Learn continuously** - Use `/learn` modules
8. **Review performance** - Check `/portfolio` regularly
9. **Document reasoning** - Note why you buy/sell
10. **Practice discipline** - Follow your rules

### ❌ Don'ts

1. **Don't trade blindly** - No gambling on random stocks
2. **Don't overtrade** - Quality over quantity
3. **Don't ignore stops** - Respect your risk management
4. **Don't revenge trade** - After losses, take a break
5. **Don't concentrate risk** - No position >15%
6. **Don't chase** - Don't buy after huge run-ups
7. **Don't panic sell** - Unless stop-loss hit
8. **Don't average down blindly** - Only if thesis intact
9. **Don't neglect sectors** - Diversify beyond tech
10. **Don't skip learning** - Complete `/learn` modules

## Integration with Analysis

### Using `/trading-ideas` to Guide Trades

The `/trading-ideas` command provides all information needed for paper trading decisions:

**1. Executive Summary** → BUY/SELL/HOLD guidance
```
BUY with $260 target (13% upside)
```

**2. Price Targets** → Set your profit targets
```
Bull: $280, Base: $260, Bear: $220
```

**3. Risk Assessment** → Position sizing guidance
```
Suggested position: 3-5% of portfolio
```

**4. Technical Context** → Entry timing
```
Support at $225, resistance at $240
RSI 45 (neutral)
```

**5. Catalyst Analysis** → Hold duration expectations
```
Earnings in 3 weeks, product launch Q2
```

### Example Integrated Workflow

```bash
# 1. Research
/trading-ideas NVDA

# Output shows:
# - BUY recommendation
# - Target $950 (current $880, +8% upside)
# - Support at $850
# - Suggest 4% position

# 2. Calculate Trade
# Portfolio: $100,000
# 4% position = $4,000
# Shares: $4,000 / $880 = 4.5 → Round to 4 shares

# 3. Execute
/paper-buy NVDA 4

# 4. Set stops and targets
# Stop: $850 (below support, -3.4%)
# Target: $950 (+8%)

# 5. Monitor
/portfolio

# 6. Exit when conditions met
# If hits $950: /paper-sell NVDA ALL
# If hits $850: /paper-sell NVDA ALL (stop hit)
```

## Troubleshooting

### Common Issues

**Issue: "Insufficient funds"**
- Check cash balance: `/portfolio`
- Reduce share count or sell other positions
- Remember: Can't spend more than available cash

**Issue: "Position not found"**
- Verify ticker spelling
- Check holdings: `/portfolio`
- You can only sell stocks you own

**Issue: "Price unavailable"**
- Market may be closed
- Specify price manually: `/paper-sell AAPL 10 230.50`
- Or wait for market hours

## Next Steps

1. **Complete Learning Modules**
   - `/learn basics` - Start here!
   - `/learn fundamentals` - Analyze companies
   - `/learn technical` - Time entries/exits
   - `/learn valuation` - Determine fair value
   - `/learn risk` - CRITICAL for success

2. **Practice the Full Cycle**
   - Research → Buy → Hold → Sell
   - Track performance for 1-3 months
   - Review what worked and what didn't

3. **Build Your Strategy**
   - Develop personal criteria for buying
   - Define risk management rules
   - Create exit strategies

4. **Graduate to Real Trading** (when ready)
   - Start with small amounts
   - Expect emotional challenges
   - Remember: Paper success ≠ guaranteed real success

---

💡 **Remember:** Paper trading is a learning tool. Take it seriously to build good habits that will serve you when trading real money!

⚠️ **Disclaimer:** This is simulated trading for educational purposes only. No real money is involved. Always consult qualified financial professionals before investing real capital.
