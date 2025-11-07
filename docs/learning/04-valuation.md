# MODULE 4: VALUATION

## Overview

Valuation answers the critical question: "What is this company actually worth?" Learn professional methods to determine fair value and identify overpriced or underpriced stocks.

**Duration:** ~30 minutes
**Prerequisites:** Module 2 (Fundamentals)
**Level:** Intermediate-Advanced

## What is Valuation?

**Valuation** is the process of determining a company's intrinsic (true) value.

**Core Question:** If the stock price is $100, is the company worth more or less than $100 per share?

**The Goal:**
- If stock price < intrinsic value → **UNDERVALUED** (potential buy)
- If stock price > intrinsic value → **OVERVALUED** (potential sell)
- If stock price ≈ intrinsic value → **FAIRLY VALUED** (hold or pass)

⚠️ **Important:** Valuation is part art, part science. Different methods produce different results. Use multiple approaches.

## Valuation Methods Overview

Professional analysts use these main approaches:

1. **Relative Valuation** - Compare to similar companies (P/E, P/S, EV/EBITDA)
2. **Discounted Cash Flow (DCF)** - Project future cash flows and discount to present value
3. **Asset-Based Valuation** - Sum of company's assets minus liabilities

We'll focus on the most practical methods for equity investors.

## Relative Valuation (Multiples)

### P/E Ratio (Price-to-Earnings)

**Formula:** P/E = Stock Price / Earnings Per Share

**How to Use for Valuation:**

**Step 1:** Find comparable companies' average P/E
**Step 2:** Apply that multiple to your company's EPS
**Step 3:** Compare to current stock price

**Example:**
```
Tech Company Comparison:
Microsoft:  P/E = 32x, EPS = $11.50
Google:     P/E = 24x, EPS = $6.80
Meta:       P/E = 28x, EPS = $14.50
Average P/E: 28x

Target Company (Adobe): EPS = $15.00
Fair Value = 28 × $15.00 = $420 per share
Current Price: $480
Conclusion: Overvalued by 14% ($480 vs $420)
```

**When to Use:** Companies with stable, positive earnings

**Limitations:**
- Doesn't work for unprofitable companies
- Ignores growth rates
- Sensitive to accounting changes

### PEG Ratio (P/E to Growth)

**Formula:** PEG = P/E Ratio / Expected Earnings Growth Rate

**Purpose:** Adjusts P/E for growth expectations

**Interpretation:**
- **PEG < 1:** Potentially undervalued relative to growth
- **PEG = 1:** Fair value
- **PEG > 1:** Potentially overvalued

**Example:**
```
Company A: P/E = 30, Expected Growth = 15%
PEG = 30 / 15 = 2.0 (expensive for growth rate)

Company B: P/E = 25, Expected Growth = 30%
PEG = 25 / 30 = 0.83 (cheaper relative to growth)
```

**When to Use:** Growth companies where P/E alone seems high

### P/S Ratio (Price-to-Sales)

**Formula:** P/S = Market Cap / Annual Revenue

**How to Use:**

**Example:**
```
Cloud Software Companies:
Salesforce: P/S = 6.5x
Workday:    P/S = 7.2x
ServiceNow: P/S = 12.0x
Average:    8.6x

Target Company: Revenue = $5 billion
Fair Value = 8.6 × $5B = $43B market cap
Current Market Cap: $50B
Conclusion: Overvalued by 16%
```

**When to Use:**
- Young companies not yet profitable
- Companies with negative earnings
- Comparing revenue-focused businesses

### EV/EBITDA (Enterprise Value to EBITDA)

**Enterprise Value (EV):** Market Cap + Debt - Cash

**Formula:** EV/EBITDA = Enterprise Value / EBITDA

**Why Better Than P/E:** Accounts for debt and is less affected by accounting choices

**Example:**
```
Company Valuation:
Market Cap: $100B
Debt: $20B
Cash: $10B
Enterprise Value: $100B + $20B - $10B = $110B

EBITDA: $10B
EV/EBITDA = $110B / $10B = 11x

Industry Average EV/EBITDA: 9x
Conclusion: Trading at premium to peers (11x vs 9x)
```

