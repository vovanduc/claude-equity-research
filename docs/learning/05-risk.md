# MODULE 5: RISK MANAGEMENT

## Overview

⚠️ **MOST IMPORTANT MODULE** ⚠️

Risk management is what separates successful investors from those who lose money. You can be right about stock picks 60% of the time and still lose money with poor risk management. Learn to protect your capital first, grow it second.

**Duration:** ~20 minutes
**Prerequisites:** Module 1 (Basics)
**Level:** Intermediate - CRITICAL FOR ALL TRADERS

## Why Risk Management Matters

### The Math of Losses

**Critical Concept:** Losses hurt more than gains help.

**Example:**
- Start with $10,000
- Lose 50% → Down to $5,000
- Need **100% gain** to get back to $10,000 (not just 50%!)

**The Math:**
- Loss: $10,000 × 0.50 = $5,000 remaining
- Recovery needed: $5,000 × 2.00 = $10,000 (100% gain)

**Key Lesson:** **Avoiding big losses is more important than finding big winners.**

### How Professionals Think About Risk

**Amateur mindset:** "How much can I make?"
**Professional mindset:** "How much can I lose, and can I survive it?"

Warren Buffett's Rules:
1. **Rule #1:** Don't lose money
2. **Rule #2:** Don't forget Rule #1

## Position Sizing

### What is Position Sizing?

**Position sizing:** Deciding how much money to allocate to each stock.

**Core Principle:** Never risk so much on one trade that a loss significantly damages your portfolio.

### The 2% Rule

**Rule:** Never risk more than 2% of your portfolio on a single trade.

**Example:**
```
Portfolio Value: $100,000
Maximum Risk per Trade: $100,000 × 0.02 = $2,000

Stock Entry: $50
Stop-Loss: $45 (10% below entry)
Risk per Share: $5

Maximum Shares: $2,000 / $5 = 400 shares
Total Position Size: 400 × $50 = $20,000 (20% of portfolio)
```

**Key:** The 2% refers to how much you can *lose* (entry to stop-loss), not how much you *invest*.

### Conservative Position Sizing Guidelines

**By Experience Level:**
- **Beginners:** 2-5% per position, max 10 positions (20-50% deployed)
- **Intermediate:** 3-7% per position, 10-15 positions (30-105% deployed with manageable risk)
- **Advanced:** 5-10% per position, 15-20 positions

**By Conviction Level:**
- **High Conviction:** 5-8% of portfolio (strong fundamental thesis, favorable risk-reward)
- **Medium Conviction:** 3-5% of portfolio (good setup, moderate confidence)
- **Low Conviction / Speculative:** 1-2% of portfolio (higher risk, experimental)

**Example Portfolio:**
```
$100,000 Portfolio:
High Conviction Stocks (3): $20,000 each = $60,000 (60%)
Medium Conviction (4): $5,000 each = $20,000 (20%)
Speculative (2): $2,000 each = $4,000 (4%)
Cash: $16,000 (16%)
```

### Position Size Warnings in Paper Trading

When you use `/paper-buy`, the system warns you if:
- **Single position >15%:** Concentration risk
- **Cash <10%:** Low liquidity buffer
- **>25 positions:** Over-diversification (hard to manage)

## Stop-Losses

### What is a Stop-Loss?

**Stop-loss:** A price level at which you automatically exit to limit losses.

**Purpose:** Prevents small losses from becoming catastrophic losses.

### Setting Stop-Losses

**Common Approaches:**

#### 1. Percentage-Based Stop-Loss

**Formula:** Stop-Loss = Entry Price × (1 - Stop %)

**Example:**
- Buy at $100
- 7% stop-loss
- Stop-Loss Price: $100 × 0.93 = $93

**Typical Stops:**
- **Aggressive:** 5-7% (tight, frequent stops)
- **Moderate:** 8-12% (balanced)
- **Conservative:** 15-20% (wide, for volatile stocks)

#### 2. Technical Stop-Loss

Place stop below key support levels.

**Example:**
- Buy stock at $105
- Support level at $98
- Place stop at $97 (just below support to avoid fakeouts)

**Why?** If support breaks, trend may have changed. Better to exit and reassess.

#### 3. ATR-Based Stop-Loss

**ATR (Average True Range):** Measures stock's typical volatility.

**Formula:** Stop-Loss = Entry - (2 × ATR)

**Example:**
- Buy at $100
- ATR = $3 (stock typically moves $3/day)
- Stop-Loss: $100 - (2 × $3) = $94

**Why?** Volatile stocks need wider stops; stable stocks can use tighter stops.

### Trailing Stop-Loss

**Concept:** Stop-loss that moves up as price rises, locking in profits.

**Example:**
```
Buy at $100, set 10% trailing stop
Price → $100: Stop at $90
Price → $120: Stop at $108 (120 × 0.90)
Price → $140: Stop at $126 (140 × 0.90)
Price falls to $126: STOPPED OUT with +26% gain!
```

**Benefit:** Lets winners run while protecting profits.

### Common Stop-Loss Mistakes

