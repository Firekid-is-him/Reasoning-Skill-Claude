# FIRST_PRINCIPLES.md — Breaking Problems to Their Root

Most answers are built on top of other answers built on top of assumptions
that nobody has questioned in years. First principles reasoning strips all of that away
and rebuilds from what is actually true.

---

## What first principles reasoning is

It is the process of breaking a problem down to its most fundamental components —
the things that are actually true — and reasoning back up from there
instead of reasoning from what's commonly believed or commonly done.

**Pattern matching** = "People solve this problem by doing X, so do X"
**First principles** = "What is this problem actually made of? What would solve it at that level?"

---

## How to apply it

### Step 1: State what you know for certain
Not what you've heard. Not what's commonly done. What is actually, verifiably true
about this problem at its most basic level.

### Step 2: Identify what's assumed
What beliefs are built into how this problem is usually framed?
Are those beliefs actually true, or are they inherited conventions?

### Step 3: Rebuild from the certain things
If you only had the verified true things and none of the inherited assumptions,
what solutions would you arrive at?

### Step 4: Compare
How does the first-principles solution compare to the conventional one?
Is the conventional approach doing something unnecessarily? Is it missing something?

---

## Why this matters

Most "impossible" things are impossible only within a specific set of assumptions.
Change the assumptions and the impossibility disappears.

The question "how do I do X?" assumes X is the right goal.
The question "what am I actually trying to achieve?" opens up every possible path.

---

## Applied example pattern

**Question:** "How do I get persistent state on Vercel?"

**Pattern matching answer:** "Vercel is serverless, it doesn't support persistent state. Use a different platform."

**First principles answer:**
- What is the actual goal? → State that persists between requests
- What does "persistent" actually require? → Storage that lives outside the request lifecycle
- What is Vercel actually blocking? → Long-running processes on their servers
- Is long-running process on their servers the only way to have persistent state? → No
- Therefore: Store state externally, access it from the serverless function. Vercel becomes the interface, not the store.

The wall only existed inside the original framing of the question.
