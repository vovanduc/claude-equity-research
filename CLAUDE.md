# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Claude Equity Research is a Claude Code plugin that provides institutional-grade equity research analysis through the `/trading-ideas` slash command. The project is command-based (no executable code) and leverages Claude's WebSearch and WebFetch capabilities to generate professional investment analysis reports.

## Core Architecture

### Plugin System Structure
- **Plugin Definition**: `.claude-plugin/marketplace.json` defines the plugin marketplace metadata and plugin registration
- **Command Implementation**: `commands/trading-ideas.md` contains the prompt template that drives the equity analysis
- **Documentation**: Extensive docs in `README.md`, `PLUGIN.md`, `docs/methodology.md`, and `docs/customization.md`

### Key Design Principles
1. **Zero-configuration**: No API keys, environment variables, or dependencies required
2. **Command-driven**: Implemented as Claude Code slash command (not standalone code)
3. **Educational focus**: All outputs include disclaimers emphasizing educational/research purposes only
4. **Institutional standards**: Follows Wall Street research report formatting and terminology

## Important Plugin Configuration Requirements

### marketplace.json Schema
When modifying `.claude-plugin/marketplace.json`:
- **Critical**: The `pluginRoot` field must be set to `"commands"` (NOT `".claude-plugin/commands"`)
- **Plugin source paths**: Must start with `./` prefix (e.g., `"./commands/trading-ideas.md"`)
- **Required fields**: name, owner (with email), metadata (description, version, pluginRoot), plugins array

Example structure:
```json
{
  "name": "claude-equity-research-marketplace",
  "owner": { "name": "...", "email": "..." },
  "metadata": { "pluginRoot": "commands" },
  "plugins": [{ "source": "./commands/trading-ideas.md", ... }]
}
```

### Command File Structure
Commands in `commands/` directory must:
- Include YAML frontmatter with `description`, `argument-hint`, and `allowed-tools`
- Define comprehensive prompts that Claude can execute autonomously
- Specify output formatting requirements with exact templates
- Include quality standards and validation criteria

## Development Workflow

### Testing the Plugin Locally
```bash
# Install the plugin from local repository
/plugin marketplace add <path-to-this-repo>
/plugin install claude-equity-research@<marketplace-name>

# Test the command
/trading-ideas AAPL

# Uninstall for cleanup
/plugin uninstall claude-equity-research@<marketplace-name>
```

### Making Changes to Commands
1. Edit `commands/trading-ideas.md` to modify analysis framework
2. Test changes by reinstalling the plugin locally
3. Verify output quality matches institutional research standards
4. Ensure all 8 sections render correctly with proper markdown formatting

### Documentation Updates
- **README.md**: User-facing installation and usage instructions
- **PLUGIN.md**: Plugin-specific documentation for end users
- **docs/methodology.md**: Detailed analytical framework documentation
- **SECURITY.md**: Security policy and vulnerability reporting

## Command Analysis Framework

The `/trading-ideas` command follows this structure:

1. **Research Phase**: Parallel WebSearch calls for financial performance, market positioning, and advanced intelligence
2. **Analysis Generation**: 8-section report with specific formatting requirements
3. **Output Sections**:
   - Executive Summary (BUY/SELL/HOLD with price target)
   - Fundamental Analysis (revenue, margins, peer comparison)
   - Catalyst Analysis (near-term and medium-term drivers)
   - Valuation & Price Targets (bull/base/bear scenarios with probability weighting)
   - Risk Assessment (company-specific and macro risks, position sizing)
   - Technical Context & Options Intelligence
   - Market Positioning (sector performance, relative strength)
   - Insider Signals (insider activity, institutional ownership)

## Quality Standards

All analysis must include:
- Specific financial metrics with numbers and percentages
- Timeframes for all data points (YoY, QoQ, etc.)
- Analyst firm names and price targets when available
- Institutional terminology (EBITDA, P/E, EV/Sales, etc.)
- Probability weightings for scenarios (bull/base/bear)
- Position sizing recommendations (typically 1-5% of portfolio)
- Comprehensive legal disclaimers

## File Organization

```
claude-equity-research/
├── .claude-plugin/
│   └── marketplace.json          # Plugin marketplace definition
├── commands/
│   ├── trading-ideas.md          # Main analysis command (core prompt)
│   └── README.md                 # Command documentation
├── config/
│   └── config.example.json       # Template configuration
├── docs/
│   ├── methodology.md            # Analytical framework details
│   ├── installation.md           # Setup instructions
│   └── customization.md          # Customization guide
├── examples/
│   └── sample_reports/           # Example analyses for reference
├── README.md                     # Main user documentation
├── PLUGIN.md                     # Plugin system documentation
└── SECURITY.md                   # Security policy
```

## Important Constraints

### Legal and Compliance
- All outputs MUST include disclaimer: "for educational and research purposes only"
- Never claim to provide personalized financial advice
- Include risk warnings about AI-generated analysis limitations
- Recommend users consult qualified financial professionals

### Data Handling
- Use only public data sources (SEC filings, financial media, analyst reports)
- Never request or store API keys or user credentials
- All data fetching happens via Claude's WebSearch/WebFetch tools
- No persistent storage or caching of financial data

### Output Quality
- Prefer specific numbers over generalities (e.g., "Revenue grew 23% YoY" not "strong growth")
- Always include upside/downside calculations for price targets
- Provide conviction levels (High/Medium/Low) for recommendations
- Include both bullish and bearish scenarios with probability weights

## Common Modifications

### Adding New Analysis Sections
1. Edit `commands/trading-ideas.md` to add new section template
2. Update `docs/methodology.md` to document the new analytical approach
3. Test with multiple tickers to ensure data availability
4. Update PLUGIN.md usage examples if section adds significant value

### Adjusting Tone or Formatting
- Modify the prompt in `commands/trading-ideas.md`
- Ensure changes maintain institutional research standards
- Test output rendering in Claude Code terminal (markdown formatting)
- Verify table formatting displays correctly

### Supporting Additional Asset Classes
Currently focused on US equities (NYSE, NASDAQ). To expand:
- Research data availability for new asset class
- Adapt valuation frameworks in methodology
- Update command frontmatter and descriptions
- Add asset-class-specific quality standards

## Repository Standards

- **Licensing**: MIT License (see LICENSE file)
- **Contact**: quant.sentiment.ai@gmail.com for security issues
- **Versioning**: Update version in marketplace.json for breaking changes
- **Git workflow**: Main branch for stable releases, feature branches for development

## Key Differentiators

This is a **command-based plugin**, not a traditional codebase:
- No build process, dependencies, or runtime environment
- No test suite (validation happens through output quality review)
- No package.json, requirements.txt, or similar dependency files
- Changes are prompt engineering, not code changes
- "Development" means refining analytical frameworks and output templates
