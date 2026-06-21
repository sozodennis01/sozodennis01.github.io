---
layout: essay
type: essay
title: "Linters Are Just Compilers, and Neither Is the Most Important Thing"
# All dates must be YYYY-MM-DD format!
date: 2026-06-20
published: true
labels:
  - Software Engineering
  - Coding Standards
  - ESLint
---

## ESLint Was Annoying at First

I am going to be honest: dealing with ESLint for the first time was annoying. Every save lit up a wall of red squiggles, and fixing them felt like busywork when the code already ran fine. But once I got past the initial friction, I understood what it was doing. It standardizes the way you write code, the same way a C compiler catches footguns before they blow up at runtime. JavaScript is an extremely flexible language, and it works in some genuinely weird ways. A linter is basically a compiler for all the stuff the actual compiler lets you get away with.

## Coding Standards in the Age of AI

My first instinct was that coding standards are not that important anymore now that AI can write code for you. But I take that back. Linters and compilers are actually *more* important when AI is in the picture, because they give you a verified signal that the AI is on the right track.

Think about it from an organization's perspective. You let an AI agent loose on a codebase, it modifies a file, and then it tries to push. But it cannot actually push to the repo unless it passes your custom lint rules first. That is a real gate — a machine-checkable one — and it is useful precisely because AI does not always get things right on its own. The linter is the guardrail.

## What I Think Actually Matters More

That said, I think the shape of code and overall system architecture matters more than any individual lint rule. If a human can read and understand the system, an AI can understand it too, and the reverse is also true. Good architecture makes everything downstream easier — linting, testing, onboarding, debugging. A perfectly linted codebase with bad architecture is still a mess.

Overall, dealing with all the ESLint stuff was annoying because at the end of the day this is an assignment. But if I am being real about what I think matters in software engineering: system architecture and design come first. A linter and compiler are important tools, but they are not the most important thing.

---

## A Note on AI Use

I recorded a voice memo with my thoughts, transcribed it, and used Claude to clean up the grammar and organize the structure. The opinions and content are mine. The AI helped with presentation, not with generating ideas.

---

*Written for ICS 314, Software Engineering I. University of Hawaiʻi at Mānoa, Summer 2026.*
