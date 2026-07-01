# ORBWEVA Pitch Night

A Claude Code skill for building and rehearsing a short (2–5 minute) spoken startup pitch for a **cross-cultural, international-readiness audience** — demo nights, pitch competitions, and accelerator showcases where the judges may not know your home market.

This is not an investor deck. It's the 3 minutes you say out loud, written to make a foreign judge picture your customer, problem, and market without local knowledge.

## Install

### Recommended: the ORBWEVA Academy installer

```bash
npx @orbweva/academy@latest
```

This places the skill **and** its slash-commands in the right folders automatically (pitch-night ships in the accelerator, mentoring, and founder tracks, and the full pack). Node 18+ and `git` are the only prerequisites. Then fully close and reopen Claude Code.

### Standalone (just this skill)

pitch-night is a Claude Code **skill + slash-commands**, and Claude Code loads those from two *separate* folders — skills from `~/.claude/skills/`, slash-commands from `~/.claude/commands/`. A plain `git clone` into one location wires up neither correctly, so clone once and copy each part into place.

**Mac / Linux (Terminal):**

```bash
git clone --depth 1 https://github.com/ORBWEVA/pitch-night.git /tmp/pitch-night
mkdir -p ~/.claude/skills ~/.claude/commands
cp -R /tmp/pitch-night/skills/pitch-night   ~/.claude/skills/pitch-night
cp -R /tmp/pitch-night/commands/pitch-night ~/.claude/commands/pitch-night
rm -rf /tmp/pitch-night
```

**Windows (PowerShell):**

```powershell
git clone --depth 1 https://github.com/ORBWEVA/pitch-night.git $env:TEMP\pitch-night
New-Item -ItemType Directory -Force -Path $HOME\.claude\skills, $HOME\.claude\commands | Out-Null
Copy-Item -Recurse -Force $env:TEMP\pitch-night\skills\pitch-night   $HOME\.claude\skills\pitch-night
Copy-Item -Recurse -Force $env:TEMP\pitch-night\commands\pitch-night $HOME\.claude\commands\pitch-night
Remove-Item -Recurse -Force $env:TEMP\pitch-night
```

Then **fully close and reopen Claude Code**, and run `/pitch-night:help`.

### Troubleshooting

- **`/pitch-night:*` commands don't appear?** The commands live in `~/.claude/commands/pitch-night/` — confirm that folder exists and holds `build.md`, `score.md`, etc. If you only cloned into `~/.claude/skills/`, you skipped the commands copy above (the skill loads but its slash-commands won't). Re-run the standalone steps, or use the `npx` installer, then restart Claude Code.
- **Don't use `/plugin install`.** On some Windows builds it fails with `Command 'git' not found or is in an unsafe location (current directory)` even though `git --version` works — a Node/Windows quirk in how that command spawns git, not a broken git install. The install steps above don't need it.
- **`git` not recognized (Windows)?** Install Git first: https://git-scm.com/download/win — then close and reopen PowerShell.
- **Don't paste a URL on its own.** `git clone` must come first; pasting just the address makes the terminal try to run it as a program and fail.

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
