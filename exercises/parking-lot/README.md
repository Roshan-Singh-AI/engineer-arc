# Parking Lot System — Exercise 01

## Goal

Design and implement the domain logic for a small parking facility. The exercise is intended to teach object-oriented design, responsibility assignment, state management, invariants, and testing.

**Do not start by creating classes.** First clarify the requirements and write down your assumptions.

## Initial scope

Assume one parking facility. It has a finite collection of parking spaces. A vehicle enters, receives a parking allocation, and later leaves. The system must prevent invalid allocations and keep occupancy accurate.

This is deliberately incomplete: identifying missing requirements is part of the exercise.

## Out of scope for the first version

- Multiple facilities or locations
- Online payments and billing integrations
- License-plate recognition hardware
- User accounts and authentication
- Distributed coordination
- Web UI, mobile UI, and database persistence

## Your first deliverable: requirements

Create a short requirements note answering these questions:

1. What kinds of vehicles exist?
2. Are spaces different sizes or types?
3. Can every vehicle use every space?
4. How is a space selected when several are available?
5. What information does a parking ticket contain?
6. What makes a ticket valid?
7. What should happen if the lot is full?
8. What should happen if the same vehicle attempts to enter twice?
9. What should happen if an unknown or already-used ticket is presented at exit?
10. What should happen if an exit operation fails?

For every answer, label it as either a confirmed requirement or an assumption you are making.

## Invariants to consider

An invariant is a rule that must remain true before and after every valid operation.

- A space cannot be occupied by more than one vehicle.
- A vehicle cannot have two active allocations in this single-lot version.
- A released space becomes available again.
- Occupancy must never exceed capacity.
- A ticket can be used to release only its own active allocation.

Add, remove, or refine invariants based on the requirements you choose.

## Observable operations

Describe the expected input, output, and failure behavior for:

- Parking a vehicle
- Finding an available space
- Looking up an active ticket
- Releasing a vehicle / space

Do not decide which class owns an operation until you understand the behavior and state involved.

## Acceptance criteria

The first design review is complete when you can:

- Explain the scope and assumptions.
- Describe the entry and exit flows.
- List the important invariants.
- Identify normal and failure cases.
- Explain what information must be stored and why.

Only after this review should you propose classes and implement the domain model.
