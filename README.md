## Environment and Dependency Setup
### Team: Phsyics
#### Challenge: Pasqal Neutral Atom Optimization
*DuQuantum 2026*

## Requirements

- **Python:** 3.13 or later
- **Package manager:** [uv](https://docs.astral.sh/uv/)

## Dependencies

| Package | Version |
|---|---|
| [Pulser](https://pypi.org/project/pulser/) | ≥ 1.9.1 |
| [QoolQit](https://pypi.org/project/qoolqit/) | ≥ 1.4.0 |
| [QUBO Solver](https://pypi.org/project/qubo-solver/) | ≥ 0.9.1 |
| [Emu-SV](https://pypi.org/project/emu-sv/) | Latest compatible |
| [Pasqal Cloud](https://pypi.org/project/pasqal-cloud/) | ≥ 0.24.0 |
| [NumPy](https://pypi.org/project/numpy/) | ≥ 2.5.4 |
| [Matplotlib](https://pypi.org/project/matplotlib/) | ≥ 3.11.2 |

Exact resolved versions are recorded in `uv.lock`.

## Setup

### 1. Install uv

**macOS / Linux**
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**Windows (PowerShell)**
```powershell
irm https://astral.sh/uv/install.ps1 | iex
```

### 2. Install dependencies (Once repo has been cloned)

```bash
uv sync --locked
```

This automatically installs the required Python version if necessary, creates a virtual environment (`.venv`), and installs the locked dependencies.

### 3.  Select VS Code Interpreter

Open the Command Palette `Mac: Cmd+Shift+P`, `Windows: Ctrl+Shift+P`.
Select `Python: Select Interpreter`.
Select `repo_name (3.13.x) ./.venv/bin/python`.

### 4. Run Python

```bash
uv run python
```

*or*

```
Run Python File (the play button in VS Code)
```

## Managing Dependencies

**Add a dependency:**
```bash
uv add <package>
```

**Remove a dependency:**
```bash
uv remove <package>
```

**Synchronize with the shared environment:**
```bash
git pull
uv sync --locked
```

When changing dependencies, commit both `pyproject.toml` and `uv.lock` to keep the team's environments consistent.
