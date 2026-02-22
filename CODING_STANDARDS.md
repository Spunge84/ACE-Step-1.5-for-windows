# ACE-Step 1.5 Coding Standards

## General Principles
- **Minimal Scope:** Solve one problem per task/PR. Touch only necessary files.
- **Stability First:** Preserve behavior for non-target hardware paths (CPU/CUDA/MPS/XPU).
- **Review Rigor:** Follow the review/accept/rebut/fix cycle defined in `CONTRIBUTING.md`.

## Python Standards
- **Decomposition:**
  - Target module size: `<= 150` LOC.
  - Hard cap: `200` LOC (requires justification).
  - Split functions by responsibility (Single Responsibility Principle).
- **Documentation:**
  - Mandatory docstrings for all modules, classes, and functions.
  - Include purpose, inputs, outputs, and exceptions.
- **Types:** Use type hints for all new or modified functions.
- **Testing:**
  - Use `unittest` style.
  - Filenames: `*_test.py` or `test_*.py`.
  - Mandatory success-path and regression tests for all changes.

## UI & CSS Patterns
- **Primary Framework:** Gradio (Python-based UI).
- **Studio Interface:** Clean, dark-themed HTML/CSS with standard modern layouts.
- **Design Language:** Follow the "Studio Pro" aesthetic (Dark background, Accent color `#1DB954`).
- **Standard:** New React/Next.js components should adhere to `shadcnui` patterns and accessibility standards.

## Naming Conventions
- **Files/Modules:** `snake_case.py`
- **Classes:** `PascalCase`
- **Functions/Variables:** `snake_case`
- **Constants:** `UPPER_SNAKE_CASE`