# To Review — Files Deleted in the Reorg

**This folder is temporary.** It exists so these files can be reviewed before
the reorganization is finalized. Once each item below is dispositioned, delete
this entire folder in a single commit.

These 8 files existed on `master` but were deleted on the `reorg` branch. They
were restored here from commit `1fd0f133` (the point where `reorg` diverged),
so they are at their last known-good state.

Folder `README.md` navigation stubs from the old layout were *not* restored —
those described directories the reorg intentionally eliminated.

## What's here

### Published PDFs — 4 unique documents

| Document | Size | Decision |
|---|---|---|
| `IHE_PCD_Suppl_POU.pdf` | 1.1 MB | ? |
| `IHE_PCD_TF_Vol1 2019-12-12.pdf` | 1.2 MB | ? |
| `IHE_PCD_TF_Vol2 2019-12-12.pdf` | 4.4 MB | ? |
| `IHE_PCD_TF_Vol3 2019-12-12.pdf` | 1.1 MB | ? |

**Note:** the three `TF_Vol*` PDFs appear twice below — under `Current Published/`
and under `TF Final Text Versions/Rev_9.0 2019/`. Both copies are **byte-identical**.
Master stored the same documents in two places; only one copy needs to survive.

**Why this matters:** `reorg` preserved the Rev_9.0 `.docx` sources at
`Technical Frameworks/archived docx/Rev_9.0 2019/`, but not these PDFs. A `.docx`
source is not a substitute for a published PDF — the PDF is the artifact that was
actually balloted and distributed. Decide deliberately whether the published
renderings should be retained.

### `notes.md`

A to-do list of process questions (branch/PR/repo-creation documentation, master
branch protection). Most have since been answered by the playbooks and governance
docs in `DEV.documentation`. Likely safe to drop, but confirm nothing here is
still outstanding — the branch-protection question in particular is still open
(`master` on this repo currently has no protection).

## Dispositions

For each item: **keep** (move to its home in the new layout), or **drop**
(delete — it stays recoverable in git history at `1fd0f133`).

Suggested homes if keeping:
- Published PDFs → alongside their `.docx` sources in
  `Technical Frameworks/archived docx/Rev_9.0 2019/`, or a new
  `Technical Frameworks/Published/`
- `notes.md` → fold any live questions into `DEV.tooling/questions.md`
