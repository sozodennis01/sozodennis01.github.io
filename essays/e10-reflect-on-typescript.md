---
layout: essay
type: essay
title: "ICS314 Summer 2026 - E10 TypeScript Reflection"
# All dates must be YYYY-MM-DD format!
date: 2026-06-05
published: true
labels:
  - Artificial Intelligence
  - Software Engineering
  - Learning
---
# TypeScript Is Fine, But I Miss My Types Up Front

*ICS 314 — E10 Reflection | Dennis Sarsozo | June 2026*

---

## My Background with TypeScript

I am not a complete beginner here. Most of my day-to-day work lives in C, C++, and some C# and Java. I have done embedded systems, flight software at HSFL, and a fair amount of Python. TypeScript is not my first language, and honestly it is not my favorite either — but the last time I actually wrote it was probably five or six years ago, so this module was a decent refresher.

The core thing that still bothers me is the type annotation style. Coming from C-family languages, I am used to declaring the type first: `int count`, `float velocity`. In TypeScript you write `let count: number`, and I know that is not wrong, it just feels backwards. It reads like you named the thing before you decided what it is. Minor complaint, but it sticks.

---

## What ES6 Actually Taught Me

One thing I genuinely did not know before this module: the distinction between `null` and `unknown`.

- **`null`** is a known empty value. You set it intentionally. The runtime knows this slot is empty.
- **`unknown`** means the type has not been determined yet — it is the TypeScript-safe alternative to `any`.

That distinction matters more than it sounds. In embedded work, a null pointer does not just return an empty value — it crashes the program, or worse, corrupts memory silently. TypeScript's type system enforces a boundary around that uncertainty at compile time, which is a real software engineering win even if the syntax annoys me.

```typescript
let result: unknown = fetchData();

if (typeof result === "string") {
  console.log(result.toUpperCase()); // safe — type narrowed
}
```

The compiler forces you to prove you know what you have before you use it. That is good design.

---

## Is TypeScript a Good Language?

From a software engineering perspective — yes, it is a net positive. JavaScript on its own has enough footguns that adding a static type layer on top makes large codebases significantly more maintainable. You get autocomplete, refactoring support, and compile-time errors instead of runtime surprises.

My honest opinion: TypeScript is a practical tool. I would not choose it for systems work, but for web and application development it solves real problems. If you are already writing JavaScript, there is no good reason not to use it.

---

## Athletic Software Engineering — What I Think About the WODs

The practice WODs are basically a low-stakes version of a technical interview. You are given a problem, you have a time limit, and you have to produce working code. I have been in real interviews where I did not solve the problem on the whiteboard perfectly, but I was able to walk through my reasoning — memory footprint, time complexity, edge cases. The WODs build that same habit.

Is it stressful? A little, but not in a bad way. The stress is proportional to how prepared you are. If you understand the material, the timer is just pressure. If you do not understand it, the timer is a signal.

This is a remote class, so there was no one sitting across from me watching the clock. That removed some of the anxiety. But the real value is not the timer itself — it is that you have to actually write the code instead of just reading about it.

---

## Does This Style of Learning Work for Me?

Yes. I prefer performance-based learning. I have always learned more from doing than from sitting through lectures or grinding through proofs. In computer science, there is too much emphasis on mathematical formalism and not enough on building things and breaking them. The WODs push you toward the latter.

I am not trying to become a TypeScript expert. I am taking this class, learning the patterns, and applying them. That is the goal. If you do the work in ICS 314, you pass. I have heard that from multiple people, and the structure confirms it. That is a fair contract.

---

## A Note on AI Use

I am going to be direct about this: I used AI to clean up this essay. My process is to record a voice memo with all my raw thoughts, transcribe it (either through macOS Voice Memos or Whisper), and then hand the transcript plus the assignment checklist to Claude. Claude cleans up the grammar, organizes the structure, and keeps my tone. I review the output and make sure it still sounds like me before submitting.

I think this is a legitimate way to work. It is prompt engineering. The ideas are mine — I said them out loud before any AI touched them. The AI helped with presentation, not content. That distinction matters to me, and I am comfortable owning it.

---

*Written for ICS 314, Software Engineering I. University of Hawaiʻi at Mānoa, Summer 2026.*
