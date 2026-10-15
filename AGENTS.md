# Project constitution

This file tells coding agents (Claude Code, Codex, Cursor, …) what this project is about and which rules apply. It is read at the start of every agent session. **Fill in the parts in brackets as a team in week 3 and keep the file up to date.**

## Goal

Forecast the daily turnover of a bakery branch in Kiel for six product groups (bread, rolls, croissants, confectionery, cakes, seasonal bread), so that the bakery can plan its daily production. Forecast quality is measured with the MAPE per product group on the test period 01.08.2018 – 31.07.2019 (Kaggle competition of the course).

## Team

[Names and who is responsible for what, e.g. data preparation, baseline model, neural network, presentation.]

## Client and audiences

- **Client:** the operations manager of the bakery. She decides every afternoon how much is baked for the next day. She is not a data scientist and needs clear recommendations without jargon.
- **Technical audience:** a data team that would take over this repository. The READMEs must allow them to reproduce all results.

## Data

- Sales, weather and Kiel Week data: see the [dataset documentation](https://github.com/opencampus-sh/intro-to-data-science-and-ml/blob/main/data/bakery/README.md). Load the files from `https://raw.githubusercontent.com/opencampus-sh/intro-to-data-science-and-ml/main/data/bakery/`.
- Additional data sources: [list them with link and the variables created from them]

## Conventions

- Environment: managed with **uv**. Install with `uv sync`; add packages only with `uv add <package>` (never `pip install`), and commit `pyproject.toml` and `uv.lock`.
- Work in Jupyter notebooks in the folder of the respective project step (`0_DataPreparation`, `1_DatasetCharacteristics`, `2_BaselineModel`, `3_Model`). Notebooks must run from top to bottom without errors.
- Every notebook starts with a short markdown cell explaining its purpose; important steps are explained in plain language.
- Weekdays are ordered Monday to Sunday, never alphabetically.
- [Further team conventions, e.g. naming of files and variables]

## Checks

Results are only committed if these checks pass:

- Merges with weather, Kiel Week or other data do not change the number of rows of the sales data, and every combination of date and product group occurs only once.
- The data is split by date: training 01.07.2013 – 31.07.2017, validation 01.08.2017 – 31.07.2018, test from the Kaggle file. No training date lies after the start of the validation period.
- Only information that is known the day before the forecast is used as a feature (no data leakage).
- Predictions for Kaggle contain exactly the IDs of the Kaggle test file.
- Model quality is always reported on validation data, next to the training score, and per product group.
- [Further checks the team agrees on]

## How the agent should work

- Explain what you do in plain language and name the concept behind it. Many team members are not programmers.
- State your plan before you change code, and point out what we should check in the results.
- Never invent results: run the code and report what it actually returns.
- Only work inside this repository. Ask before deleting files, installing software outside the project environment or pushing to GitHub.
- Never write passwords, API keys or personal data into files.
