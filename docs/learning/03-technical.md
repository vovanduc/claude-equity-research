# MODULE 3: TECHNICAL ANALYSIS

## Overview

Technical analysis studies price charts and trading patterns to predict future movements. While fundamental analysis asks "what is the business worth?", technical analysis asks "what does price action tell us?"

**Duration:** ~20 minutes
**Prerequisites:** Module 1 (Basics)
**Level:** Intermediate

## What is Technical Analysis?

**Technical analysis** examines historical price and volume data to identify trading opportunities.

**Core Belief:** "The market price reflects all available information, and patterns repeat due to human psychology."

**What Technicians Study:**
- Chart patterns (support, resistance, trends)
- Indicators (RSI, MACD, moving averages)
- Volume and momentum
- Entry and exit timing

⚠️ **Important:** Technical analysis works best for **timing** trades, not determining **what** to buy. Combine with fundamentals for best results.

## Charts and Price Action

### Reading a Stock Chart

Stock charts plot price over time. Key elements:

- **X-axis:** Time (minutes, hours, days, months)
- **Y-axis:** Price
- **Green candles/bars:** Price closed higher than it opened (bullish)
- **Red candles/bars:** Price closed lower than it opened (bearish)

**Example:**
```
Price Chart for AAPL (Daily)
$230 |              ╱╲
$225 |          ╱╲╱  ╲
$220 |      ╱╲╱      ╲╱╲
$215 |  ╱╲╱
$210 |╱
     └─────────────────────→ Time
```

### Support and Resistance

**Support:** Price level where buying interest is strong enough to prevent further declines.
**Resistance:** Price level where selling pressure prevents further gains.

**Think of it like:**
- Support = floor (price bounces up)
- Resistance = ceiling (price bounces down)

**Example:**
- Tesla repeatedly bounces at $200 → **$200 is support**
- Tesla repeatedly fails to break $250 → **$250 is resistance**

**Trading Strategy:**
- Buy near support (expecting bounce)
- Sell near resistance (expecting rejection)
- **Breakout:** If price breaks through resistance, it may become new support

### Trends

**Trend:** The general direction of price movement.

**Three Types:**
1. **Uptrend:** Higher highs and higher lows (🔺 bullish)
2. **Downtrend:** Lower highs and lower lows (🔻 bearish)
3. **Sideways/Range:** Moving between support and resistance (neutral)

**Trading Wisdom:** "The trend is your friend." Don't fight the prevailing direction.

**Example:**
```
Uptrend:
       ╱╲     ╱╲
      ╱  ╲   ╱  ╲
     ╱    ╲ ╱
    ╱      ╱      (Each low higher than previous)
```

### Volume

**Volume:** Number of shares traded in a period.

**Why It Matters:** Volume confirms price moves.

- **Price up + high volume** = Strong bullish signal
- **Price up + low volume** = Weak move, may reverse
- **Price down + high volume** = Strong bearish signal
- **Price down + low volume** = Weak selloff, may bounce

**Example:** Stock breaks resistance at $100 with 3x average volume → Strong confirmation of breakout.

## Key Technical Indicators

### 1. Moving Averages (MA)

**Definition:** Average price over X periods. Smooths out noise to show trends.

**Common Types:**
- **50-day MA:** Medium-term trend
- **200-day MA:** Long-term trend

**Golden Cross:** When 50-day MA crosses above 200-day MA (bullish signal)
**Death Cross:** When 50-day MA crosses below 200-day MA (bearish signal)

**Trading Strategy:**
- Price above MA = bullish bias
- Price below MA = bearish bias
- MA can act as dynamic support/resistance

**Example:**
- Apple trading at $225, 50-day MA at $220 → Price above MA (bullish)
- If Apple falls to $220, the MA might provide support

### 2. Relative Strength Index (RSI)

**Definition:** Momentum indicator showing if a stock is overbought or oversold.

**Scale:** 0 to 100

