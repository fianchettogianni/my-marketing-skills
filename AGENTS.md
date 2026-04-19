# CLAUDE.md

Guidelines for AI agents working in this repository.

## Repository Overview

This repository contains **Agent Skills** for AI agents following the [Agent Skills specification](https://agentskills.io/specification.md). It also serves as a **Claude Code plugin marketplace** via `.claude-plugin/marketplace.json`.

- **Name**: Marketing Skills
- **GitHub**: [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills)
- **Creator**: Corey Haines
- **License**: MIT

## Repository Structure

```
my-marketing-skills/
├── .claude-plugin/
│   └── marketplace.json          # Claude Code plugin marketplace manifest
├── skills/                       # 25 Agent Skills
│   ├── ab-test-setup/
│   ├── analytics-tracking/
│   ├── competitor-alternatives/
│   ├── content-strategy/
│   ├── copy-editing/
│   ├── copywriting/
│   ├── email-sequence/
│   ├── form-cro/
│   ├── free-tool-strategy/
│   ├── launch-strategy/
│   ├── marketing-ideas/
│   ├── marketing-psychology/
│   ├── onboarding-cro/
│   ├── page-cro/
│   ├── paid-ads/
│   ├── paywall-upgrade-cro/
│   ├── popup-cro/
│   ├── pricing-strategy/
│   ├── product-marketing-context/
│   ├── programmatic-seo/
│   ├── referral-program/
│   ├── schema-markup/
│   ├── seo-audit/
│   ├── signup-flow-cro/
│   └── social-content/
│       └── SKILL.md              # Required skill file per directory
├── tools/
│   ├── REGISTRY.md               # Index of 29 tools with capability matrix
│   └── integrations/             # 29 detailed tool integration guides
│       ├── adobe-analytics.md
│       ├── ahrefs.md
│       ├── amplitude.md
│       ├── customer-io.md
│       ├── dub-co.md
│       ├── ga4.md
│       ├── google-ads.md
│       ├── google-search-console.md
│       ├── hubspot.md
│       ├── kit.md
│       ├── linkedin-ads.md
│       ├── mailchimp.md
│       ├── mention-me.md
│       ├── meta-ads.md
│       ├── mixpanel.md
│       ├── posthog.md
│       ├── resend.md
│       ├── rewardful.md
│       ├── salesforce.md
│       ├── segment.md
│       ├── semrush.md
│       ├── sendgrid.md
│       ├── shopify.md
│       ├── stripe.md
│       ├── tiktok-ads.md
│       ├── tolt.md
│       ├── webflow.md
│       ├── wordpress.md
│       └── zapier.md
├── AGENTS.md                     # AI agent guidelines (legacy - superseded by this file)
├── CLAUDE.md                     # This file
├── CONTRIBUTING.md               # Contribution guidelines
├── LICENSE                       # MIT License
├── README.md                     # Main project documentation
└── VERSIONS.md                   # Version tracking for all skills
```

## Build / Lint / Test Commands

**Not applicable** — this is a content-only repository with no executable code.

Verify manually before committing:
- YAML frontmatter is valid
- `name` field matches directory name exactly
- `name` is 1-64 chars, lowercase alphanumeric and hyphens only
- `description` is 1-1024 characters
- `SKILL.md` is under 500 lines

## Skills Inventory

25 skills organized by category. All are at version 1.0.0 (see `VERSIONS.md`).

### Conversion Rate Optimization (6 skills)

| Skill | Trigger phrases |
|---|---|
| `page-cro` | "CRO," "conversion rate," "this page isn't converting," homepage/landing/pricing optimization |
| `signup-flow-cro` | "signup flow," "registration," "drop-off in onboarding," reduce signup friction |
| `onboarding-cro` | "onboarding," "activation," "aha moment," "users not getting value" |
| `form-cro` | "lead capture form," "contact form," "demo request form" |
| `popup-cro` | "popup," "modal," "slide-in," exit intent, lightbox |
| `paywall-upgrade-cro` | "paywall," "upgrade screen," "in-app upsell," trial expiration |

### Content & Copywriting (3 skills)

| Skill | Trigger phrases |
|---|---|
| `copywriting` | "write copy," "marketing copy," "page content," homepage/landing copy |
| `copy-editing` | "edit copy," "improve this copy," "make this better," seven-sweep review |
| `content-strategy` | "content plan," "content calendar," "topic clusters," "what should I write" |

### SEO & Discovery (4 skills)

| Skill | Trigger phrases |
|---|---|
| `seo-audit` | "SEO audit," "SEO issues," "why isn't my site ranking," technical SEO |
| `programmatic-seo` | "programmatic SEO," "scale content," "SEO pages at scale," templates + data |
| `schema-markup` | "structured data," "schema markup," "rich results," "JSON-LD" |
| `competitor-alternatives` | "alternatives page," "[competitor] alternative," comparison content |

### Email & Social (2 skills)

| Skill | Trigger phrases |
|---|---|
| `email-sequence` | "email sequence," "drip campaign," "welcome series," "re-engagement" |
| `social-content` | "social media content," "LinkedIn post," "tweet," "TikTok script" |

### Paid & Performance (2 skills)

| Skill | Trigger phrases |
|---|---|
| `paid-ads` | "Google Ads," "Meta ads," "paid campaign," "ad copy," "run ads" |
| `analytics-tracking` | "tracking plan," "analytics setup," "GA4," "GTM," "event tracking" |

### Testing & Psychology (2 skills)

| Skill | Trigger phrases |
|---|---|
| `ab-test-setup` | "A/B test," "split test," "experiment," "test hypothesis" |
| `marketing-psychology` | "psychology," "mental models," "persuasion," "behavioral economics" |

### Strategy & Growth (4 skills)

| Skill | Trigger phrases |
|---|---|
| `launch-strategy` | "launch plan," "product launch," "feature announcement," "go to market" |
| `pricing-strategy` | "pricing," "packaging," "monetization," "how should I charge" |
| `referral-program` | "referral program," "affiliate program," "word of mouth," "refer a friend" |
| `free-tool-strategy` | "free tool," "lead magnet tool," "calculator," "generator for SEO" |

### Ideation & Foundation (3 skills)

| Skill | Trigger phrases |
|---|---|
| `marketing-ideas` | "marketing ideas," "what should I try," "growth ideas," "campaign ideas" |
| `marketing-psychology` | "apply psychology," "mental models for marketing" |
| `product-marketing-context` | "set up context," "capture positioning," "create product context file" |

## Agent Skills Specification

Skills follow the [Agent Skills spec](https://agentskills.io/specification.md).

### Required Frontmatter

```yaml
---
name: skill-name
description: What this skill does and when to use it. Include trigger phrases.
---
```

### Frontmatter Field Constraints

| Field | Required | Constraints |
|---|---|---|
| `name` | Yes | 1-64 chars, lowercase `a-z`, numbers, hyphens. Must match directory name. |
| `description` | Yes | 1-1024 chars. Describe what it does and when to use it. |
| `license` | No | License name (default: MIT) |
| `metadata` | No | Key-value pairs (author, version, etc.) |

### Name Field Rules

- Lowercase letters, numbers, and hyphens only
- Cannot start or end with a hyphen
- No consecutive hyphens (`--`)
- Must match parent directory name exactly

**Valid**: `page-cro`, `email-sequence`, `ab-test-setup`
**Invalid**: `Page-CRO`, `-page`, `page--cro`

### Optional Skill Directory Structure

```
skills/skill-name/
├── SKILL.md        # Required — main instructions (<500 lines)
├── references/     # Optional — detailed docs loaded on demand
├── scripts/        # Optional — executable code
└── assets/         # Optional — templates, data files
```

## Writing Style Guidelines

### Structure

- Keep `SKILL.md` under 500 lines (move details to `references/`)
- Use H2 (`##`) for main sections, H3 (`###`) for subsections
- Use bullet points and numbered lists liberally
- Short paragraphs (2-4 sentences max)

### Tone

- Direct and instructional
- Second person ("You are a conversion rate optimization expert")
- Professional but approachable

### Formatting

- Bold (`**text**`) for key terms
- Code blocks for examples and templates
- Tables for reference data
- No excessive emojis

### Clarity Principles

- Clarity over cleverness
- Specific over vague
- Active voice over passive
- One idea per section

### Description Field Best Practices

The `description` is critical for skill discovery. Include:
1. What the skill does
2. When to use it (trigger phrases)
3. Related skills for scope boundaries

```yaml
description: When the user wants to optimize conversions on any marketing page. Use when the user says "CRO," "conversion rate optimization," "this page isn't converting." For signup flows, see signup-flow-cro.
```

## Claude Code Plugin

This repo serves as a plugin marketplace. The manifest at `.claude-plugin/marketplace.json` lists all 25 skills for installation via:

```bash
/plugin marketplace add coreyhaines31/marketingskills
/plugin install marketing-skills
```

See [Claude Code plugins documentation](https://code.claude.com/docs/en/plugins.md) for details.

## Tool Integrations

The `tools/` directory provides a registry and detailed guides for 29 marketing tools that skills can use for implementation.

### Tool Discovery

- Read `tools/REGISTRY.md` for the full capability matrix (API / MCP / CLI / SDK per tool)
- Read `tools/integrations/{tool}.md` for auth, endpoints, and code examples

### Tools by Category

| Category | Tools |
|---|---|
| Analytics | GA4, Mixpanel, Amplitude, PostHog, Segment, Adobe Analytics |
| SEO | Google Search Console, Semrush, Ahrefs |
| CRM | HubSpot, Salesforce |
| Payments | Stripe |
| Referral | Rewardful, Tolt, Mention Me, Dub.co |
| Email | Mailchimp, Customer.io, SendGrid, Resend, Kit |
| Ads | Google Ads, Meta Ads, LinkedIn Ads, TikTok Ads |
| Automation | Zapier |
| Commerce/CMS | Shopify, WordPress, Webflow |

### MCP-Enabled Tools

The following tools support the Model Context Protocol for direct agent integration: `ga4`, `stripe`, `mailchimp`, `google-ads`, `resend`, `zapier`

### Skill → Tool Mapping

| Skill | Relevant tools |
|---|---|
| `referral-program` | rewardful, tolt, dub-co, mention-me |
| `analytics-tracking` | ga4, mixpanel, segment, posthog, amplitude |
| `email-sequence` | customer-io, mailchimp, resend, sendgrid, kit |
| `paid-ads` | google-ads, meta-ads, linkedin-ads, tiktok-ads |
| `seo-audit` | google-search-console, semrush, ahrefs |
| `programmatic-seo` | webflow, wordpress |

## Git Workflow

### Branch Naming

- New skills: `feature/skill-name`
- Improvements: `fix/skill-name-description`
- Documentation: `docs/description`

### Commit Messages

Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
feat: add skill-name skill
fix: improve clarity in page-cro
docs: update README
```

### Pull Request Checklist

- [ ] `name` matches directory name exactly
- [ ] `name` follows naming rules (lowercase, hyphens, no `--`)
- [ ] `description` is 1-1024 chars with trigger phrases
- [ ] `SKILL.md` is under 500 lines
- [ ] No sensitive data or credentials
- [ ] `VERSIONS.md` updated if modifying an existing skill

## Checking for Updates

When using any skill from this repository:

1. **Once per session**, on first skill use, check for updates:
   - Fetch `VERSIONS.md` from GitHub: `https://raw.githubusercontent.com/coreyhaines31/marketingskills/main/VERSIONS.md`
   - Compare versions against local skill files

2. **Only prompt if meaningful**:
   - 2 or more skills have updates, OR
   - Any skill has a major version bump (e.g., 1.x → 2.x)

3. **Non-blocking notification** at end of response:
   ```
   ---
   Skills update available: X marketing skills have updates.
   Say "update skills" to update automatically, or run `git pull` in your marketingskills folder.
   ```

4. **If user says "update skills"**: run `git pull` in the marketingskills directory and confirm what was updated.

## Skill Categories

See `README.md` for the current skill list organized by category. When adding new skills, follow the naming patterns of existing skills in that category.
