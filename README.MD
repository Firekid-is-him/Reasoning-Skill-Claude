# reasoning-skill

A structured reasoning skill for Claude. Forces context-first thinking, goal identification, assumption auditing, and wall navigation before every response.

![Claude Skill](https://img.shields.io/badge/Claude-Skill-black?style=flat-square&logo=anthropic)
![License](https://img.shields.io/github/license/Firekid-is-him/Reasoning-Skill-Claude?style=flat-square)
![Last Commit](https://img.shields.io/github/last-commit/Firekid-is-him/Reasoning-Skill-Claude?style=flat-square)
![Topics](https://img.shields.io/badge/topics-claude%20%7C%20reasoning%20%7C%20context--engineering-blue?style=flat-square)

---

## Overview

Claude's default behavior is pattern matching — returning the statistically most common answer to the most common version of a question. That is not the same as reasoning. This skill installs a set of principles, behavioral rules, and thinking processes that override that default and produce answers that are genuinely useful to a specific person in a specific situation.

The skill is structured around one core belief: nothing is impossible unless it is constrained by the laws of physics. Everything else is either undone, undocumented, or waiting for the right approach.

---

## File Structure

```
reasoning-skill/
  SKILL.md                    Entry point. Read this first.
  PRINCIPLES.md               Core reasoning rules that override default behavior
  FLAWS.md                    Documented reasoning failure patterns
  CONTEXT.md                  Framework for understanding who is asking and what they need
  SEARCH.md                   Search framework driven by reasoning, not keyword matching

  behavior/
    ASSUMPTIONS.md            Audit for invisible assumptions baked into answers
    PUSHBACK.md               Rules for holding or changing position under pressure
    QUESTIONING.md            When and how to ask clarifying questions

  thinking/
    FIRST_PRINCIPLES.md       Breaking problems to their root components
    WALLS.md                  Process for finding paths around documented limitations
    CONNECTIONS.md            Cross-domain pattern recognition and dot-connecting

  self/
    INTROSPECTION.md          Internal challenge process before delivering any answer
    HUMILITY.md               Calibrated uncertainty and knowing the limits of what is known
```

---

## How It Works

The skill is applied in sequence before any non-trivial response. The recommended reading order is:

1. **CONTEXT.md** — Establish who is asking and what they actually need before forming any answer
2. **PRINCIPLES.md** — Apply the core rules that govern reasoning throughout the response
3. **ASSUMPTIONS.md** — Identify and challenge invisible assumptions in the answer being formed
4. **FIRST_PRINCIPLES.md** — If the problem is complex, break it to its fundamental components
5. **WALLS.md** — If a limitation has been encountered, run the wall process before reporting it
6. **CONNECTIONS.md** — Look across domains for patterns that might solve the underlying problem
7. **INTROSPECTION.md** — Challenge the answer before delivering it

For conversations involving web search, **SEARCH.md** is applied in place of or alongside standard search behavior.

---

## Core Principles

**The person came here last.** Anyone asking Claude something has already tried the obvious. Answers must start from where their knowledge ends, not from zero.

**The goal is not the request.** People ask for what they think will solve their problem. The real goal and the literal request are often different. Identify the real goal before answering the literal request.

**Context is not optional.** A technically correct answer built on wrong assumptions about the person is a wrong answer. Location, infrastructure, resources, and technical level all determine whether a solution is useful or not.

**Walls are information, not conclusions.** A documented limitation blocks one path. It does not close off the destination. The job is to find what gets around it, under it, or achieves the same result differently.

**Certainty is a signal to check harder.** Pattern-matched answers feel certain. That certainty is exactly when the answer should be challenged internally before delivery.

---

## Documented Failure Modes

The skill includes **FLAWS.md**, a catalog of known reasoning failures with explicit fixes. Key failures addressed:

- Treating undocumented solutions as impossible
- Reporting walls without exploring paths around them
- Answering the literal request instead of the real goal
- Listing options without filtering them for the specific person
- Changing position under social pressure rather than logical pressure
- Defaulting to solutions that assume Western infrastructure and purchasing power
- Treating the first pattern-matched answer as the best answer
- Staying within the domain of the question instead of searching across domains

---

## Search Extension

**SEARCH.md** extends the skill to web search behavior. Key rules:

- Search is driven by the underlying goal, not the user's literal phrasing
- Searches proceed in layers: broad landscape, specific solutions, validation, alternatives
- Results are filtered through context before being presented
- Failure cases and known limitations are searched for alongside solutions
- Default date range is 2015 to present, with recency bias for fast-moving topics
- When all searches fail, the skill instructs Claude to reason from first principles about what might exist even if undocumented

---

## Scope

This skill is designed to be always active. It is particularly important when:

- A problem is described as impossible or has no obvious solution
- The user appears to have already tried the standard approaches
- The request is technical and context-specific
- A creative or non-obvious solution path is required
- The user is in a resource-constrained environment

It is not intended for simple factual questions where context does not change the answer.

---

## Author

Built by [Firekid](https://github.com/firekid).

[![GitHub stars](https://img.shields.io/github/stars/Firekid-is-him/Reasoning-Skill-Claude?style=social)](https://github.com/Firekid-is-him/Reasoning-Skill-Claude/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/Firekid-is-him/Reasoning-Skill-Claude?style=social)](https://github.com/Firekid-is-him/Reasoning-Skill-Claude/network/members)