**When to Use:**
- Comparing companies with different capital structures
- Mature, capital-intensive businesses
- M&A scenarios (buyers care about EV, not just equity value)

**Industry Benchmarks:**
- Technology: 15-25x
- Industrials: 8-12x
- Utilities: 6-10x
- High-growth: 20-40x+

## Discounted Cash Flow (DCF) Valuation

### The Concept

**DCF Logic:** A company is worth the present value of all future cash flows it will generate.

**Why Discount?** A dollar today is worth more than a dollar tomorrow (time value of money).

### DCF Steps

**Step 1: Project Free Cash Flows (FCF) for 5-10 years**

Example (simplified):
```
Year 1: $5.0B
Year 2: $5.5B (+10% growth)
Year 3: $6.0B (+9% growth)
Year 4: $6.5B (+8% growth)
Year 5: $7.0B (+8% growth)
```

**Step 2: Calculate Terminal Value**

What's the company worth beyond your projection period?

**Formula:** Terminal Value = Final Year FCF × (1 + perpetual growth rate) / (discount rate - perpetual growth rate)

**Example:**
```
Year 5 FCF: $7.0B
Perpetual growth: 3%
Discount rate: 10%
Terminal Value = $7.0B × 1.03 / (0.10 - 0.03) = $103B
```

**Step 3: Discount Everything to Present Value**

**Formula:** PV = Future Value / (1 + discount rate)^years

**Example:**
```
Year 1 PV: $5.0B / 1.10^1 = $4.55B
Year 2 PV: $5.5B / 1.10^2 = $4.55B
Year 3 PV: $6.0B / 1.10^3 = $4.51B
Year 4 PV: $6.5B / 1.10^4 = $4.44B
Year 5 PV: $7.0B / 1.10^5 = $4.35B
Terminal PV: $103B / 1.10^5 = $63.95B

Total Enterprise Value: $86.35B
```

**Step 4: Calculate Per-Share Value**

```
Enterprise Value: $86.35B
- Debt: $10B
+ Cash: $5B
= Equity Value: $81.35B

Shares Outstanding: 1B
Fair Value Per Share: $81.35
```

### DCF Challenges

⚠️ **Highly Sensitive to Assumptions:**
- 1% change in discount rate or growth rate dramatically changes valuation
- Garbage in, garbage out (bad assumptions = bad valuation)
- Long-term projections are difficult and often wrong

**When DCF Works Best:**
- Mature companies with predictable cash flows
- Capital-intensive businesses (utilities, industrials)
- Companies with long operating history

**When to Avoid DCF:**
- Early-stage, unprofitable companies
- Highly cyclical businesses
- Biotechs (binary outcomes)

## Scenario Analysis (Bull/Base/Bear)

Professional analysts create multiple valuations for different outcomes.

### Three Scenarios

**Example: Valuing a SaaS Company**

**1. Bull Case ($150 per share)**
- Revenue grows 30% annually (vs 20% base case)
- Margins expand to 25% (vs 20% base case)
- P/S multiple of 12x (premium to peers)
- **Probability: 25%**

**2. Base Case ($100 per share)**
- Revenue grows 20% annually
- Margins stable at 20%
- P/S multiple of 8x (in-line with peers)
- **Probability: 50%**

**3. Bear Case ($60 per share)**
- Revenue grows only 10% (competition intensifies)
- Margins compress to 15%
- P/S multiple of 5x (discount to peers)
- **Probability: 25%**

### Probability-Weighted Fair Value

**Formula:** Fair Value = (Bull × Prob) + (Base × Prob) + (Bear × Prob)

**Example:**
```
Fair Value = ($150 × 0.25) + ($100 × 0.50) + ($60 × 0.25)
          = $37.50 + $50.00 + $15.00
          = $102.50

Current Price: $95
Conclusion: Undervalued by 7.9% → POTENTIAL BUY
```

**Why This Approach?** Accounts for uncertainty and multiple outcomes rather than single-point estimates.

## Comparing Valuation Methods

**Example: Valuing Company XYZ (Current Price: $120)**

| Method | Fair Value | Implied Rating | Weight |
|--------|------------|----------------|--------|
| P/E Comps | $110 | Overvalued -8% | 30% |
| EV/EBITDA | $125 | Undervalued +4% | 25% |
| P/S Comps | $115 | Overvalued -4% | 20% |
| DCF | $130 | Undervalued +8% | 25% |

