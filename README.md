# ORBWEVA Pitch Night

A Claude Code skill for building and rehearsing a short (2–5 minute) spoken startup pitch for a **cross-cultural, international-readiness audience** — demo nights, pitch competitions, and accelerator showcases where the judges may not know your home market.

This is not an investor deck. It's the 3 minutes you say out loud, written to make a foreign judge picture your customer, problem, and market without local knowledge.

## Install

> ⚠️ **The folder MUST end up inside `~/.claude/skills/`.** Claude Code only loads skills from there. If you clone it anywhere else (e.g. your home folder or Desktop), the skill will **not** appear and `/pitch-night:help` will do nothing.

**Mac / Linux (Terminal):**

```bash
git clone https://github.com/ORBWEVA/pitch-night.git ~/.claude/skills/pitch-night
```

**Windows (PowerShell):**

```powershell
git clone https://github.com/ORBWEVA/pitch-night.git $HOME\.claude\skills\pitch-night
```

Then **fully close and reopen Claude Code**, and run `/pitch-night:help`.

(Or install the full ORBWEVA Academy pack: `curl -fsSL https://orbweva.com/install-skills.sh | bash`.)

### Troubleshooting

- **Cloned it to the wrong place?** Delete that copy and re-clone into the path above. On Windows, from your home folder (`cd ~`): `Remove-Item -Recurse -Force pitch-night` then re-run the clone command. On Mac/Linux: `rm -rf ~/pitch-night` then re-run.
- **`git` not recognized (Windows)?** Install Git first: https://git-scm.com/download/win — then close and reopen PowerShell.
- **Don't paste the URL on its own.** `git clone` must come first; pasting just the address makes the terminal try to run it as a program and fail.

## Commands

| Command | What it does |
|---------|-------------|
| `/pitch-night:build` | Build the 3-minute spoken script, budgeted second-by-second |
| `/pitch-night:translate` | Make your home market legible to judges who don't know it |
| `/pitch-night:rehearse` | Timing and delivery checklist against the clock |
| `/pitch-night:score` | Self-score against the judging rubric |
| `/pitch-night:help` | Command reference |

For an investor fundraising deck (10–15 slides, financial model, VC objection prep), use the `founder-pitch` skill instead.

## License

Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0). © 2026 ORBWEVA.
