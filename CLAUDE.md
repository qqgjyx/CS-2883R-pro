# CS-2883R-pro: final project workspace

Experiments and code for the CS 2883R final project, "Sampling Dependence in DriftNeRF's Density
Consensus", by Juntang Wang and Ciro Zhang.

## Where things live

| What | Where |
| --- | --- |
| Experiments, code (this repo) | `qqgjyx/CS-2883R-pro`, checked out at `.../2026FA/CS-2883R/2026-12-04_PRO` |
| Paper (report, Overleaf-synced) | `qqgjyx/overleaf_CS-2883R-pro`, checked out at `.../Documents/_Paper/overleaf_CS-2883R-pro` |
| Course repo (parent) | `qqgjyx/CS-2883R`; do not edit it from here |
| Proposal (final, handed in 30 Oct) | `doc/proposal.pdf`, source `doc/proposal.tex` |
| Course rules for the project | `doc/project_guidelines.md` |
| DriftNeRF, the method we extend | paper arXiv 2610.29106; code `Q9gJYx/DriftNeRF`; paper source `qqgjyx/overleaf_DriftNeRF` |

The two `-pro` names differ only by the `overleaf_` prefix. Paper work goes in the Overleaf repo,
code and results here. Figures and tables for the paper are produced here and copied over.

## Deadlines

- Presentation: Wed 2 Dec 2026, in class
- Report: Fri 4 Dec 2026, 11:59 p.m. ET. Four pages in the ACM template, references excluded;
  contributions and AI usage may run past page four

## This repo is a git submodule: work around it every time

CS-2883R pins this repo as the submodule `2026-12-04_PRO`. Submodule checkouts fall back to a
detached HEAD whenever the parent runs `git submodule update`, and commits made there can be lost.

- Start every session with `git status -sb`. If it says `HEAD (no branch)`, run
  `git switch main && git pull --ff-only` before touching anything.
- Never run `git submodule update` from the parent without `--remote --merge`.
- Do not commit the parent's pin from here. When a milestone lands, tell Juntang; the CS-2883R
  session bumps the pin.

## OneDrive

This checkout lives in OneDrive. Keep large or regenerable files (datasets, checkpoints, run logs)
in the git-ignored `data/`, `outputs/`, `checkpoints/`, `runs/`, or on a compute host
(`~/.claude/memory/compute-hosts.md`). Commit code, configs and small result tables only.

## Conventions

- Python ML repo: apply the `minimal-python-ml-repos` skill (src layout, no reinvented wheels,
  `notebooks/00_eda.ipynb`, `01_train.ipynb`, `02_eval.ipynb`).
- Every claim about DriftNeRF or prior work is checked against the source before it reaches the
  paper.
- Course AI policy (`doc/project_guidelines.md`): ideas and the first draft of written
  submissions must be the authors'; AI may help brainstorm, implement and polish, and every use is
  acknowledged in the report. Ask Juntang before drafting report prose.
- Git: branch, PR, squash-merge; ask before committing or pushing. Ciro has access to this repo.