**Weighted Average Fair Value:**
```
= ($110 × 0.30) + ($125 × 0.25) + ($115 × 0.20) + ($130 × 0.25)
= $33 + $31.25 + $23 + $32.50
= $119.75
```

**Conclusion:** Current price $120 ≈ Fair Value $119.75 → **FAIRLY VALUED / HOLD**

## Practical Application

### Using Valuation in `/trading-ideas`

When you run `/trading-ideas [TICKER]`, the Valuation section includes:

- Price targets from multiple analysts
- Bull/base/bear scenarios
- Key valuation multiples vs peers
- Probability weightings
- Upside/downside calculations

**Example Output:**
```
VALUATION & PRICE TARGETS:
Current consensus: $225 (range $210-$245). Bull case $260 assumes strong
iPhone 16 cycle and services growth acceleration. Base case $225 reflects
steady growth. Bear case $190 on macro weakness. Probability weighting:
25%/50%/25%. Current P/E 28x vs sector 25x (slight premium justified by
ecosystem moat).
```

### Practice Exercise

**Task:** Perform relative valuation

1. Pick an industry (e.g., social media, cloud software, automotive)
2. Run `/trading-ideas` on 3-4 companies in that industry
3. Compare their key multiples:
   - P/E ratios
   - P/S ratios
   - EV/EBITDA (if shown)
   - Growth rates
4. Calculate average multiples for the group
5. Identify which stock appears cheapest/most expensive relative to peers
6. Consider if the valuation gap is justified by fundamentals
7. Make paper trade based on your analysis

**Example:**
```
/trading-ideas AAPL
/trading-ideas MSFT
/trading-ideas GOOGL

Compare P/E ratios:
AAPL: 28x, MSFT: 32x, GOOGL: 24x
Average: 28x

GOOGL at 24x looks cheap relative to peers. Why?
- Slower growth? Regulatory risks? Justified discount?
If fundamentals are strong, might be a buy opportunity.
```

## Common Valuation Mistakes

### ❌ Mistake 1: Using Only One Method

Each method has limitations. One method can be misleading.

**Solution:** Use 2-3 methods and triangulate to a range.

### ❌ Mistake 2: Ignoring Industry Context

A P/E of 15x is expensive for a bank, cheap for a tech company.

**Solution:** Always compare to industry peers and historical norms.

### ❌ Mistake 3: Overly Precise DCF Models

"The company is worth $47.32 per share" - false precision!

**Solution:** Think in ranges: "Fair value $40-$50 range."

### ❌ Mistake 4: Anchoring to Current Price

Assuming current price is roughly correct and working backwards.

**Solution:** Do valuation independently, then compare to market price.

### ❌ Mistake 5: Ignoring Qualitative Factors

Numbers aren't everything. Brand, moat, management matter.

**Solution:** Adjust valuations for competitive advantages or disadvantages.

## Key Takeaways

✅ **Valuation determines if a stock is cheap or expensive** relative to intrinsic worth
✅ **P/E ratio** compares price to earnings (most common multiple)
✅ **PEG ratio** adjusts P/E for growth expectations
✅ **EV/EBITDA** better for comparing companies with different debt levels
✅ **DCF values future cash flows** discounted to present value (sensitive to assumptions)
✅ **Bull/base/bear scenarios** account for multiple outcomes with probabilities
✅ **Use multiple methods** and triangulate to a valuation range
✅ **Compare to peers** within the same industry
✅ **Price targets in `/trading-ideas`** show professional analyst valuations

## Related Terms

Deep dive into these concepts:

• `/glossary "P/E ratio"`
• `/glossary "PEG ratio"`
• `/glossary "enterprise value"`
• `/glossary "DCF"`
• `/glossary "intrinsic value"`

## What's Next?

You now understand how to value companies!

**Recommended Next:**
- `/learn risk` - CRITICAL: Learn risk management before trading real money
- `/learn portfolio` - Build diversified portfolios using valuation insights

---

💡 **Key Insight:** In `/trading-ideas` reports, analysts provide bull/base/bear valuations. Understanding these scenarios helps you assess if the current price offers good risk-reward!
