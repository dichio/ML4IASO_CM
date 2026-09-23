# Project instructions for Claude Code

## Scope & autonomy
- This is a graduate course-design project ("Foundations of Machine Learning").
  Work independently within the project directory: don't ask before routine
  actions (creating scripts, running them, generating data/figures, fixing
  bugs). Do ask before anything destructive or structural (see below).
- Treat `_materials/` subfolders (leading underscore) as scratch/working
  space, consistent with the project's `.gitignore` — code, data, and
  generated figures for a given lecture live under
  `<lecture folder>/_materials/{data,figures,code}` unless told otherwise.

## Before deleting or overwriting
- **Always ask before deleting any file**, in this project or elsewhere on
  disk. No exceptions for files that look temporary or generated.
- Prefer not to silently overwrite existing data/figure files either —
  if a script would regenerate output that already exists, flag it and
  confirm, or write to a new filename, rather than overwriting by default.

## Figures
- All figures use **physical axes/figure size specified in centimeters**,
  not inches or default matplotlib units — convert internally
  (1 inch = 2.54 cm) but the parameter exposed to me should be in cm, since
  these are placed at fixed sizes in slides.
- Keep a single shared plotting-style helper (e.g. `_materials/code/plot_style.py`
  or similar, reused across scripts) for figure size, font size, and color
  palette, rather than each script reinventing its own — so all lecture
  figures look consistent with each other.
- Default to a consistent, colorblind-safe palette across the course, and
  keep font sizes large enough to be legible on a projected slide, not just
  on screen.

## Notation
- Variable names in code, and labels/legends in figures, should follow the
  conventions in `notations.md` (e.g. `n` observations, `p` features,
  bold for vectors, capital non-bold for random variables in any math
  rendered on a figure). Flag it if a script's natural variable names would
  conflict with this and ask how to resolve it, rather than silently picking
  one convention.

## Reproducibility
- Any script involving randomness must expose a `random_seed` parameter and
  use it consistently — no unseeded randomness in anything meant to produce
  a stable teaching figure.
- Data-generating scripts should be self-contained and rerunnable: running
  them again with the same parameters should reproduce identical output.

## Code style
- Python, with clear docstrings and inline comments — this is teaching
  material, and should be readable by a human (me, or a TA) without
  needing to reverse-engineer intent from the code alone.
- Keep dependencies to the standard scientific stack (numpy, pandas,
  matplotlib, scipy) unless I explicitly approve something else.
- Prefer small, single-purpose scripts over a shared framework/library,
  unless I ask for the latter — this project favors many simple, legible
  scripts over one clever general-purpose one.

## Version control (if/when used)
- Don't `git commit` or `git push` without asking first, even if the
  change seems minor.
