# Enhanced Calculator (Python)

A modular, pattern‑driven, fully‑tested calculator application implemented in Python. This project demonstrates clean software architecture, multiple design patterns, robust input validation, state management (undo/redo), and a fully interactive REPL interface — all backed by a comprehensive pytest suite with 97% coverage.

## Features
- Arithmetic operations: add, subtract, multiply, divide, power, root
- Undo/redo using the Memento pattern
- Logging & autosave via Observer pattern
- Input validation using Decimal
- Environment‑driven configuration
- Fully interactive REPL interface
- 97% test coverage with pytest

## Architecture Overview
The project is organized into clear modules under app/:
```text
enhanced-calculator/
│
├── app/
│   ├── __init__.py
│   ├── calculation.py
│   ├── calculator.py
│   ├── calculator_config.py
│   ├── calculator_memento.py
│   ├── calculator_repl.py
│   ├── exceptions.py
│   ├── history.py
│   ├── input_validators.py
│   └── operations.py
│
└── tests/
    ├── conftest.py
    ├── test_calculation.py
    ├── test_calculator.py
    ├── test_calculator_config.py
    ├── test_calculator_memento.py
    ├── test_calculator_repl.py
    ├── test_exceptions.py
    ├── test_history.py
    ├── test_input_validators.py
    └── test_operations.py
```
### Core Logic
- calculation.py — value object for a single calculation
- operations.py — strategy classes + factory

### Application Layer
- calculator.py — main controller (Facade)
- calculator_memento.py — undo/redo snapshots
- history.py — observers for logging/autosave

### Validation & Config
- input_validators.py
- calculator_config.py

### Interface
- calculator_repl.py — command‑line REPL

## Design Patterns Used
- Strategy — arithmetic operations
- Factory — operation creation
- Observer — logging & autosave
- Memento — undo/redo
- Facade — unified calculator interface