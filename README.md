# Sigma QuickStarts

Sample code and assets for the [Sigma QuickStarts](https://quickstarts.sigmacomputing.com/). Each folder belongs to one or more QuickStarts, which explain how to use it.

**IMPORTANT:**
This repository's contents are not intended for use in a production environment.

We make no guarantees regarding the reliability, safety, or suitability of this code for production purposes.

Users are cautioned to use the code at their own discretion and risk.

## Configuration files

Projects that need credentials include a `.env.example` file with empty values. Copy it to `.env` in the same folder, then add your own values:

```
cp .env.example .env
```

`.env` files are listed in `.gitignore`. Never commit credentials, tokens or other secrets to this repository.

## Secret scanning

Every pull request, every push to `main` and a weekly scheduled run scan the full history and the current files with [Betterleaks](https://github.com/betterleaks/betterleaks), using the rules in `.betterleaks.toml`. The workflow also fails if any `.env` file is committed.

Contributors should also scan their changes before each commit with the pre-commit hook:

```
pip install pre-commit
pre-commit install
```
