# Assignment 01 — TA feedback: Jamil (Jamil Vallis-Walker)

- **Evaluated by:** Yilin Pan (TA)
- **Date:** 2026-10-05

## Scores

| Category | Pts | Student's LLM eval | TA verified | Notes |
|---|---|---|---|---|
| Immutability & encapsulation | 25 | 25 | 25 | |
| Constructor validation | 25 | 22 | 22 | |
| Correctness | 15 | 15 | 15 | |
| Testing | 15 | 13 | 13 | |
| Code quality & style | 10 | 9 | 9 | |
| Introspection, LLM eval & code walk | 10 | 7 | 9 | −1 scope (`HashMap`); `Species` is graded from the code walk |
| **Total** | **100** | **91** | **93** | |

## Checks

- [x] All tests pass (31/31)
- [x] No `UnsupportedOperationException` stubs left
- [x] Checkstyle warnings: 0
- [x] Coverage (lines / branches): 100% / 100%
- [ ] Nothing out of scope (inheritance, collections, `equals`/`hashCode`): `HashMap`/`Map` used in `Animal`
- [x] `submission/LLM-Evaluation.md` present
- [x] `submission/introspection.md` present

## Where the TA disagrees with the student's LLM evaluation

- Categories 1–5: I'm keeping your LLM's scores. Your LLM got one thing wrong, though. Collapsing
  interior spaces (Animal.java:193) isn't "a superset of the spec". `"Mr  Whiskers"` gets stored as
  `"Mr Whiskers"`, which changes the name.
- Cat 6 +2: −1 for using `HashMap`/`Map` in `Animal` (Animal.java:4–5, 165–170), since the lab
  excludes collections. Explaining `Species` is part of the code walk, not the introspection, and your code walk covered it, so full credit.

## Feedback

Your tests are strong, with exact message checks and lots of Unicode whitespace cases. The main thing
is to stick to what the spec asks. The whitespace normalization and the Map-based validation add
risk without adding value. A few small things:

- The "U+00A0" entry at AnimalTest.java:33 is actually a regular space.
- You replaced the provided 1-month delegation test instead of adding a new one.
- There's a leftover `System.err.println` at AnimalTest.java:180.
- There's no test for `MAX_MONTHS - 1`.

## Grade

**Final grade:** 93 / 100
