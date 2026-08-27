# BYRSA — read-only fork provenance

This fork is **read-only** for the BYRSA workspace. No code in this repository
is modified; this file is the entire diff.

The BYRSA workspace forks five repositories on the instruction to *"pin the
version, mine one idea each"*. This records the pin and the idea, so a later
session can tell what was borrowed and check it against the source.

| | |
|---|---|
| **Pinned commit** | `9cd20b6a3232b77ac114fb45a3979d51a4332850` (`9cd20b6`, 2026-06-18) |
| **Idea mined** | **The one-ply `SimpleBot` pattern.** Enumerate your legal options, simulate each, score the resulting state, take the best. It is the correct first rung above heuristics and the honest baseline any search agent has to beat. |
| **Where it landed** | `byrsa-sim/byrsa_sim/agents/tier4.py::GreedyBot`, scored against BYRSA's actual objective (A2 §5: binary and total) plus the Sufet tempo term |
| **Cited in** | `01` §4 Tier 4 |

## Why pinning matters

A borrowed idea that drifts with upstream is an unrecorded dependency. The BYRSA
corpus requires every finding to carry a git SHA and seed range; a technique
borrowed from a moving target would break that chain. This fork is not tracked
for updates — if the idea needs revisiting, it is revisited against **this**
commit.

## What was NOT taken

No rule from any bundled game, ever. BYRSA's rules live in exactly one place:
A2 of the corpus, implemented by `byrsa-sim/byrsa_sim/rules.py`. What is
borrowed here is *methodology* — how to structure a bot roster, how to shape a
report, how to parameterise a strategy — never a mechanic.
