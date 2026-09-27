# Verifica Regole .gitignore

## Output di `git status`
```text
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   .gitignore

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	M0_ambiente/autenticazione.md
	M0_ambiente/cronologia.md
	M0_ambiente/gitignore_verifica.md

nothing added to commit but untracked files present (use "git add" to track)
```

## Output di `git check-ignore -v M0_ambiente/.venv/pyvenv.cfg`
```text
.gitignore:7:.venv/    M0_ambiente/.venv/pyvenv.cfg
```
