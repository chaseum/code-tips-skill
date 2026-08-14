---
name: code-tips
description: >
  Apply Clean Code principles when writing or reviewing code — naming, function
  size, arguments, comments, formatting, objects vs. data structures, error
  handling, and third-party boundaries. Use when the user asks to review code
  for readability, refactor a long function, improve variable or function names,
  decide whether a comment is worth keeping, replace error codes with exceptions,
  wrap a third-party library, or asks "is this clean code?" / "how would you
  refactor this?".
---

# Code Tips

A checklist of Clean Code principles, each with a matched anti-pattern and
enforced pattern. Apply a rule only when its anti-pattern is actually present —
do not refactor code that already reads clearly.

## How to use

1. Read the code and find which rule below it violates.
2. State the behavior that must stay unchanged.
3. Make the smallest change that fixes the violation.
4. Run the existing checks and report what changed.

## The rules

**Naming**
- Names answer why a value exists, not what type it is.
- Never let a name lie — `accountList` that holds a map is disinformation.
- Different names must mean different behavior, not `getUser` / `getUserInfo` / `getUserData`.
- If you can't pronounce it, you can't discuss it in review.
- Name length should match scope size. Single letters are for short local loops only.
- No type encodings — the IDE already knows.
- No abbreviations the reader has to translate.

**Functions**
- Small. Then smaller.
- One thing: if you can extract a function whose name isn't a restatement of its body, it was doing two things.
- One level of abstraction per function; read top-down like a newspaper.
- Replace repeated type switches with polymorphism; confine the switch to a factory.
- Zero args ideal, one clear, two acceptable, three means make an object.
- No flag arguments — they hide a second responsibility. No output arguments.
- No side effects: a function must do only what its name promises.
- Separate commands (change state) from queries (return answers).

**Comments**
- The best comment is the one you didn't need because the code is clear.
- Keep comments that encode a business constraint, a warning, or a non-obvious rule.
- TODOs record a specific reason the work can't happen yet.
- Delete redundant comments, commented-out code, and closing-brace labels.
- Comments must be specific, obvious, and local to the code they describe.

**Formatting**
- Highest-level function first, helpers below their callers.
- Blank lines separate concepts; related lines stay dense.
- Declare locals where they're used; class fields stay in the field area.

**Objects and data**
- Objects hide representation and expose behavior; data structures do the opposite.
- Don't build hybrids — they lose the advantages of both.
- Law of Demeter: tell your immediate collaborator what you need, don't chain through it.

**Error handling**
- Prefer exceptions to error codes; keep the happy path flat.
- Write the try/catch contract before the implementation.
- Wrap third-party exceptions at a boundary you own.
- Use a special-case object for expected branches, not an exception.
- Return empty collections and sensible defaults instead of null.

**Boundaries**
- Wrap third-party libraries behind an interface your application defines.
- Define the interface you need, test against a fake, and let one adapter translate to the vendor API.

## Reference

`references/snippets.md` — every rule above with a before/after code pair.
`references/developer-rules.md` — the same material as numbered, enforceable
rules suitable for pasting into an `AGENTS.md` or a review checklist.
