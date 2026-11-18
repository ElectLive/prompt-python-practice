# Contributing

This repository is for practice. Thank you for sending a PR; please read this page first.

## The flow

1. **Fork** this repository to your GitHub account: `gh repo fork crowdy/prompt-python-practice --clone=false`
2. **Clone** your fork (check that the URL has your account name) and move into it: `git clone <your fork's URL>`, then `cd prompt-python-practice`
3. **Branch**: make a new branch for the issue, for example `git switch -c add-test-same-month`.
   Do not work on `main`.

## The fixed order

Every change follows the same order. Do not skip a step because the change is small.

1. **Test**: write or change the test for your change.
   A change that does not change behavior (documentation, comments) needs no new test: start from step 2.
2. **`uv run pytest`**: run all the tests on your computer and read the result.
3. **Commit**: one commit for one change, with a message that says what changed.
4. **Push**: `git push -u origin <your branch>`
5. **PR**: open a PR from your branch to `main` of this repository.

## When the tests run

- In your fork, GitHub Actions is off by default, so pushing to your fork does not run the tests. Run `uv run pytest` yourself (step 2).
- Until a PR of yours has been merged here, the tests start only after the maintainer approves the run. Until then the PR shows that the run is
  waiting for approval. A run not approved within 30 days expires. Most practice PRs are closed rather than merged,
  so most readers go through this approval. (GitHub Docs: "Managing GitHub Actions settings for a repository",
  "Approving workflow runs from forks".)

## Keep the PR small

- One PR for one issue. Do not fix other things you noticed in the same PR; open an issue for them instead.
- Change only the files the issue needs.

## The PR description

The PR template asks four things. Fill in all of them.

| Section | What to write |
|---|---|
| What | The files you changed and what you changed in them |
| Why | The issue number, and how your change solves it |
| How I verified | The commands you ran (for example `uv run pytest`) and their output. If you added a test for a bug, say that it failed before the fix |
| AI use | See below |

### Disclosing AI use

AI tools are allowed here. If you used one, say so in the PR description:

- the tool and its version (for example Claude Code 2.1.325),
- what you asked it to do,
- what you did yourself (which lines you read, which commands you ran).

If you did not use an AI tool, write "None".

## You must understand your change

You are responsible for every line in your PR, whoever or whatever wrote it.
Before you open the PR, make sure you can explain each changed line in one sentence.
The reviewer may ask "what does this line do?" — answer in your own words.
Do not send code you do not understand.

## Do not edit the workflow

Do not change `.github/workflows/tests.yml` or add other workflow files. A PR that changes them is closed without review.
The tests are the first judge of every PR, so they have to be the same for everyone.

## Be kind in reviews

Whether you are reviewing or being reviewed, be kind. Comment on the code, not the person.
Say what you saw and why it matters, and assume the other person is learning too — everyone here is.
