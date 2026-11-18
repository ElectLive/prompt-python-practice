# prompt-python-practice

Practice repository for the book **"프롬프트로 배우는 파이썬"** (Learning Python by Prompting).
In the book's chapter 15 you fork this repository, send a pull request (PR), and review a PR that someone else wrote.
Readers of the Korean, Japanese and English editions share it, so everything here is in English.

## What is in it

| Path | What it is |
|---|---|
| `sales.py` | A small program that adds up sales by month from a CSV file |
| `data/sample.csv` | A few rows of sample sales data |
| `tests/test_sales.py` | Tests for `sales.py` |
| `.github/workflows/tests.yml` | Runs `uv run pytest` on every push and every PR |
| `CONTRIBUTING.md` | How to send a practice PR. Read it before you start |

## Run it

You need [uv](https://docs.astral.sh/uv/). From the repository folder:

```
uv run sales.py data/sample.csv
uv run pytest
```

## How practice PRs are handled

1. Pick an issue labelled `exercise`.
2. Send a PR in the order described in `CONTRIBUTING.md`.
3. The automated tests run first. A PR whose tests fail is not reviewed until they pass.
4. Then the author of the book reviews the PR.

Please keep in mind:

- **Many readers do the same exercise.** The issues stay open on purpose, and `main` is kept as it is,
  so the next reader finds the same starting point. Do not worry if you see other PRs for the same issue.
- **A practice PR may be closed after review instead of merged.** Being closed does not mean your PR was wrong.
  Read the review comments; they are the result of the exercise.
- **Do not put personal data in a PR**: no real names of other people, addresses, phone numbers, passwords,
  API keys, or real sales data. Use the sample data in this repository.

The PR labelled `do not merge` and `review practice` is for the review exercise in chapter 15. Review it; do not copy it.

## License

MIT. See `LICENSE`.
