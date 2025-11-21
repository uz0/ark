---
title: Article Fact-Checking Guide
description: Self-checks and argument validation for wiki articles
published: true
date: 2025-10-28T11:59:42.752Z
tags: [fact-checking, validation, quality]
editor: markdown
---

# Article Fact-Checking and Self-Validation

## The Fact-Checking Process

Every article must go through rigorous self-validation before publication.

### 1. Source Verification

**For each factual claim:**

```
1. Identify the claim
2. Find authoritative source
3. Verify source credibility
4. Check publication date
5. Add inline citation
6. Record in Fact Check section
```

### 2. Source Authority Hierarchy

**Tier 1 (Most Reliable):**
- Peer-reviewed research papers
- Official documentation
- Government/academic institutions
- Primary sources

**Tier 2 (Reliable with Verification):**
- Reputable tech blogs (with author credentials)
- Well-known industry publications
- Conference proceedings
- Technical books

**Tier 3 (Use Sparingly):**
- Blog posts (require multiple sources)
- Forum discussions (for community consensus only)
- Social media (expert accounts only)

**Avoid:**
- Anonymous sources
- Unverified claims
- Outdated information (>2 years old without re-verification)

### 3. Link Validation

**Check every link:**

```bash
# Use link checker tool
npx broken-link-checker https://wiki.example.com/article

# Or manual checks:
- Click each link
- Verify destination is correct
- Check for 404 errors
- Ensure HTTPS where possible
```

### 4. Date Currency

**Verification dates must be:**
- Within 6 months for technical content
- Within 1 year for conceptual content
- Current for time-sensitive information

**When to re-verify:**
- API/tool version changes
- Security vulnerabilities discovered
- Official recommendations change
- Reader reports outdated info

## Self-Check Checklist

### Before Publishing

- [ ] **Sources**: Every claim has authoritative source
- [ ] **Links**: All URLs tested and working
- [ ] **Dates**: Verification dates are current
- [ ] **Context**: Why each fact matters is clear
- [ ] **Accuracy**: Technical details are correct
- [ ] **Completeness**: No missing steps or information
- [ ] **Clarity**: Non-experts can understand
- [ ] **Examples**: Code/commands are tested
- [ ] **Screenshots**: Images are clear and annotated
- [ ] **Fact Check Section**: Complete and accurate

### Content Quality

- [ ] **Grammar**: No spelling or grammar errors
- [ ] **Consistency**: Terminology used consistently
- [ ] **Structure**: Logical flow and organization
- [ ] **Formatting**: Proper Markdown formatting
- [ ] **Navigation**: Links to related articles
- [ ] **Searchability**: Appropriate tags
- [ ] **Accessibility**: Alt text for images

### Technical Accuracy

- [ ] **Commands**: All commands tested
- [ ] **Code**: All code examples work
- [ ] **Versions**: Software versions specified
- [ ] **Prerequisites**: All requirements listed
- [ ] **Troubleshooting**: Common issues addressed
- [ ] **Warnings**: Potential pitfalls noted

## Common Fact-Checking Patterns

### Pattern 1: Installation Instructions

```markdown
## Installation

```bash
npm install -g @dcversus/prp
```

**Source:** [npm - @dcversus/prp](https://www.npmjs.com/package/@dcversus/prp)
**Version:** 0.2.0
**Verified:** 2025-10-28

**Prerequisites:**
- Node.js ≥20.0.0 **Source:** [package.json#L60](https://github.com/dcversus/prp/blob/main/package.json#L60)
- npm ≥10.0.0 **Source:** [package.json#L61](https://github.com/dcversus/prp/blob/main/package.json#L61)
```

### Pattern 2: Configuration Options

```markdown
## Configuration

`--template` option accepts:
- `react` - React with Vite
- `typescript-lib` - TypeScript library
- `fastapi` - FastAPI Python
- `wikijs` - Wiki.js documentation

**Source:** [src/types.ts#L30-39](https://github.com/dcversus/prp/blob/main/src/types.ts#L30-39)
**Verified:** 2025-10-28
```

### Pattern 3: Feature Claims

```markdown
## Features

PRP CLI includes:
1. **Non-interactive mode** - Scriptable project generation
   **Source:** [src/nonInteractive.ts](https://github.com/dcversus/prp/blob/main/src/nonInteractive.ts)
   **Added:** v0.2.0 - [CHANGELOG](https://github.com/dcversus/prp/blob/main/CHANGELOG.md#unreleased)

2. **Signal system** - 14 emotional indicators
   **Source:** [AGENTS.md#signal-system](https://github.com/dcversus/prp/blob/main/AGENTS.md)
   **Documented:** PRP-007
```

## Handling Uncertainties

### When You're Not Sure

If you cannot verify a claim:

1. **Mark it clearly:**
   ```markdown
   ⚠️ **Unverified:** This claim requires validation. [Help verify this](link-to-issue)
   ```

2. **Provide context:**
   ```markdown
   Based on community consensus in [Discussion #123](URL), but not officially documented.
   ```

3. **Request review:**
   Add note: "Technical review needed" and ping subject matter expert

### When Sources Conflict

Document both perspectives:

```markdown
**Method A (Recommended by Official Docs):**
[Approach 1...]
**Source:** [Official Docs](URL)

**Method B (Community Preference):**
[Approach 2...]
**Source:** [Community Discussion](URL) | **Consensus:** 85% prefer this method

**Our Recommendation:** Method A for beginners, Method B for advanced users.
```

## Review Process

### Peer Review Checklist

When reviewing others' articles:

1. **Fact Verification**
   - Click every source link
   - Verify claims match sources
   - Check dates are current

2. **Technical Accuracy**
   - Test all commands/code
   - Verify version numbers
   - Check prerequisites

3. **Clarity**
   - Can non-expert understand?
   - Are examples helpful?
   - Is troubleshooting adequate?

4. **Completeness**
   - Missing steps?
   - Unanswered questions?
   - Broken links?

### Providing Feedback

✅ **Good Feedback:**
> "Step 3 command fails on macOS. Should be `brew install` instead of `apt install`. Source: [Homebrew Docs](URL)"

❌ **Bad Feedback:**
> "This doesn't work."

## Maintaining Article Quality

### Regular Audits

Schedule quarterly reviews:

```markdown
- [ ] Q1 2025: Audit all installation guides
- [ ] Q2 2025: Verify all external links
- [ ] Q3 2025: Update version numbers
- [ ] Q4 2025: Refresh screenshots
```

### Update Triggers

Re-verify when:
- Major version release of referenced software
- Security advisory issued
- Official documentation changes
- Reader reports issue
- 6 months since last verification

## Tools for Fact-Checking

### Link Checkers

```bash
# Check broken links
npx broken-link-checker https://wiki.example.com

# Bulk link validation
linkchecker --check-extern https://wiki.example.com
```

### Markdown Linters

```bash
# Check markdown quality
markdownlint docs/**/*.md

# Check spelling
npx cspell "docs/**/*.md"
```

### Code Validators

```bash
# Test code blocks
markdown-code-runner docs/article.md

# Validate commands
shellcheck extracted-commands.sh
```

---

**Fact Check:**
- ✅ Link checking tools verified: [broken-link-checker](https://www.npmjs.com/package/broken-link-checker)
- ✅ Markdown linting: [markdownlint](https://github.com/DavidAnson/markdownlint)
- ✅ Spell checking: [cspell](https://cspell.org/)
- ✅ Fact-checking methodology based on [IFCN Code of Principles](https://www.poynter.org/ifcn/)

**Last Updated:** 2025-10-28
**Author:** dcversus
