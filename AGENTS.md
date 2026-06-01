# Project Instructions

## Scope

This repository demonstrates how small educational practice repositories can be prepared for Codex-style maintenance.

## Commands

- Audit all practices with `codex-study audit practicas/python-basics` and `codex-study audit practicas/cpp-basics`.
- Run the Python example from its practice folder with `cd practicas/python-basics && python -m unittest discover -s tests`.
- Run the C++ example with `mkdir -p build && g++ -std=c++17 -I practicas/cpp-basics/src practicas/cpp-basics/tests/test_sumar_pares.cpp -o build/test_sumar_pares && ./build/test_sumar_pares`.

## Workflow

- Keep practice-specific instructions in each practice folder.
- Keep root-level docs focused on navigation and maintainer workflow.
- When adding a new practice, include tests, a rubric and a validation command.