❌ **No stop-loss at all:** "I'll just wait for it to come back" (famous last words)
❌ **Moving stop-loss down:** Defeats the purpose of risk management
❌ **Stop too tight:** Gets triggered by normal volatility
❌ **Stop too wide:** Allows excessive losses
❌ **Ignoring the stop:** Setting one but not following through

## Risk-Reward Ratio

### What is Risk-Reward?

**Risk-Reward Ratio:** How much you can potentially gain vs how much you risk losing.

**Formula:** Risk-Reward = (Target Price - Entry Price) / (Entry Price - Stop-Loss Price)

### Calculating Risk-Reward

**Example 1: Good Risk-Reward**
```
Entry: $100
Target: $130 (30% upside)
Stop-Loss: $92 (8% downside)

Risk-Reward = ($130 - $100) / ($100 - $92)
            = $30 / $8
            = 3.75:1

For every $1 risked, you can make $3.75 → GOOD TRADE SETUP
```

**Example 2: Poor Risk-Reward**
```
Entry: $100
Target: $110 (10% upside)
Stop-Loss: $85 (15% downside)

Risk-Reward = ($110 - $100) / ($100 - $85)
            = $10 / $15
            = 0.67:1

Risk $1 to make $0.67 → BAD TRADE SETUP (skip this trade!)
```

### Minimum Risk-Reward Rules

**Professional Standards:**
- **Minimum acceptable:** 2:1 risk-reward
- **Good trade:** 3:1 or better
- **Excellent trade:** 5:1 or better

**Why?** Even with 50% win rate, 2:1 risk-reward makes you profitable:
```
10 trades, 50% win rate, 2:1 risk-reward:
Wins: 5 × $200 = +$1,000
Losses: 5 × $100 = -$500
Net: +$500 profit
```

With 1:1 risk-reward, you need >50% win rate just to break even.

### Applying Risk-Reward in `/trading-ideas`

When you run `/trading-ideas`, the analysis includes:

**Example:**
```
VALUATION & PRICE TARGETS:
Bull case $260, Base case $225, Bear case $190.
Current price: $220

Potential Upside to Base Case: +2.3%
Potential Upside to Bull Case: +18%
Potential Downside to Bear Case: -13.6%

Risk-Reward Assessment: With appropriate stop-loss at $200 (-9%), potential
upside of +18% to bull case offers 2:1 risk-reward ratio.
```

Use this information to decide if the trade has favorable risk-reward!

## Diversification

### Why Diversify?

**Don't put all eggs in one basket.** If one stock crashes, your portfolio doesn't crash.

**Key Principle:** Losses on some positions offset by gains on others.

### Diversification Guidelines

#### By Number of Holdings

- **Too Concentrated (<5 stocks):** One bad pick can devastate portfolio
- **Well-Diversified (10-20 stocks):** Balanced risk and manageability
- **Over-Diversified (>30 stocks):** Hard to track, dilutes returns from best ideas

**Sweet Spot:** 10-15 stocks for most individual investors

#### By Sector

Don't load up on one industry. If tech crashes, a tech-heavy portfolio crashes.

**Example Good Diversification:**
```
Portfolio Allocation by Sector:
Technology: 25%
Healthcare: 20%
Financial: 15%
Consumer: 15%
Industrial: 10%
Energy: 10%
Cash: 5%
```

**Example Bad Diversification (Sector Concentration):**
```
Portfolio:
AAPL, MSFT, GOOGL, NVDA, AMD, TSLA = 90% Tech
→ If tech sector crashes, entire portfolio crashes!
```

#### By Market Cap

Mix large-cap (stable), mid-cap (growth), small-cap (high risk/reward).

**Example:**
- Large-cap (>$10B): 60-70% (core holdings)
- Mid-cap ($2-10B): 20-30% (growth opportunities)
- Small-cap (<$2B): 0-10% (speculative)

### Correlation

**Correlation:** How stocks move together.
- **+1.0:** Perfect correlation (move together)
- **0.0:** No correlation (independent)
- **-1.0:** Perfect inverse (one up, other down)

**Goal:** Hold stocks with low correlation to reduce portfolio volatility.

**Example:**
- Tech stocks and energy stocks often have low correlation
- Buying AAPL and MSFT = high correlation (both tech, similar drivers)
- Better: Mix AAPL (tech) + XOM (energy) + JNJ (healthcare)

## Portfolio Heat

**Portfolio Heat:** Total capital at risk across all open positions.

**Formula:** Portfolio Heat = Sum of (Position Size × Stop-Loss %)

**Example:**
```
Position 1: $10,000 position, 8% stop = $800 risk
Position 2: $15,000 position, 10% stop = $1,500 risk
Position 3: $20,000 position, 7% stop = $1,400 risk

Total Portfolio Heat: $800 + $1,500 + $1,400 = $3,700

Portfolio Value: $100,000
Heat %: $3,700 / $100,000 = 3.7%
```

**Guidelines:**
- **Total heat <6%:** Conservative (if all stops hit, lose only 6%)
- **Total heat 6-10%:** Moderate risk
- **Total heat >10%:** Aggressive / dangerous

