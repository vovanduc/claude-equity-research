# Claude Equity Research

[![Built with Claude Code](https://img.shields.io/badge/Built%20with-Claude%20Code-blue?logo=anthropic&logoColor=white)](https://claude.ai/claude-code)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Claude Code Required](https://img.shields.io/badge/Claude_Code-Required-blue.svg)
![Status: Active](https://img.shields.io/badge/Status-Active-green.svg)

>🤖 Built entirely with Claude Code - demonstrating AI-native development workflows for professional-grade financial tools.

Professional equity research and trading analysis powered by Claude AI, delivering institutional-grade investment insights with Goldman Sachs-style formatting and comprehensive risk assessment.

## What It Does

- **Institutional-Grade Analysis**: Generates professional equity research reports matching Wall Street standards
- **AI-Powered Intelligence**: Leverages Claude AI for comprehensive fundamental and technical analysis
- **Real-Time Data Integration**: Pulls live market data, earnings reports, and analyst coverage
- **Risk-Adjusted Recommendations**: Provides buy/sell/hold ratings with specific price targets and position sizing
- **Advanced Market Intelligence**: Includes options flow analysis, insider trading activity, and sector positioning

## Key Features

### 📊 Equity Research & Analysis
- **Institutional-Grade Reports**: `/trading-ideas` generates professional research with BUY/SELL/HOLD recommendations
- **Comprehensive Framework**: 8-section analysis including fundamentals, catalysts, valuation, and risk assessment
- **Real-Time Intelligence**: Live market data, earnings reports, analyst coverage, and insider activity
- **Advanced Metrics**: Options flow, sector positioning, technical indicators, and ESG scores

### 💼 Paper Trading Portfolio (NEW!)
- **Simulated Trading**: Practice investing with $100,000 virtual capital
- **Portfolio Tracking**: `/portfolio` shows positions, P&L, and performance metrics
- **Realistic Execution**: `/paper-buy` and `/paper-sell` commands for full trading simulation
- **Risk Management**: Position sizing warnings, allocation tracking, and stop-loss practice
- **Transaction History**: Complete trade history with realized gains/losses
- **Learn Risk-Free**: Build confidence and test strategies without real money

### 🎓 Interactive Learning System (NEW!)
- **Structured Curriculum**: 6 progressive modules from beginner to advanced
- **Comprehensive Topics**:
  - `/learn basics` - Stock market fundamentals (15 min)
  - `/learn fundamentals` - Financial analysis & metrics (25 min)
  - `/learn technical` - Chart patterns & indicators (20 min)
  - `/learn valuation` - DCF, multiples, price targets (30 min)
  - `/learn risk` - Risk management & position sizing (20 min) **← CRITICAL**
  - `/learn portfolio` - Diversification & portfolio construction (25 min)
- **Real Examples**: Every concept includes specific numbers and real company examples
- **Practice Exercises**: Apply learning with `/trading-ideas` and paper trading

### 📖 Financial Terminology Glossary (NEW!)
- **50+ Key Terms**: `/glossary` provides instant definitions with examples
- **Categorized by Topic**: Fundamental, technical, valuation, risk management, and trading terms
- **Beginner-Friendly**: Clear explanations without jargon
- **Integrated Learning**: Links to relevant `/learn` modules for deeper understanding
- **Search by Term**: Look up P/E ratio, EBITDA, stop-loss, and more

### Professional Standards
- **Institutional Terminology**: EBITDA, P/E ratios, EV/Sales, conviction levels
- **Probability Weighting**: Bull/base/bear scenarios with percentage allocations
- **Legal Protection**: Comprehensive disclaimers for educational use
- **Data Sourcing**: Real-time web search with analyst firm citations
- **Educational Focus**: Designed for learning and skill development

## Installation & Setup

### Prerequisites
- Claude Code CLI (version 2.0.11 or higher)
- Claude paid subscription (Pro, Team, or Enterprise)
- Internet connection for real-time data retrieval

### Installation via Claude Code Plugin (Recommended)

**Quick Install - Interactive Menu:**
```bash
# Step 1: Add the marketplace
/plugin marketplace add quant-sentiment-ai/claude-equity-research

# Step 2: Open the plugin menu
/plugin

# Step 3: Select "Browse Plugins" → find "claude-equity-research" → "Install now"
```

**Alternative - Direct Install:**
```bash
/plugin marketplace add quant-sentiment-ai/claude-equity-research
/plugin install claude-equity-research@quant-sentiment-ai
```

**Verify Installation:**
```bash
/help  # Confirm /trading-ideas command is listed
```

**Start Analyzing:**
```bash
/trading-ideas AAPL
/trading-ideas NVDA --detailed
```

> 💡 **Tip**: Restart Claude Code after installation for best results.

For comprehensive plugin documentation, see [PLUGIN.md](PLUGIN.md).

<details>
<summary><strong>Manual Installation (Advanced)</strong></summary>

### Quick Start

1. **Install the /trading-ideas command** (system-wide):
```bash
mkdir -p ~/.claude/commands
curl -o ~/.claude/commands/trading-ideas.md https://raw.githubusercontent.com/quant-sentiment-ai/claude-equity-research/main/commands/trading-ideas.md
```

2. **Basic usage**:
```bash
/trading-ideas AAPL
```

3. **Enhanced analysis**:
```bash
/trading-ideas HOOD --detailed
```

### Manual Setup via Git Clone

1. **Clone the repository**:
```bash
git clone https://github.com/quant-sentiment-ai/claude-equity-research.git
cd claude-equity-research
```

2. **Copy command to Claude Code**:
```bash
cp commands/trading-ideas.md ~/.claude/commands/
```

</details>

## Usage Examples

### Complete Beginner Workflow (Start Here!)

```bash
# 1. Learn the basics
/learn basics

# 2. Research your first stock
/trading-ideas AAPL

# 3. Make your first paper trade
/paper-buy AAPL 10

# 4. Check your portfolio
/portfolio

# 5. Look up unfamiliar terms
/glossary "P/E ratio"
```

### Equity Research & Analysis

#### Basic Analysis
```bash
/trading-ideas AAPL
```
**Output**: Comprehensive institutional research report with BUY/SELL/HOLD recommendation

#### Technology Sector
```bash
/trading-ideas NVDA
```
**Features**: AI/semiconductor sector positioning, relative valuation vs peers

#### Financial Services
```bash
/trading-ideas JPM
```
**Includes**: Interest rate sensitivity, regulatory environment, book value analysis

### Paper Trading Examples

#### Building a Diversified Portfolio
```bash
# Research and buy tech stocks
/trading-ideas AAPL
/paper-buy AAPL 25

/trading-ideas MSFT
/paper-buy MSFT 10

# Add healthcare diversification
/trading-ideas JNJ
/paper-buy JNJ 20

# Check portfolio allocation
/portfolio --detailed
```

#### Taking Profits
```bash
# Stock is up 15%, time to take partial profits
/paper-sell AAPL 10       # Sell 40% of position
/portfolio                # Check remaining position
```

#### Practice Risk Management
```bash
# Stock hit your stop-loss level
/paper-sell TSLA ALL      # Exit full position
/learn risk              # Review risk management concepts
```

### Learning Path Examples

#### For Complete Beginners
```bash
# Day 1: Learn fundamentals
/learn basics
/learn fundamentals

# Day 2: Practice research
/trading-ideas AAPL
/trading-ideas MSFT
/glossary "market cap"

# Day 3: Start paper trading
/paper-buy AAPL 10
/portfolio
```

#### For Intermediate Investors
```bash
# Deep dive into analysis
/learn technical
/learn valuation

# Apply to real stocks
/trading-ideas NVDA      # Note technical levels and valuation
/paper-buy NVDA 5        # Enter with risk management
```

### Glossary Usage Examples

```bash
# Browse all terms
/glossary

# Look up specific terms
/glossary "P/E ratio"
/glossary "EBITDA"
/glossary "stop-loss"

# Multi-word terms
/glossary "risk-reward ratio"
/glossary "free cash flow"
```

## Sample Output Format

```
# APPLE INC (AAPL) - ENHANCED EQUITY RESEARCH

## EXECUTIVE SUMMARY
BUY with $250 price target (9% upside) over 12 months. Strong Q4 2024 
results driven by iPhone 16 launch and AI integration provide foundation 
for premium product cycle. Balanced risk-reward with established ecosystem moat.

## FUNDAMENTAL ANALYSIS
Q4 2024: Revenue $94.9B (+6% YoY), EPS $1.64 (+12% YoY). iPhone revenue 
$46.2B (~49% of total), Services +12% to $25B with recurring characteristics.

## VALUATION & PRICE TARGETS
Consensus: $242 (range $200-$280)
Bull case: $280 | Base case: $250 | Bear case: $200
Probability weighting: 25%/55%/20%

## RECOMMENDATION: BUY | Conviction: High | Price Target: $250
```

## Command Reference

### All Available Commands

| Command | Description | Usage | Output |
|---------|-------------|-------|--------|
| **Equity Research** ||||
| `/trading-ideas <TICKER>` | Institutional-grade equity analysis | `/trading-ideas AAPL` | 8-section comprehensive report with BUY/SELL/HOLD |
| `/trading-ideas <TICKER> --detailed` | Enhanced analysis with options flow | `/trading-ideas NVDA --detailed` | Extended technical and insider analysis |
| **Paper Trading** ||||
| `/portfolio` | View portfolio summary | `/portfolio` | Positions, P&L, allocation |
| `/portfolio --detailed` | Detailed portfolio view | `/portfolio --detailed` | Full breakdown with transactions |
| `/paper-buy <TICKER> <SHARES>` | Buy stocks (simulated) | `/paper-buy AAPL 25` | Trade confirmation, updated position |
| `/paper-buy <TICKER> <SHARES> <PRICE>` | Buy at specific price | `/paper-buy MSFT 10 380.50` | Trade execution with price control |
| `/paper-sell <TICKER> <SHARES>` | Sell stocks (simulated) | `/paper-sell AAPL 10` | Realized P&L, remaining position |
| `/paper-sell <TICKER> ALL` | Sell entire position | `/paper-sell TSLA ALL` | Position closed, total P&L |
| **Learning System** ||||
| `/learn` | Show learning path overview | `/learn` | 6 modules with descriptions |
| `/learn basics` | Stock market fundamentals | `/learn basics` | 15-min beginner module |
| `/learn fundamentals` | Financial analysis | `/learn fundamentals` | 25-min financial metrics module |
| `/learn technical` | Technical analysis | `/learn technical` | 20-min chart patterns module |
| `/learn valuation` | Valuation methods | `/learn valuation` | 30-min DCF and multiples |
| `/learn risk` | Risk management ⚠️ CRITICAL | `/learn risk` | 20-min position sizing & stops |
| `/learn portfolio` | Portfolio management | `/learn portfolio` | 25-min diversification |
| **Glossary** ||||
| `/glossary` | Browse all financial terms | `/glossary` | Categorized term list |
| `/glossary <TERM>` | Look up specific term | `/glossary "P/E ratio"` | Definition with examples |

## Repository Structure

```
claude-equity-research/
├── .claude-plugin/
│   └── marketplace.json          # Plugin marketplace definition (6 commands)
├── commands/
│   ├── trading-ideas.md          # Equity research analysis command
│   ├── portfolio.md              # Portfolio viewing command
│   ├── paper-buy.md              # Simulated buy orders
│   ├── paper-sell.md             # Simulated sell orders
│   ├── learn.md                  # Learning system command
│   ├── glossary.md               # Financial terminology lookup
│   └── README.md                 # Command documentation
├── docs/
│   ├── methodology.md            # Analysis framework
│   ├── installation.md           # Setup instructions
│   ├── customization.md          # Customization guide
│   ├── portfolio-guide.md        # Paper trading guide (NEW!)
│   ├── glossary-terms.md         # Financial term definitions (NEW!)
│   └── learning/                 # Learning modules (NEW!)
│       ├── 01-basics.md          # Stock market fundamentals
│       ├── 02-fundamentals.md    # Financial analysis
│       ├── 03-technical.md       # Technical analysis
│       ├── 04-valuation.md       # Valuation methods
│       └── 05-risk.md            # Risk management ⚠️
├── examples/
│   ├── sample_reports/           # Example equity analyses
│   │   ├── AAPL_analysis.md      # Apple BUY example
│   │   └── HOOD_analysis.md      # Robinhood HOLD example
│   └── sample_portfolio.json     # Example portfolio state (NEW!)
├── config/
│   └── config.example.json       # Template configuration
├── README.md                     # This file
├── PLUGIN.md                     # Plugin system documentation
├── CLAUDE.md                     # Claude Code guidance
├── LICENSE                       # MIT License
└── SECURITY.md                   # Security policy

User Data Storage (created on first use):
~/.claude/equity-research/
├── portfolio.json                # Current positions and cash
└── transactions.json             # Complete trade history
```

## Analysis Methodology

Our research framework combines:

### Quantitative Analysis
- **Financial Statements**: Revenue, margins, cash flow analysis
- **Valuation Models**: Multiple approaches (DCF, comparable company, precedent transaction)
- **Technical Indicators**: Support/resistance, momentum, relative strength
- **Options Analytics**: Implied volatility, unusual activity, sentiment indicators

### Qualitative Assessment
- **Competitive Positioning**: Market share, competitive advantages, moat analysis
- **Management Quality**: Track record, capital allocation, strategic vision
- **Regulatory Environment**: Industry-specific risks, compliance issues
- **ESG Factors**: Environmental, social, governance considerations

### Risk Management
- **Scenario Analysis**: Bull/base/bear cases with probability weighting
- **Position Sizing**: Risk-adjusted allocation recommendations (1-5% typical)
- **Stop-Loss Guidance**: Downside protection levels
- **Correlation Analysis**: Portfolio diversification considerations

## Data Sources

- **Financial Data**: SEC filings, earnings reports, company guidance
- **Market Data**: Real-time pricing, volume, technical indicators
- **Analyst Coverage**: Wall Street research, price target updates
- **News & Sentiment**: Financial media, regulatory announcements
- **Options Data**: Unusual activity, implied volatility, positioning
- **Insider Activity**: Form 4 filings, executive transactions

## Professional Disclaimers

### ⚠️ Important Legal Notice

This tool is designed for **educational and research purposes only**. All analysis and recommendations are:

- **Not financial advice** - For informational purposes only
- **Not personalized** - Does not consider individual circumstances
- **Historical data based** - Past performance doesn't guarantee future results
- **Requiring due diligence** - Users must conduct independent research
- **Risk warning included** - All investments carry risk of loss

### Risk Warnings
- Stock prices are volatile and unpredictable
- AI analysis may contain errors or biases
- Market conditions change rapidly
- Regulatory and company-specific risks may not be fully captured
- Position sizing recommendations are general guidelines only

### Professional Consultation
Always consult with qualified financial professionals before making investment decisions. This tool does not replace professional financial advice.

## Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md):

### Development Areas
- Enhanced data source integration
- Improved technical analysis algorithms
- Additional sector-specific metrics
- ESG scoring improvements
- Risk model enhancements

### Code Contributions
```bash
# Fork the repository
git fork https://github.com/quant-sentiment-ai/claude-equity-research

# Create feature branch
git checkout -b feature/your-enhancement

# Submit pull request with detailed description
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support & Community

- 📖 [Documentation](docs/)
- 🐛 [Report Issues](https://github.com/quant-sentiment-ai/claude-equity-research/issues)
- 💬 [Discussions](https://github.com/quant-sentiment-ai/claude-equity-research/discussions)
- 🔄 [Changelog](CHANGELOG.md)

## Acknowledgments

- Built for [Claude Code](https://claude.ai/code) - Anthropic's official CLI
- Inspired by institutional equity research standards
- Community-driven development and feedback

---

**Remember**: This tool provides educational insights only. Always conduct your own due diligence and consult qualified financial professionals before making investment decisions. Past performance does not guarantee future results.
