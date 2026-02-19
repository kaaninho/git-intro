# Git Cheat Sheet

## Repository einrichten

```bash
git init                    # Neues Repo erstellen
git clone <url>             # Repo klonen
```

## Status & History

```bash
git status                  # Änderungen anzeigen
git log                     # Kompakte Commit-History
git diff                    # Unstaged Änderungen zeigen
```

## Staging & Commits

```bash
git add <datei>             # Datei stagen
git add .                   # Alles stagen
git commit -m "Nachricht"   # Commit erstellen
git commit --amend          # Letzten Commit bearbeiten
```

## Branches

```bash
git branch                  # Branches auflisten
git branch <name>           # Branch erstellen
git switch <name>           # Branch wechseln
git switch -c <name>        # Branch erstellen & wechseln
git merge <branch>          # Branch mergen
git branch -d <name>        # Branch löschen
```

## Remote

```bash
git fetch                   # Änderungen holen (kein merge)
git pull                    # Fetch + Merge
git push origin <branch>    # Branch pushen
```

## Rückgängig machen

```bash
git restore <datei>         # Unstaged Änderungen verwerfen
git restore --staged <datei># Datei unstagen
git reset --hard HEAD~1     # Letzten Commit entfernen ⚠️
```

## Stash

```bash
git stash                   # Änderungen zwischenspeichern
git stash pop               # Stash wiederherstellen
git stash list              # Alle Stashes anzeigen
```
