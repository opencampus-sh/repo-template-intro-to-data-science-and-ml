# Project constitution

This file tells coding agents (Claude Code, Codex, Cursor, …) what this project is about and which rules apply. It is read at the start of every agent session. The course infrastructure below is filled in. Your team adds the rest in week 3: `/setup-ds-project` adds a section that points to your canvas, glossary and decision log, and `/grill-question` fills the canvas.

## Team

[Names and who is responsible for what, e.g. data preparation, baseline model, neural network, presentation.]

## Data

- Sales, weather and Kiel Week data: see the [dataset documentation](https://github.com/opencampus-sh/intro-to-data-science-and-ml/blob/main/data/bakery/README.md). Load the files from `https://raw.githubusercontent.com/opencampus-sh/intro-to-data-science-and-ml/main/data/bakery/`.
- Additional data sources: [list them with link and the variables created from them]

## Conventions

- Environment: managed with **uv**. Install with `uv sync`; add packages only with `uv add <package>` (never `pip install`), and commit `pyproject.toml` and `uv.lock`.
- Work in Jupyter notebooks in the folder of the respective project step (`0_DataPreparation`, `1_DatasetCharacteristics`, `2_BaselineModel`, `3_Model`). Notebooks must run from top to bottom without errors.
- Every notebook starts with a short markdown cell explaining its purpose; important steps are explained in plain language.
- Weekdays are ordered Monday to Sunday, never alphabetically.
- [Further team conventions, e.g. naming of files and variables]

## How the agent should work

- Explain what you do in plain language and name the concept behind it. Many team members are not programmers.
- State your plan before you change code, and point out what we should check in the results.
- Never invent results: run the code and report what it actually returns.
- Questions about the decision, the audiences, what counts as success, what is known in advance, how to split the data and which checks to run are the team’s to decide. If the canvas or the decision log does not settle them yet, ask; do not decide them yourself.
- Only work inside this repository. Ask before deleting files, installing software outside the project environment or pushing to GitHub.
- Never write passwords, API keys or personal data into files.