**Interpretation:**
- **RSI > 70:** Overbought (potential pullback coming)
- **RSI < 30:** Oversold (potential bounce coming)
- **RSI 40-60:** Neutral territory

**Example:**
- Stock at $150, RSI = 82 → Overbought, consider waiting for pullback
- Stock at $120, RSI = 25 → Oversold, potential buy opportunity

**Limitations:** In strong trends, stocks can stay overbought/oversold for extended periods.

### 3. MACD (Moving Average Convergence Divergence)

**Definition:** Shows relationship between two moving averages to identify momentum changes.

**Components:**
- MACD line
- Signal line
- Histogram (difference between the two)

**Signals:**
- **MACD crosses above signal line:** Bullish (potential buy)
- **MACD crosses below signal line:** Bearish (potential sell)
- **Histogram expanding:** Momentum increasing
- **Histogram shrinking:** Momentum weakening

**Example:**
MACD crosses above signal line while stock at $200 → Consider buying for potential upward momentum.

### 4. Bollinger Bands

**Definition:** Bands placed above and below a moving average showing volatility.

**Components:**
- Middle band: 20-day MA
- Upper band: 2 standard deviations above MA
- Lower band: 2 standard deviations below MA

**Interpretation:**
- **Price at upper band:** Potentially overbought
- **Price at lower band:** Potentially oversold
- **Bands contracting:** Low volatility (breakout may be coming)
- **Bands expanding:** High volatility

**Trading Strategy:** Buy when price touches lower band, sell when it touches upper band (works best in ranging markets).

## Chart Patterns

### Bullish Patterns

#### 1. Cup and Handle

Shape: Rounded bottom (cup) followed by small consolidation (handle).

**Signal:** Breakout from handle = strong buy signal

**Example:**
```
     ╱──╲    (handle)
   ╱      ╲╱
 ╱          (cup)
```

#### 2. Double Bottom (W Pattern)

Price drops, bounces, drops to similar level, then rallies.

**Signal:** Second bottom holds = bullish reversal

#### 3. Ascending Triangle

Price forms higher lows while resistance stays flat.

**Signal:** Breakout above resistance = buy signal

### Bearish Patterns

#### 1. Head and Shoulders

Three peaks: left shoulder, higher head, right shoulder.

**Signal:** Break below "neckline" = sell signal

#### 2. Double Top (M Pattern)

Price rises, pulls back, rises to similar level, then falls.

**Signal:** Second peak fails = bearish reversal

#### 3. Descending Triangle

Price forms lower highs while support holds flat.

**Signal:** Breakdown below support = sell signal

⚠️ **Pattern Reliability:** Patterns work ~60-70% of the time. Never rely on patterns alone - confirm with volume and fundamentals.

## Practical Application

### How Technical Analysis Appears in `/trading-ideas`

When you run `/trading-ideas [TICKER]`, the technical analysis section includes:

- Current trend direction
- Key support and resistance levels
- RSI and momentum indicators
- Moving average positions
- Recent pattern formations

**Example Output:**
```
TECHNICAL CONTEXT:
Stock trading above 50-day MA ($220) and 200-day MA ($210) - bullish alignment.
RSI at 58 (neutral). Resistance at $230, support at $220. Momentum positive
with MACD showing bullish crossover. Volume above average on recent gains.
```

### Using Technical Analysis for Entry/Exit

**Scenario 1: Finding Entry Point**
1. `/trading-ideas AAPL` shows BUY rating (fundamental thesis)
2. Technical section shows: "Stock pulled back to support at $220, RSI at 35 (oversold)"
3. **Action:** `/paper-buy AAPL [SHARES]` - Buy at support with oversold RSI

**Scenario 2: Taking Profits**
1. Your AAPL position is up 15%
2. Technical section shows: "Stock at resistance $250, RSI at 75 (overbought)"
3. **Action:** `/paper-sell AAPL [SHARES]` - Take profits at resistance