**Why It Matters:** If market crashes and all positions hit stops, you want to survive to trade another day.

## Practical Application

### Risk Management with Paper Trading

**When using `/paper-buy`:**

1. **Calculate position size** based on portfolio % and stop-loss
2. **Set a mental stop-loss** (e.g., "I'll sell if it drops below $X")
3. **Track in a note** your stop level and risk-reward
4. **Honor the stop** if price hits it (practice discipline!)

**Example:**
```
/trading-ideas AAPL → BUY rating, target $260, support at $210
Current price: $230
Portfolio: $100,000

Plan:
Entry: $230
Stop-Loss: $210 (8.7% risk)
Target: $260 (13% gain)
Risk-Reward: 1.5:1 (acceptable)

Max Risk: $100,000 × 0.02 = $2,000
Risk per Share: $230 - $210 = $20
Max Shares: $2,000 / $20 = 100 shares
Position Size: 100 × $230 = $23,000 (23% of portfolio)

Execute: /paper-buy AAPL 100

If price hits $210: /paper-sell AAPL 100 (honor the stop!)
If price hits $260: /paper-sell AAPL 50 (take partial profits)
```

### Practice Exercise

**Task:** Create a risk-managed position

1. Run `/trading-ideas [TICKER]`
2. Note the support level from technical analysis
3. Calculate:
   - Entry price (current price)
   - Stop-loss (below support)
   - Target (from price targets in report)
   - Risk-reward ratio
4. Determine position size using 2% rule
5. Execute `/paper-buy [TICKER] [SHARES]`
6. Set a reminder to check if stop is hit
7. Practice exiting at stop-loss if triggered (builds discipline!)

## Common Risk Management Mistakes

### ❌ Mistake 1: "I'll Just Hold Through the Dip"

**Problem:** Small losses become large losses. Many stocks never recover.

**Solution:** Set stops and honor them. You can always re-enter if thesis changes.

### ❌ Mistake 2: Revenge Trading

**Problem:** After a loss, immediately making risky trade to "make it back."

**Solution:** Take a break after losses. Analyze what went wrong. Trade with clear head.

### ❌ Mistake 3: Averaging Down on Losers

**Problem:** "It's down 20%, I'll buy more to lower my average!" (Often compounds losses)

**Solution:** Only average down if thesis is intact and new analysis supports it.

### ❌ Mistake 4: Cutting Winners, Letting Losers Run

**Problem:** Selling profitable stocks quickly while holding losing positions "hoping they recover."

**Solution:** Reverse this! Let winners run (trailing stops), cut losers quickly (fixed stops).

### ❌ Mistake 5: Position Sizes Based on "Feel"

**Problem:** "This is a sure thing, I'll go all-in!" (Famous last words before disaster)

**Solution:** Always use position sizing rules. No such thing as "sure thing."

## Risk Management Checklist

Before every trade, ask:

✅ **Position Size:** Is this position <5% of my portfolio?
✅ **Stop-Loss:** Where is my stop, and is it reasonable?
✅ **Risk-Reward:** Is this at least 2:1 risk-reward?
✅ **Portfolio Heat:** Will this push my total heat above 10%?
✅ **Diversification:** Am I too concentrated in one sector?
✅ **Thesis:** Can I explain in one sentence why I'm buying?
✅ **Exit Plan:** Do I know when I'll sell (both stop and target)?

If you can't check all boxes, **don't take the trade**.

## Key Takeaways

✅ **Losing 50% requires 100% gain to recover** - avoid big losses!
✅ **2% Rule:** Never risk more than 2% of portfolio on one trade
✅ **Position Size:** 3-7% per stock for most investors (10-15 total holdings)
✅ **Always use stop-losses** - typically 7-12% below entry
✅ **Trailing stops** lock in profits as winners rise
✅ **Risk-Reward minimum 2:1** - only take trades with favorable risk-reward
✅ **Diversify across 10-15 stocks** and multiple sectors
✅ **Portfolio Heat <10%** - total capital at risk across all positions
✅ **Honor your stops** - discipline separates winners from losers
✅ **Let winners run, cut losers quickly** - opposite of natural instinct!

## Related Terms

Master these risk concepts:

• `/glossary "stop-loss"`
• `/glossary "risk-reward ratio"`
• `/glossary "position sizing"`
• `/glossary "diversification"`
• `/glossary "volatility"`

## What's Next?

You now understand critical risk management!

**Complete Your Education:**
- `/learn portfolio` - Build complete portfolio strategies with risk management

**Or Start Practicing:**
- Apply risk management to paper trades
- Use `/trading-ideas` to find setups
- Calculate position sizes and stops
- Track performance with `/portfolio`

---

⚠️ **CRITICAL REMINDER:** Risk management isn't optional. It's the difference between surviving and thriving as an investor. Practice it in paper trading so it becomes second nature before risking real money!

💡 **Pro Tip:** Professional traders often say "Your first loss is your smallest loss." Don't hope and pray - honor your stops and live to trade another day!
