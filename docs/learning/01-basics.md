# MODULE 1: STOCK MARKET BASICS

## Overview

Welcome to your investing journey! This module covers the fundamental concepts you need to understand before trading stocks. You'll learn what stocks are, how markets work, and the basic mechanics of buying and selling shares.

**Duration:** ~15 minutes
**Prerequisites:** None
**Level:** Beginner

## What is a Stock?

### The Simple Definition

A **stock** (also called a "share" or "equity") represents partial ownership in a company. When you buy one share of Apple stock, you literally own a tiny piece of Apple Inc.

### Why Companies Sell Stock

Companies sell stock to raise money for growth without taking on debt. Instead of borrowing from banks, they sell pieces of ownership to public investors. In exchange, investors hope the company grows and the stock value increases.

**Example:**
Imagine you start a lemonade stand with $100. Business is great, and you want to expand to 5 stands but need $400 more. You could:
1. **Borrow $400** (debt - you pay interest)
2. **Sell 80% of your business** for $400 (equity - others own part of your company)

Public companies do option #2 by issuing stocks on stock exchanges.

## How Stock Markets Work

### Stock Exchanges

Stocks are bought and sold on **stock exchanges** - organized marketplaces where buyers and sellers meet. The two major US exchanges are:

- **NYSE (New York Stock Exchange)**: Traditional exchange with physical trading floor
- **NASDAQ**: Fully electronic exchange, home to many tech companies

**Example Companies:**
- NYSE: Walmart (WMT), Berkshire Hathaway (BRK.A), ExxonMobil (XOM)
- NASDAQ: Apple (AAPL), Microsoft (MSFT), Tesla (TSLA)

### Market Hours

US stock markets are open:
- **Regular Hours:** 9:30 AM - 4:00 PM Eastern Time, Monday-Friday
- **Pre-Market:** 4:00 AM - 9:30 AM ET (limited liquidity)
- **After-Hours:** 4:00 PM - 8:00 PM ET (limited liquidity)

Markets are closed on weekends and US holidays.

### Ticker Symbols

Every stock has a unique **ticker symbol** - a short code (1-5 letters) used to identify it.

**Examples:**
- AAPL = Apple Inc.
- TSLA = Tesla, Inc.
- MSFT = Microsoft Corporation
- GOOGL = Alphabet Inc. (Google)

This is the symbol you'll use in commands like `/trading-ideas AAPL` or `/paper-buy MSFT 10`.

## How Stock Prices Work

### Supply and Demand

Stock prices move based on **supply** (how many people want to sell) and **demand** (how many want to buy).

- **More buyers than sellers** → Price goes UP ⬆️
- **More sellers than buyers** → Price goes DOWN ⬇️

### Bid and Ask

At any moment, a stock has two prices:

- **Bid:** The highest price a buyer is willing to pay
- **Ask:** The lowest price a seller is willing to accept

**Example:**
- Apple stock Bid: $225.50
- Apple stock Ask: $225.52
- **Spread:** $0.02 (the difference)

When you place a market order, you get the ask price (if buying) or the bid price (if selling).

### Last Price vs Current Price

- **Last Price:** The price of the most recent trade
- **Current Price:** Generally refers to the last price, but the next trade could be different

Prices change constantly during market hours based on new buy/sell orders.

## Types of Orders

When you buy or sell stocks, you place an **order**. There are several types:

### 1. Market Order

**Definition:** Buy or sell immediately at the current market price.

**Pros:**
- Executes instantly (during market hours)
- Guaranteed to fill

**Cons:**
- You don't control the exact price
- Can be expensive during volatile markets

**Example:**
You place a market order to buy 10 shares of Apple. If the ask price is $225.52, you'll pay $2,255.20 (plus commission if applicable).

**When to use:** When you want to enter/exit quickly and price isn't critical.

### 2. Limit Order

**Definition:** Buy or sell only at a specific price or better.

**Pros:**
- You control the maximum price you pay (or minimum you receive)
- Prevents overpaying in volatile markets

