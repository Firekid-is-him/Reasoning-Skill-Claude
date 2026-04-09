---
name: reasoning-search
description: >
  A search framework that forces Claude to search using reasoning, not just keyword matching.
  Use this whenever a web search is needed. Claude should search based on what the problem
  actually is — not just the words the user said. Searches should cover the date range
  2015 to present unless otherwise specified. Always active alongside the reasoning skill.
---

# Reasoning Search Skill

Searching for what the user said is not the same as searching for what they need.
This skill forces search to be driven by reasoning about the problem —
not pattern matching on the user's exact words.

---

## Core search principles

### 1. Search the goal, not the request
Before running a search, identify the real goal behind the request.
Search for that goal — not the literal phrasing of the question.

**Example:**
- User says: "how to make Vercel a persistent server"
- Wrong search: "Vercel persistent server"
- Right search: "persistent state serverless architecture" + "Vercel external state management"

The right search finds solutions. The wrong search finds walls.

---

### 2. Search across domains
If a search within the obvious domain returns no useful results,
search in adjacent or unrelated domains for analogous solutions.

The answer to a frontend problem might be documented as a backend pattern.
The answer to a software problem might be documented as a networking pattern.
Expand the search domain before concluding no answer exists.

---

### 3. Default date range: 2015 to current year
Unless the user specifies otherwise, search within 2015 to present.
This captures the modern tech era while excluding outdated approaches
that may no longer apply.

For rapidly changing topics (AI, cloud infrastructure, mobile development):
prioritize results from the last 2 years within that range.

For stable topics (algorithms, mathematics, protocols):
the full range is appropriate.

---

### 4. Search in layers

**Layer 1 — Broad search:** What is the landscape of this problem?
**Layer 2 — Specific search:** What are the specific solutions that fit this context?
**Layer 3 — Validation search:** Do these solutions actually work? Are there known failure cases?
**Layer 4 — Alternative search:** If the main solutions don't fit, what else exists?

Don't stop at layer 1 and return results. Go deeper until something actually useful is found.

---

### 5. Search for failure cases, not just solutions

A solution that sounds right but has a known failure mode is not a good recommendation.
Always search for: "[solution] problems", "[solution] limitations", "[solution] doesn't work when"

Knowing where a solution breaks is as important as knowing that it exists.

---

### 6. Never return results that don't survive the context filter

Before presenting search results, run them through CONTEXT.md filters:
- Does this solution work for someone in this person's likely location?
- Does it require resources or infrastructure this person may not have?
- Is it actually current or is it an outdated approach?

Filter out results that fail these checks before presenting.

---

## Search query construction rules

- Build queries from the underlying problem, not the surface request
- Use multiple shorter targeted queries rather than one long complex query
- Search for the problem from multiple angles before concluding no solution exists
- When one query fails, reason about why it failed and adjust the angle — don't repeat it slightly rephrased
- Include year ranges when recency matters: append "2020 2021 2022 2023 2024 2025" or "after:2020"

---

## When search returns nothing useful

If multiple searches across multiple angles return nothing useful:
- State this honestly
- Explain what was searched and why it didn't return what was needed
- Reason from first principles about what might exist even if it isn't documented
- This itself is useful — it tells the person they may be at the frontier of an unsolved problem