### Practice Exercise

**Task:** Use technical analysis to time a trade

1. Run `/trading-ideas [TICKER]` on a stock
2. Read the Technical Context section
3. Identify:
   - Current trend (up, down, sideways)
   - Support and resistance levels
   - RSI level (overbought/oversold/neutral)
   - Position relative to moving averages
4. Decide if technical setup is favorable
5. If yes, execute trade with technical levels in mind
6. Set mental stop-loss below support level

## Combining Technical and Fundamental Analysis

**Best Approach:** Use fundamentals to **decide WHAT to buy**, technical to **decide WHEN to buy**.

**Example Workflow:**
1. **Fundamental screening:** `/trading-ideas MSFT` → BUY rating, strong growth, good margins
2. **Technical timing:** Wait for pullback to support or buy on breakout above resistance
3. **Execute:** `/paper-buy MSFT [SHARES]` at favorable technical entry
4. **Risk management:** Place stop-loss below support level

**Why This Works:**
- Fundamentals ensure you're buying quality companies
- Technicals help you avoid buying at tops and selling at bottoms
- Combined approach improves risk-reward ratio

## Common Mistakes

### ❌ Mistake 1: Relying Only on Technical Analysis

Ignoring fundamentals can lead to buying technically strong but fundamentally broken companies.

**Solution:** Always check fundamental health first.

### ❌ Mistake 2: Overcomplicating with Too Many Indicators

Using 10 indicators creates confusion and contradictory signals.

**Solution:** Pick 2-3 indicators you understand well (e.g., moving averages, RSI, volume).

### ❌ Mistake 3: Ignoring Volume

Price moves without volume confirmation often reverse.

**Solution:** Always check if volume supports the price action.

### ❌ Mistake 4: Fighting the Trend

Trying to catch falling knives (buy during strong downtrends).

**Solution:** Wait for trend reversal signals before entering.

### ❌ Mistake 5: Pattern Obsession

Seeing patterns everywhere and forcing trades.

**Solution:** Wait for clear, high-probability setups.

## When Technical Analysis Works Best

✅ **Short-term trading:** Day trading and swing trading (days to weeks)
✅ **Timing entries/exits:** Finding optimal buy/sell points
✅ **High-liquidity stocks:** Large-cap stocks with consistent volume
✅ **Trending markets:** Clear directional moves

## When to Be Cautious with Technicals

⚠️ **News-driven events:** Earnings, FDA approvals, major announcements
⚠️ **Low-volume stocks:** Patterns less reliable with thin trading
⚠️ **Long-term investing:** Multi-year holds care less about short-term chart patterns
⚠️ **Fundamental shifts:** Company business model changes invalidate technical patterns

## Key Takeaways

✅ **Technical analysis studies price action** and chart patterns
✅ **Support/resistance** are key levels where price tends to reverse
✅ **Trends** (up/down/sideways) guide trading direction
✅ **Volume confirms price moves** - high volume adds conviction
✅ **Moving averages** show trends and act as dynamic support/resistance
✅ **RSI** shows overbought (>70) and oversold (<30) conditions
✅ **Combine with fundamentals** - use fundamentals for WHAT, technicals for WHEN
✅ **Patterns work ~60-70%** of the time - never rely on one signal

## Related Terms

Learn more about these concepts:

• `/glossary "support"`
• `/glossary "resistance"`
• `/glossary "RSI"`
• `/glossary "moving average"`
• `/glossary "volume"`
• `/glossary "MACD"`

## What's Next?

You now understand technical analysis basics!

**Next Options:**
- `/learn valuation` - Learn advanced valuation methods
- `/learn risk` - Critical risk management strategies
- `/learn portfolio` - Portfolio construction and diversification

---

💡 **Practice Tip:** In `/trading-ideas` reports, pay attention to the Technical Context section. Over time, you'll learn which technical setups work best for your trading style!
