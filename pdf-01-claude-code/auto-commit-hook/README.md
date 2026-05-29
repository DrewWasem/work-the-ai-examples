# Auto-Commit Stop Hook

Drop a `.claude/settings.json` at your project root that auto-commits after every Claude Code session. Every run becomes a save point you can roll back from.

## Install

```bash
cp -r .claude /path/to/your/project/
cd /path/to/your/project
git init       # if not already a git repo
```

That's it. The hook fires on Claude Code's Stop event. If there are changes, it commits them with a timestamp. If there aren't, it does nothing.

## What the hook does

```bash
git add -A && (git diff --cached --quiet || git commit -m "auto: <timestamp>")
```

`git diff --cached --quiet` exits non-zero when there are staged changes, so the commit only runs when there's something to commit. The `|| true` keeps the session from erroring if the commit fails for any reason.
