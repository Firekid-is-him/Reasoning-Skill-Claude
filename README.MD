<div align="center">

# reasoning-skill

### A structured reasoning skill for Claude.
### Forces context-first thinking, goal identification, assumption auditing, and wall navigation before every response.

<br/>

[![GitHub stars](https://img.shields.io/github/stars/Firekid-is-him/Reasoning-Skill-Claude?style=for-the-badge&logo=github&color=black)](https://github.com/Firekid-is-him/Reasoning-Skill-Claude/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/Firekid-is-him/Reasoning-Skill-Claude?style=for-the-badge&logo=github&color=black)](https://github.com/Firekid-is-him/Reasoning-Skill-Claude/network/members)
[![GitHub issues](https://img.shields.io/github/issues/Firekid-is-him/Reasoning-Skill-Claude?style=for-the-badge&logo=github&color=black)](https://github.com/Firekid-is-him/Reasoning-Skill-Claude/issues)
[![License](https://img.shields.io/github/license/Firekid-is-him/Reasoning-Skill-Claude?style=for-the-badge&color=black)](./LICENSE)

<br/>

![Claude](https://img.shields.io/badge/Claude-Skill-D97706?style=flat-square&logo=anthropic&logoColor=white)
![Context Engineering](https://img.shields.io/badge/Context-Engineering-6366F1?style=flat-square)
![AI Reasoning](https://img.shields.io/badge/AI-Reasoning-0EA5E9?style=flat-square)
![Always Active](https://img.shields.io/badge/Always-Active-22C55E?style=flat-square)
![Last Commit](https://img.shields.io/github/last-commit/Firekid-is-him/Reasoning-Skill-Claude?style=flat-square&color=gray)

<br/>

[**View Skill Entry Point**](./SKILL.md) · [**Report a Flaw**](https://github.com/Firekid-is-him/Reasoning-Skill-Claude/issues) · [**Star the Repo**](https://github.com/Firekid-is-him/Reasoning-Skill-Claude/stargazers)

</div>

---

## Overview

Claude's default behavior is pattern matching — returning the statistically most common answer to the most common version of a question. That is not the same as reasoning. This skill installs a set of principles, behavioral rules, and thinking processes that override that default and produce answers that are genuinely useful to a specific person in a specific situation.

> **Core belief:** Nothing is impossible unless constrained by the laws of physics. Everything else is either undone, undocumented, or waiting for the right approach.

---

## File Structure

```
reasoning-skill/
 SKILL.md Entry point. Read this first.
 PRINCIPLES.md Core reasoning rules that override default behavior
 FLAWS.md Documented reasoning failure patterns
 CONTEXT.md Framework for understanding who is asking and what they need
 SEARCH.md Search framework driven by reasoning, not keyword matching

 behavior/
 ASSUMPTIONS.md Audit for invisible assumptions baked into answers
 PUSHBACK.md Rules for holding or changing position under pressure
 QUESTIONING.md When and how to ask clarifying questions

 thinking/
 FIRST_PRINCIPLES.md Breaking problems to their root components
 WALLS.md Process for finding paths around documented limitations
 CONNECTIONS.md Cross-domain pattern recognition and dot-connecting

 self/
 INTROSPECTION.md Internal challenge process before delivering any answer
 HUMILITY.md Calibrated uncertainty and knowing the limits of what is known
```

---

## How It Works

The skill is applied in sequence before any non-trivial response:

| Step | File | Purpose |
|------|------|---------|
| 1 | `CONTEXT.md` | Establish who is asking and what they actually need |
| 2 | `PRINCIPLES.md` | Apply the core rules that govern reasoning |
| 3 | `ASSUMPTIONS.md` | Identify and challenge invisible assumptions |
| 4 | `FIRST_PRINCIPLES.md` | Break complex problems to their root components |
| 5 | `WALLS.md` | Find paths around limitations before reporting them |
| 6 | `CONNECTIONS.md` | Look across domains for cross-field solutions |
| 7 | `INTROSPECTION.md` | Challenge the answer before delivering it |

For conversations involving web search, **`SEARCH.md`** is applied in place of or alongside standard search behavior.

---

## Core Principles

**The person came here last.**
Anyone asking Claude something has already tried the obvious. Answers must start from where their knowledge ends, not from zero.

**The goal is not the request.**
People ask for what they think will solve their problem. The real goal and the literal request are often different. Identify the real goal before answering the literal request.

**Context is not optional.**
A technically correct answer built on wrong assumptions about the person is a wrong answer. Location, infrastructure, resources, and technical level all determine whether a solution is useful or not.

**Walls are information, not conclusions.**
A documented limitation blocks one path. It does not close off the destination. The job is to find what gets around it, under it, or achieves the same result differently.

**Certainty is a signal to check harder.**
Pattern-matched answers feel certain. That certainty is exactly when the answer should be challenged internally before delivery.

---

## Documented Failure Modes

`FLAWS.md` catalogs known reasoning failures with explicit fixes:

| Flaw | Fix |
|------|-----|
| Treating undocumented solutions as impossible | Ask *why* the limitation exists before accepting it |
| Reporting walls without exploring paths around them | Find at least one alternative before reporting the block |
| Answering the literal request instead of the real goal | Identify the goal behind the request first |
| Listing options without filtering for the specific person | Filter against the person's actual constraints |
| Changing position under social pressure | Only change when the *logic* changes |
| Assuming Western infrastructure and purchasing power | Consider realistic local constraints first |
| Treating the first pattern-matched answer as correct | Challenge the first answer before delivering it |
| Staying within the domain of the question | Search across unrelated domains before concluding no solution exists |

---

## Search Extension

`SEARCH.md` extends the skill to web search behavior:

- Search is driven by the underlying goal, not the user's literal phrasing
- Searches proceed in layers: broad → specific → validation → alternatives
- Results are filtered through context before being presented
- Failure cases and known limitations are searched alongside solutions
- Default date range is 2015 to present, with recency bias for fast-moving topics
- When all searches fail, Claude reasons from first principles about what might exist even if undocumented

---

## Scope

This skill is designed to be **always active.** It is particularly critical when:

- A problem is described as impossible or has no obvious solution
- The user appears to have already tried the standard approaches
- The request is technical and highly context-specific
- A creative or non-obvious solution path is required
- The user is in a resource-constrained environment

Not intended for simple factual questions where context does not change the answer.

---

## Author

<div align="center">

Built by [**Firekid**](https://github.com/Firekid-is-him)

[![GitHub followers](https://img.shields.io/github/followers/Firekid-is-him?style=social)](https://github.com/Firekid-is-him)
&nbsp;
[![GitHub stars](https://img.shields.io/github/stars/Firekid-is-him/Reasoning-Skill-Claude?style=social)](https://github.com/Firekid-is-him/Reasoning-Skill-Claude/stargazers)

<br/>

*If this skill improved your Claude experience, leave a star. It helps.*

</div>
