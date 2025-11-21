---
title: Writing Valid Articles
description: How to write proof-checked wiki articles
published: true
date: 2025-10-28T11:59:42.752Z
tags: [writing, documentation, best-practices]
editor: markdown
---

# Writing Valid Proof-Checked Articles

## Mandatory Requirements

Every factual claim must include:

1. **Source Link** - URL to authoritative source
2. **Verification Date** - When fact was checked
3. **Context** - Why this fact matters

## Article Structure Template

```markdown
---
title: Article Title
description: Brief description
published: true
date: YYYY-MM-DD
tags: [tag1, tag2, tag3]
editor: markdown
---

# Article Title

> **Source:** [Authority](URL) | **Verified:** YYYY-MM-DD

## Introduction

[Clear, concise intro...]

## Main Content

### Subsection

[Content with inline citations...]

**Reference:** [Source Name](https://example.com/source)

## Fact Check Section

**Fact Check:**
- ✅ Claim 1: [Source](URL) - Verified YYYY-MM-DD
- ✅ Claim 2: [Source](URL) - Verified YYYY-MM-DD
- ⚠️ Claim 3: Based on observation, not peer-reviewed

**Last Updated:** YYYY-MM-DD
**Author:** Name

---

**Next:** [Related Article](link) →
```

## Self-Check Criteria

Before publishing, verify:

- [ ] Every factual claim has a source
- [ ] All URLs are valid and accessible
- [ ] Verification dates are current (< 6 months)
- [ ] Screenshots are clear and annotated
- [ ] Code examples are tested
- [ ] Grammar and spelling checked
- [ ] Links work and go to correct pages
- [ ] Fact Check section is complete

## Citation Standards

### Web Resources

```markdown
**Source:** [Site Name - Article Title](https://exact-url.com)
**Verified:** 2025-10-28
```

### Research Papers

```markdown
**Source:** Author et al. (Year). "Title". *Journal*. [DOI](https://doi.org/...)
**Verified:** 2025-10-28
```

### Official Documentation

```markdown
**Source:** [Official Docs - Section](https://docs.example.com/section)
**Version:** 2.0.1
**Verified:** 2025-10-28
```

## Common Mistakes to Avoid

❌ **Bad:**
> "Studies show that X is better than Y."

✅ **Good:**
> "A 2024 study by MIT researchers found X performed 30% better than Y in benchmarks."
> **Source:** [MIT Study](https://example.com) | **Verified:** 2025-10-28

❌ **Bad:**
> "Everyone knows that..."

✅ **Good:**
> "According to the official documentation..."
> **Source:** [Docs](URL) | **Verified:** 2025-10-28

## Updating Outdated Articles

When information changes:

1. Update the content
2. Update verification dates
3. Add note about what changed
4. Update "Last Updated" date

```markdown
> **Update:** As of 2025-10-28, this process has changed. See [New Guide](URL).
```

## Quality Standards

### Excellent Article Example

✅ Clear structure
✅ Every claim sourced
✅ Recent verification dates
✅ Helpful examples
✅ Troubleshooting section
✅ Links to related articles
✅ Complete fact check

---

**Fact Check:**
- ✅ Article structure template follows [Wiki.js Markdown Guide](https://docs.requarks.io/editors/markdown)
- ✅ Citation standards based on [APA Style](https://apastyle.apa.org)
- ✅ Self-check criteria from [Technical Writing Best Practices](https://developers.google.com/tech-writing)

**Last Updated:** 2025-10-28
**Author:** dcversus
