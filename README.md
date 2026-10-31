# Engineer Arc

A hands-on software engineering learning workspace focused on building sound engineering judgment through progressively realistic projects.

The goal is not to generate code quickly. It is to become able to reason about, build, test, and explain software systems independently.

## Learning loop

1. Understand requirements and constraints.
2. Design responsibilities, state ownership, and invariants.
3. Define observable behavior and failure cases.
4. Write tests before or alongside implementation.
5. Implement in small increments.
6. Review correctness, maintainability, and trade-offs.
7. Explain the design in your own words and record what changed.

## First exercise: Parking Lot

Start with the [Parking Lot exercise brief](exercises/parking-lot/README.md). Do not jump straight to classes or implementation: clarify requirements, assumptions, responsibilities, and invariants first.

## Getting started

Requires Python 3.12 or newer.

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -e ".[dev]"
python -m pytest
```

On Windows PowerShell, activate the environment with:

```powershell
.venv\Scripts\Activate.ps1
```

## Quality checks

Run the full local quality gate:

```bash
make check
```

Or run individual commands:

```bash
python -m ruff check .
python -m mypy src
python -m pytest
```

GitHub Actions runs linting, type checking, and tests on pushes to `main`, pull requests targeting `main`, and manual workflow dispatches. Dependabot checks Python and GitHub Actions dependencies weekly.

## Repository layout

```text
.
├── .github/
│   ├── pull_request_template.md
│   └── workflows/ci.yml
├── docs/
│   └── engineering-workflow.md
├── exercises/
│   └── parking-lot/README.md
├── src/
│   └── engineer_arc/
├── tests/
├── .gitignore
├── .python-version
├── Makefile
└── pyproject.toml
```

See [the engineering workflow](docs/engineering-workflow.md) for the project quality gates and review rubric.
