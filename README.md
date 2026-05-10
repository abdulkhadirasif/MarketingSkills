

A collection of AI agent skills focused on marketing tasks. Built for technical marketers and founders who want AI coding agents to help with conversion optimization, copywriting, SEO, analytics, and growth engineering. Works with Claude Code, OpenAI Codex, Cursor, Windsurf, and any agent that supports the [Agent Skills spec](https://agentskills.io).

Built by [Corey Haines](https://corey.co?ref=marketingskills). Need hands-on help? Check out [Conversion Factory](https://conversionfactory.co?ref=marketingskills) — Corey's agency for conversion optimization, landing pages, and growth strategy. Want to learn more about marketing? Subscribe to [Swipe Files](https://swipefiles.com?ref=marketingskills). Want an autonomous AI agent that uses these skills to be your CMO? Try [Magister](https://magistermarketing.com?ref=marketingskills).
This fork is maintained at [abdulkhadirasif/MarketingSkills](https://github.com/abdulkhadirasif/MarketingSkills) and is configured for GitHub Copilot in VS Code. Originally built by [Corey Haines](https://corey.co?ref=marketingskills). Need hands-on help? Check out [Conversion Factory](https://conversionfactory.co?ref=marketingskills) — Corey's agency for conversion optimization, landing pages, and growth strategy. Want to learn more about marketing? Subscribe to [Swipe Files](https://swipefiles.com?ref=marketingskills). Want an autonomous AI agent that uses these skills to be your CMO? Try [Magister](https://magistermarketing.com?ref=marketingskills).

New to the terminal and coding agents? Check out the companion guide [Coding for Marketers](https://codingformarketers.com?ref=marketingskills).

**Contributions welcome!** Found a way to improve a skill or have a new one to add? [Open a PR](#contributing).

Run into a problem or have a question? [Open an issue](https://github.com/coreyhaines31/marketingskills/issues) — we're happy to help.
Run into a problem or have a question? [Open an issue](https://github.com/abdulkhadirasif/MarketingSkills/issues).

## What are Skills?


```bash
mkdir -p .github/skills
cp -r path/to/marketingskills/.github/skills/* .github/skills/
cp -r path/to/MarketingSkills/.github/skills/* .github/skills/
```

For personal skills shared across projects, copy them to `~/.copilot/skills/`.
If you use the GitHub CLI skill commands, install skills for Copilot at project scope:

```bash
gh skill install coreyhaines31/marketingskills
gh skill install abdulkhadirasif/MarketingSkills

# Install one skill
gh skill install coreyhaines31/marketingskills page-cro
gh skill install abdulkhadirasif/MarketingSkills page-cro

# Check for updates
gh skill update

```bash
# Install all skills
npx skills add coreyhaines31/marketingskills
npx skills add abdulkhadirasif/MarketingSkills

# Install specific skills
npx skills add coreyhaines31/marketingskills --skill page-cro copywriting
npx skills add abdulkhadirasif/MarketingSkills --skill page-cro copywriting

# List available skills
npx skills add coreyhaines31/marketingskills --list
npx skills add abdulkhadirasif/MarketingSkills --list
```

### Option 4: Claude Code Plugin

```bash
# Add the marketplace
/plugin marketplace add coreyhaines31/marketingskills
/plugin marketplace add abdulkhadirasif/MarketingSkills

# Install all marketing skills
/plugin install marketing-skills
Add as a submodule for easy updates, then reference `.github/skills/` from the submodule:

```bash
git submodule add https://github.com/coreyhaines31/marketingskills.git .agents/marketingskills
git submodule add https://github.com/abdulkhadirasif/MarketingSkills.git .agents/marketingskills
```

### Option 6: Fork and Customize

```bash
# Install all skills
npx skillkit install coreyhaines31/marketingskills
npx skillkit install abdulkhadirasif/MarketingSkills

# Install specific skills
npx skillkit install coreyhaines31/marketingskills --skill page-cro copywriting
npx skillkit install abdulkhadirasif/MarketingSkills --skill page-cro copywriting

# List available skills
npx skillkit install coreyhaines31/marketingskills --list
npx skillkit install abdulkhadirasif/MarketingSkills --list
```

## Upgrading from v1.0