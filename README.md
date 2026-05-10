# Marketing Skills for AI Agents

A collection of AI agent skills focused on marketing tasks. Built for technical marketers and founders who want AI coding agents to help with conversion optimization, copywriting, SEO, analytics, and growth engineering. Works with Claude Code, OpenAI Codex, Cursor, Windsurf, and any agent that supports the [Agent Skills spec](https://agentskills.io).

Built by [Corey Haines](https://corey.co?ref=marketingskills). Need hands-on help? Check out [Conversion Factory](https://conversionfactory.co?ref=marketingskills) — Corey's agency for conversion optimization, landing pages, and growth strategy. Want to learn more about marketing? Subscribe to [Swipe Files](https://swipefiles.com?ref=marketingskills). Want an autonomous AI agent that uses these skills to be your CMO? Try [Magister](https://magistermarketing.com?ref=marketingskills).

New to the terminal and coding agents? Check out the companion guide [Coding for Marketers](https://codingformarketers.com?ref=marketingskills).

**Contributions welcome!** Found a way to improve a skill or have a new one to add? [Open a PR](#contributing).

Run into a problem or have a question? [Open an issue](https://github.com/coreyhaines31/marketingskills/issues) — we're happy to help.

## What are Skills?

Skills are markdown files that give AI agents specialized knowledge and workflows for specific tasks. When you add these to your project, your agent can recognize when you're working on a marketing task and apply the right frameworks and best practices.

## How Skills Work Together

Skills reference each other and build on shared context. The `product-marketing-context` skill is the foundation — every other skill checks it first to understand your product, audience, and positioning before doing anything.

```
                            ┌──────────────────────────────────────┐
                            │      product-marketing-context       │
                            │    (read by all other skills first)  │
                            └──────────────────┬───────────────────┘
                                               │
    ┌──────────────┬─────────────┬─────────────┼─────────────┬──────────────┬──────────────┐
    ▼              ▼             ▼             ▼             ▼              ▼              ▼
┌──────────┐ ┌──────────┐ ┌──────────┐ ┌────────────┐ ┌──────────┐ ┌─────────────┐ ┌───────────┐
│  SEO &   │ │   CRO    │ │Content & │ │  Paid &    │ │ Growth & │ │  Sales &    │ │ Strategy  │
│ Content  │ │          │ │   Copy   │ │Measurement │ │Retention │ │    GTM      │ │           │
├──────────┤ ├──────────┤ ├──────────┤ ├────────────┤ ├──────────┤ ├─────────────┤ ├───────────┤
│seo-audit │ │page-cro  │ │copywritng│ │paid-ads    │ │referral  │ │revops       │ │mktg-ideas │
│ai-seo    │ │signup-cro│ │copy-edit │ │ad-creative │ │free-tool │ │sales-enable │ │mktg-psych │
│site-arch │ │onboard   │ │cold-email│ │ab-test     │ │churn-    │ │launch       │ │customer-  │
│programm  │ │form-cro  │ │email-seq │ │analytics   │ │ prevent  │ │pricing      │ │ research  │
│schema    │ │popup-cro │ │social    │ │            │ │community │ │comp-alts    │ │           │
│content   │ │paywall   │ │video     │ │            │ │lead-magnt│ │comp-profile │ │           │
│aso-audit │ │          │ │image     │ │            │ │co-mktg   │ │directory    │ │           │
└────┬─────┘ └────┬─────┘ └────┬─────┘ └─────┬──────┘ └────┬─────┘ └──────┬──────┘ └─────┬─────┘
     │            │            │              │             │              │              │
     └────────────┴─────┬──────┴──────────────┴─────────────┴──────────────┴──────────────┘
                        │
         Skills cross-reference each other:
           copywriting ↔ page-cro ↔ ab-test-setup
           revops ↔ sales-enablement ↔ cold-email
           seo-audit ↔ schema-markup ↔ ai-seo
           customer-research → copywriting, page-cro, competitor-alternatives
```

See each skill's **Related Skills** section for the full dependency map.

## Available Skills

<!-- SKILLS:START -->
| Skill | Description |
|-------|-------------|
| [ab-test-setup](.github/skills/ab-test-setup/) | When the user wants to plan, design, or implement an A/B test or experiment, or build a growth experimentation program.... |
| [ad-creative](.github/skills/ad-creative/) | When the user wants to generate, iterate, or scale ad creative — headlines, descriptions, primary text, or full ad... |
| [ai-seo](.github/skills/ai-seo/) | When the user wants to optimize content for AI search engines, get cited by LLMs, or appear in AI-generated answers.... |
| [analytics-tracking](.github/skills/analytics-tracking/) | When the user wants to set up, improve, or audit analytics tracking and measurement. Also use when the user mentions... |
| [aso-audit](.github/skills/aso-audit/) | When the user wants to audit or optimize an App Store or Google Play listing. Also use when the user mentions 'ASO... |
| [churn-prevention](.github/skills/churn-prevention/) | When the user wants to reduce churn, build cancellation flows, set up save offers, recover failed payments, or... |
| [co-marketing](.github/skills/co-marketing/) | When the user wants to find co-marketing partners, plan joint campaigns, or brainstorm partnership opportunities. Use... |
| [cold-email](.github/skills/cold-email/) | Write B2B cold emails and follow-up sequences that get replies. Use when the user wants to write cold outreach emails,... |
| [community-marketing](.github/skills/community-marketing/) | Build and leverage online communities to drive product growth and brand loyalty. Use when the user wants to create a... |
| [competitor-alternatives](.github/skills/competitor-alternatives/) | When the user wants to create competitor comparison or alternative pages for SEO and sales enablement. Also use when... |
| [competitor-profiling](.github/skills/competitor-profiling/) | When the user wants to research, profile, or analyze competitors from their URLs. Also use when the user mentions... |
| [content-strategy](.github/skills/content-strategy/) | When the user wants to plan a content strategy, decide what content to create, or figure out what topics to cover. Also... |
| [copy-editing](.github/skills/copy-editing/) | When the user wants to edit, review, or improve existing marketing copy, or refresh outdated content. Also use when the... |
| [copywriting](.github/skills/copywriting/) | When the user wants to write, rewrite, or improve marketing copy for any page — including homepage, landing pages,... |
| [customer-research](.github/skills/customer-research/) | When the user wants to conduct, analyze, or synthesize customer research. Use when the user mentions "customer... |
| [directory-submissions](.github/skills/directory-submissions/) | When the user wants to submit their product to startup, SaaS, AI, agent, MCP, no-code, or review directories for... |
| [email-sequence](.github/skills/email-sequence/) | When the user wants to create or optimize an email sequence, drip campaign, automated email flow, or lifecycle email... |
| [form-cro](.github/skills/form-cro/) | When the user wants to optimize any form that is NOT signup/registration — including lead capture forms, contact forms,... |
| [free-tool-strategy](.github/skills/free-tool-strategy/) | When the user wants to plan, evaluate, or build a free tool for marketing purposes — lead generation, SEO value, or... |
| [image](.github/skills/image/) | When the user wants to create, generate, edit, or optimize images for marketing — blog heroes, social graphics, product... |
| [launch-strategy](.github/skills/launch-strategy/) | When the user wants to plan a product launch, feature announcement, or release strategy. Also use when the user... |
| [lead-magnets](.github/skills/lead-magnets/) | When the user wants to create, plan, or optimize a lead magnet for email capture or lead generation. Also use when the... |
| [marketing-ideas](.github/skills/marketing-ideas/) | When the user needs marketing ideas, inspiration, or strategies for their SaaS or software product. Also use when the... |
| [marketing-psychology](.github/skills/marketing-psychology/) | When the user wants to apply psychological principles, mental models, or behavioral science to marketing. Also use when... |
| [onboarding-cro](.github/skills/onboarding-cro/) | When the user wants to optimize post-signup onboarding, user activation, first-run experience, or time-to-value. Also... |
| [page-cro](.github/skills/page-cro/) | When the user wants to optimize, improve, or increase conversions on any marketing page — including homepage, landing... |
| [paid-ads](.github/skills/paid-ads/) | When the user wants help with paid advertising campaigns on Google Ads, Meta (Facebook/Instagram), LinkedIn, Twitter/X,... |
| [paywall-upgrade-cro](.github/skills/paywall-upgrade-cro/) | When the user wants to create or optimize in-app paywalls, upgrade screens, upsell modals, or feature gates. Also use... |
| [popup-cro](.github/skills/popup-cro/) | When the user wants to create or optimize popups, modals, overlays, slide-ins, or banners for conversion purposes. Also... |
| [pricing-strategy](.github/skills/pricing-strategy/) | When the user wants help with pricing decisions, packaging, or monetization strategy. Also use when the user mentions... |
| [product-marketing-context](.github/skills/product-marketing-context/) | When the user wants to create or update their product marketing context document. Also use when the user mentions... |
| [programmatic-seo](.github/skills/programmatic-seo/) | When the user wants to create SEO-driven pages at scale using templates and data. Also use when the user mentions... |
| [referral-program](.github/skills/referral-program/) | When the user wants to create, optimize, or analyze a referral program, affiliate program, or word-of-mouth strategy.... |
| [revops](.github/skills/revops/) | When the user wants help with revenue operations, lead lifecycle management, or marketing-to-sales handoff processes.... |
| [sales-enablement](.github/skills/sales-enablement/) | When the user wants to create sales collateral, pitch decks, one-pagers, objection handling docs, or demo scripts. Also... |
| [schema-markup](.github/skills/schema-markup/) | When the user wants to add, fix, or optimize schema markup and structured data on their site. Also use when the user... |
| [seo-audit](.github/skills/seo-audit/) | When the user wants to audit, review, or diagnose SEO issues on their site. Also use when the user mentions "SEO... |
| [signup-flow-cro](.github/skills/signup-flow-cro/) | When the user wants to optimize signup, registration, account creation, or trial activation flows. Also use when the... |
| [site-architecture](.github/skills/site-architecture/) | When the user wants to plan, map, or restructure their website's page hierarchy, navigation, URL structure, or internal... |
| [social-content](.github/skills/social-content/) | When the user wants help creating, scheduling, or optimizing social media content for LinkedIn, Twitter/X, Instagram,... |
| [video](.github/skills/video/) | When the user wants to create, generate, or produce video content using AI tools or programmatic frameworks. Also use... |
<!-- SKILLS:END -->

## Installation

### Option 1: GitHub Copilot in VS Code (Recommended)

This repository is configured for Copilot project skills. Open this repo in VS Code and Copilot agent mode can discover skills from `.github/skills/`. Repository-wide Copilot guidance lives in `.github/copilot-instructions.md`.

To use these skills in another project, copy the skill folders into that project's `.github/skills/` directory:

```bash
mkdir -p .github/skills
cp -r path/to/marketingskills/.github/skills/* .github/skills/
```

For personal skills shared across projects, copy them to `~/.copilot/skills/`.

### Option 2: GitHub CLI Skill Install

If you use the GitHub CLI skill commands, install skills for Copilot at project scope:

```bash
gh skill install coreyhaines31/marketingskills

# Install one skill
gh skill install coreyhaines31/marketingskills page-cro

# Check for updates
gh skill update
```

### Option 3: Multi-Agent CLI Install

Use [npx skills](https://github.com/vercel-labs/skills) to install skills into `.agents/skills/` for agents that support the cross-agent location:

```bash
# Install all skills
npx skills add coreyhaines31/marketingskills

# Install specific skills
npx skills add coreyhaines31/marketingskills --skill page-cro copywriting

# List available skills
npx skills add coreyhaines31/marketingskills --list
```

### Option 4: Claude Code Plugin

Install via Claude Code's built-in plugin system:

```bash
# Add the marketplace
/plugin marketplace add coreyhaines31/marketingskills

# Install all marketing skills
/plugin install marketing-skills
```

### Option 5: Git Submodule

Add as a submodule for easy updates, then reference `.github/skills/` from the submodule:

```bash
git submodule add https://github.com/coreyhaines31/marketingskills.git .agents/marketingskills
```

### Option 6: Fork and Customize

1. Fork this repository
2. Customize skills for your specific needs
3. Clone your fork into your projects

### Option 7: SkillKit (Multi-Agent)

Use [SkillKit](https://github.com/rohitg00/skillkit) to install skills across multiple AI agents (Claude Code, Cursor, Copilot, etc.):

```bash
# Install all skills
npx skillkit install coreyhaines31/marketingskills

# Install specific skills
npx skillkit install coreyhaines31/marketingskills --skill page-cro copywriting

# List available skills
npx skillkit install coreyhaines31/marketingskills --list
```

## Upgrading from v1.0

Skills now use `.agents/` instead of `.claude/` for the product marketing context file. Move your existing context file:

```bash
mkdir -p .agents
mv .claude/product-marketing-context.md .agents/product-marketing-context.md
```

Skills will still check `.claude/` as a fallback, so nothing breaks if you don't.

## Usage

Once installed, just ask your agent to help with marketing tasks:

```
"Help me optimize this landing page for conversions"
→ Uses page-cro skill

"Write homepage copy for my SaaS"
→ Uses copywriting skill

"Set up GA4 tracking for signups"
→ Uses analytics-tracking skill

"Create a 5-email welcome sequence"
→ Uses email-sequence skill
```

You can also invoke skills directly:

```
/page-cro
/email-sequence
/seo-audit
```

## Skill Categories

### Conversion Optimization
- `page-cro` - Any marketing page
- `signup-flow-cro` - Registration flows
- `onboarding-cro` - Post-signup activation
- `form-cro` - Lead capture forms
- `popup-cro` - Modals and overlays
- `paywall-upgrade-cro` - In-app upgrade moments

### Content & Copy
- `copywriting` - Marketing page copy
- `copy-editing` - Edit and polish existing copy
- `cold-email` - B2B cold outreach emails and sequences
- `email-sequence` - Automated email flows
- `social-content` - Social media content
- `image` - AI image generation, design tools, and optimization

### SEO & Discovery
- `seo-audit` - Technical and on-page SEO
- `ai-seo` - AI search optimization (AEO, GEO, LLMO)
- `programmatic-seo` - Scaled page generation
- `site-architecture` - Page hierarchy, navigation, URL structure
- `competitor-alternatives` - Comparison and alternative pages
- `schema-markup` - Structured data

### Paid & Distribution
- `paid-ads` - Google, Meta, LinkedIn ad campaigns
- `ad-creative` - Bulk ad creative generation and iteration
- `social-content` - Social media scheduling and strategy

### Measurement & Testing
- `analytics-tracking` - Event tracking setup
- `ab-test-setup` - Experiment design

### Retention
- `churn-prevention` - Cancel flows, save offers, dunning, payment recovery

### Growth Engineering
- `co-marketing` - Partner identification and joint campaigns
- `free-tool-strategy` - Marketing tools and calculators
- `referral-program` - Referral and affiliate programs

### Strategy & Monetization
- `marketing-ideas` - 140 SaaS marketing ideas
- `marketing-psychology` - Mental models and psychology
- `launch-strategy` - Product launches and announcements
- `pricing-strategy` - Pricing, packaging, and monetization

### Sales & RevOps
- `revops` - Lead lifecycle, scoring, routing, pipeline management
- `sales-enablement` - Sales decks, one-pagers, objection docs, demo scripts

## Contributing

Found a way to improve a skill? Have a new skill to suggest? PRs and issues welcome!

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on adding or improving skills.

## License

[MIT](LICENSE) - Use these however you want.