**Cons:**
- May not execute if price doesn't reach your limit
- Could miss opportunities if stock moves away from your price

**Example:**
Apple is trading at $225, but you only want to buy if it drops to $220. You place a limit order to buy 10 shares at $220. Your order only fills if Apple drops to $220 or below.

**When to use:** When you have a target price and are willing to wait.

### 3. Stop-Loss Order

**Definition:** Automatically sell when the price drops to a specified level (to limit losses).

**How it works:** Your stop-loss becomes a market order once the "stop price" is hit.

**Example:**
You buy Apple at $225. To limit potential losses, you set a stop-loss at $203 (10% below entry). If Apple drops to $203, your shares automatically sell at the next available price.

**When to use:** Risk management - to automatically cut losses if stock moves against you.

⚠️ **Important:** Stop-losses can trigger during temporary dips, selling your position before recovery. Use carefully!

## Long vs Short Positions

### Long Position (Buying Stock)

When you **buy** stock, you have a "long position." You profit if the price goes UP.

**Example:**
- Buy 10 shares of Tesla at $250 = $2,500 investment
- Tesla rises to $300
- Sell 10 shares at $300 = $3,000
- **Profit: $500 (20% gain)**

This is what most investors do and what you'll practice with `/paper-buy`.

### Short Position (Selling Stock You Don't Own)

"Shorting" means betting a stock will go DOWN. You borrow shares, sell them, then buy them back cheaper later.

**Example:**
- Borrow 10 shares of Tesla at $250, sell immediately = $2,500 received
- Tesla drops to $200
- Buy back 10 shares at $200 = $2,000 spent
- **Profit: $500**

⚠️ **Risk Warning:** Short selling has unlimited risk! If the stock goes up instead of down, your losses can be massive. Short selling is NOT supported in this paper trading system and is not recommended for beginners.

## Making Money from Stocks

There are two ways to profit from stocks:

### 1. Capital Gains (Price Appreciation)

Buy low, sell high. The difference is your profit.

**Example:**
- Buy Amazon at $150
- Sell Amazon at $180
- **Capital Gain: $30 per share**

### 2. Dividends (Cash Payments)

Some companies pay **dividends** - regular cash payments to shareholders (usually quarterly).

**Example:**
Microsoft pays $0.75 per share quarterly ($3.00 annually).
- You own 100 shares
- You receive $75 every quarter ($300/year)
- This is passive income even if the stock price doesn't change

**Growth stocks** (like Tesla, Amazon) typically don't pay dividends - they reinvest profits into growth.
**Value stocks** (like Coca-Cola, Procter & Gamble) often pay steady dividends.

## Key Concepts

### Market Capitalization (Market Cap)

The total value of a company's stock.

**Formula:** Market Cap = Stock Price × Total Shares Outstanding

**Example:**
- Apple stock price: $225
- Total shares: 15.6 billion
- Market Cap: $225 × 15.6B = **$3.51 trillion**

**Company Size Categories:**
- **Large-cap:** >$10 billion (Apple, Microsoft, Amazon)
- **Mid-cap:** $2B - $10B (Smaller established companies)
- **Small-cap:** $300M - $2B (Smaller, often riskier companies)

### Volume

The number of shares traded in a period (usually one day).

**Why it matters:** High volume means easy to buy/sell (good **liquidity**). Low volume means harder to trade without moving the price.

**Example:**
Apple typically trades 50-70 million shares per day. A small company might trade only 100,000 shares per day, making it harder to buy large amounts without pushing the price up.

### Volatility

How much a stock's price moves up and down.

- **High volatility:** Large price swings (risky but potential for big gains) - Example: Tesla
- **Low volatility:** Steady, small price changes (safer but slower gains) - Example: Procter & Gamble

## Bull Markets vs Bear Markets

### Bull Market 🐂

A **bull market** is when stock prices are rising over an extended period (months or years). Investor confidence is high, economy is typically strong.

**Historical Example:** 2009-2020 was a long bull market after the 2008 financial crisis.

