# Make search better

Status: Backlog · Priority: Normal · Size: Unset

## User problem

Someone remembers a phrase from a note but cannot find it through the current
title-only search.

## Concrete example

A note titled "Trip planning" contains "blue suitcase" in its body. Searching for
"suitcase" returns nothing.

## Desired outcome

Find a note using remembered content, even when its title does not contain it.

## Current workaround

Open likely notes one by one and search their text.

## Decisions needed

- Should search match the body as well as the title?
- Does matching mean a case-insensitive substring, whole words, or something else?
- How should results be ordered, and what is the expected data size?

Next action: the maintainer confirms matching and ordering rules. Then prepare a
bounded implementation task with examples and verification. "Make search better"
is not sufficient acceptance criteria, so this remains in Backlog.
