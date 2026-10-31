# Engineering Workflow

This repository is a learning environment, not a code-generation exercise. The goal is to build the ability to reason about, implement, test, and explain software.

## The loop

1. **Understand** — restate the problem, identify actors, constraints, and unknowns.
2. **Design** — assign responsibilities, identify state ownership, and write invariants.
3. **Specify** — describe observable behavior, edge cases, and failure behavior.
4. **Test** — write examples that demonstrate expected behavior before or alongside implementation.
5. **Implement** — make the smallest coherent change that passes the tests.
6. **Review** — inspect correctness, readability, coupling, and trade-offs.
7. **Reflect** — explain the design in your own words and record what you would improve.

## Working rules

- Do not add abstractions before a requirement justifies them.
- Prefer explicit behavior over clever code.
- Keep domain logic independent from frameworks and user interfaces.
- Make invalid states difficult to represent.
- Test normal cases, boundary cases, and failure cases.
- Never claim a test passed unless it was actually run.
- Keep changes small enough to explain.

## Tutor protocol

When working through an exercise, the tutor should:
- Ask one focused question at a time.
- Give a hint before revealing a complete solution.
- Explain why a design decision is appropriate, not merely what to type.
- Ask the learner to predict behavior before running code.
- Review the learner's own reasoning and code.
- Avoid taking over the implementation unless explicitly asked.

## Completion rubric

Score each category from 0 to 2:

| Category | 0 | 1 | 2 |
|---|---|---|---|
| Requirements | Missing or unclear | Mostly clear | Clear, scoped, and testable |
| Responsibility | Poorly assigned | Some overlap | Cohesive ownership |
| State and invariants | Not identified | Partially handled | Explicitly protected |
| Failure handling | Ignored | Some cases handled | Important failures specified |
| Tests | Missing | Happy path only | Normal, boundary, and failure cases |
| Explanation | Cannot explain | Partial explanation | Can explain choices and trade-offs |

A project is review-ready at 9/12 or higher, with no zero in state ownership, failure handling, or tests.