### Bear Market 🐻

A **bear market** is when stock prices fall 20% or more from recent highs and stay down. Investor pessimism, often during economic downturns.

**Historical Example:** March 2020 (COVID crash) - stocks fell 30-40% in weeks, then recovered.

**Memory trick:** Bulls thrust horns UP ⬆️, bears swipe claws DOWN ⬇️.

## Common Mistakes Beginners Make

### ❌ Mistake 1: Trading on Emotion

Buying when everyone is excited (at market tops) and selling in panic when prices drop (at market bottoms).

**Solution:** Create a plan before you invest. Use analysis (`/trading-ideas`) to make informed decisions, not emotional ones.

### ❌ Mistake 2: Not Using Stop-Losses

Letting losing positions run hoping they'll recover, while cutting winners too early.

**Solution:** Learn risk management (`/learn risk`). Set stop-losses to limit downside.

### ❌ Mistake 3: Ignoring Fees

In real trading, commissions and taxes eat into profits. A $100 profit might become $80 after fees and taxes.

**Solution:** Understand the full cost of trading. Paper trading has no fees, but real trading does!

### ❌ Mistake 4: Overtrading

Making too many trades, often based on short-term noise rather than sound analysis.

**Solution:** Quality over quantity. Fewer, well-researched trades often beat constant trading.

### ❌ Mistake 5: Not Diversifying

Putting all money into one stock. If that company fails, you lose everything.

**Solution:** Spread investments across multiple stocks (`/learn portfolio` for diversification strategies).

## Practical Application

### How to Use These Concepts

1. **Research a Stock**
   ```
   /trading-ideas AAPL
   ```
   This gives you professional analysis with BUY/SELL/HOLD recommendations.

2. **Make Your First Paper Trade**
   ```
   /paper-buy AAPL 10
   ```
   Buy 10 shares at current market price (simulated).

3. **Track Your Portfolio**
   ```
   /portfolio
   ```
   See your positions, profit/loss, and allocations.

4. **Practice Selling**
   ```
   /paper-sell AAPL 5
   ```
   Sell 5 shares to practice taking profits or cutting losses.

### Practice Exercise

**Task:** Research and execute a paper trade

1. Pick a company you use every day (Apple, Microsoft, Tesla, Amazon, etc.)
2. Run `/trading-ideas [TICKER]` to get analysis
3. Read the recommendation and price target
4. Decide if you'd buy based on the analysis
5. If yes, execute `/paper-buy [TICKER] [SHARES]`
6. Check `/portfolio` to see your new position

This simulates the full process: research → decision → execution → tracking.

## Key Takeaways

✅ **Stocks represent ownership** in companies
✅ **Markets operate based on supply and demand** - more buyers = higher prices
✅ **Ticker symbols** uniquely identify stocks (AAPL, TSLA, MSFT)
✅ **Market orders execute immediately**, limit orders wait for your price
✅ **Long positions profit when stocks rise** (this is normal stock buying)
✅ **Two ways to profit:** capital gains (price increase) and dividends (cash payments)
✅ **Market cap** shows company size (large-cap, mid-cap, small-cap)
✅ **Bull markets rise**, bear markets fall
✅ **Avoid common mistakes:** emotional trading, no stop-losses, overtrading, lack of diversification

## Related Terms

Look up these terms to deepen your understanding:

• `/glossary "market order"`
• `/glossary "limit order"`
• `/glossary "market cap"`
• `/glossary "dividend"`
• `/glossary "volatility"`
• `/glossary "bid-ask spread"`

## What's Next?

Congratulations! You now understand stock market fundamentals.

**Next Module:** `/learn fundamentals`

Learn how to analyze companies using financial statements, revenue growth, profit margins, and key metrics like P/E ratios. This is where you learn to distinguish good companies from bad ones.

---

💡 **Remember:** Paper trading lets you practice these concepts without risking real money. Use `/trading-ideas`, `/paper-buy`, and `/portfolio` to build your skills before considering real investments!
