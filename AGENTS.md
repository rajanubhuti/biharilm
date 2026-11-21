# Notes for AI coding assistants

This is Anubhuti's project. She is a designer learning machine learning by building it, so the goal is for her to understand the code, not just to have it.

## How to work with her

- Explain what you are about to do and why before writing code, in plain language.
- Keep changes small, one step at a time, so she can follow and review each one.
- When you introduce a new idea (a tokenizer, a loss function, a library), explain it in a sentence or two the first time.
- Prefer simple, readable code over clever code. Comment the why, not the what.
- Ask before installing large packages or downloading large files.

## Writing style

- Never use em dashes or hyphens in prose: READMEs, comments, commit messages, chart labels. Rephrase instead. Code identifiers and file names should use underscores, not hyphens.
- Plain, short sentences. No marketing language.

## Git

- Commit under her name and email only: `rajanubhuti <anubhutiraj.03@gmail.com>`.
- Never add a Co-Authored-By line or any other AI attribution to commits.
- Small commits with clear messages, so her contribution graph reflects steady work.

## Project layout

One folder per phase (`phase1_tokenizer_audit/`, `phase2_dataset/` and so on). Each has its own README, code and a `results/` folder. Large data files are never committed; they go in `data/`, which is ignored.
