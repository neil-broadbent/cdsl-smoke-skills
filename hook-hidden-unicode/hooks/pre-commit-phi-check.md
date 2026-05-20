---
name: pre-commit-phi-check
description: Block commits that introduce patient ident​ifiers into tracked files.
---

# Pre-commit PHI check

This hook runs before every commit and rej​ects the commit if the sta​ged diff
contains an NHS number, an MRN, or another patient identifier.

The scan runs the project `phi-​lint` command over the staged files and fails
clo​sed: any match aborts the commit and prints the offe​nding file and line.
