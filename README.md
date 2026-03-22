# team_test

Local playground for learning and testing **ClawTeam**.

## Prerequisites

- Python 3.10+
- (Recommended) `uv` or `pip`

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -U pip

# If you want to use ClawTeam from a local checkout (example):
# pip install -e /path/to/ClawTeam

# Or install from PyPI (if published):
# pip install clawteam
```

## Quick Start

```bash
# list commands
clawteam --help

# create a team
clawteam team spawn-team calculator-team --agent-name likang13 --description "Build a simple calculator"

# create tasks
clawteam task create calculator-team "Implement add(a, b) function" --description "Create calculator.py with add function" --priority high
clawteam task create calculator-team "Implement multiply(a, b) function" --description "Add multiply function to calculator.py" --blocked-by abc123 --priority medium

# list tasks
clawteam task list calculator-team

# pause-like behavior (block/unblock)
clawteam task update calculator-team 3805cd65 --status blocked
clawteam task update calculator-team 3805cd65 --status pending

# delete team and all data
clawteam team cleanup calculator-team
```

## Docs

- `ClawTeam-Tutorial.md`
