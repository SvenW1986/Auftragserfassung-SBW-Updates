# Erstbefüllung des leeren GitHub-Repositories

Repository-Name:

```text
Auftragserfassung-SBW-Updates
```

GitHub:

```text
SvenW1986/Auftragserfassung-SBW-Updates
```

## Variante mit Git lokal

Im entpackten Ordner ausführen:

```bash
git init
git branch -M main
git add .
git commit -m "Initiales Update-Repository fuer SBW Auftragserfassung"
git remote add origin https://github.com/SvenW1986/Auftragserfassung-SBW-Updates.git
git push -u origin main

git tag v0.3.27
git push origin v0.3.27
```

Danach sollte GitHub Actions automatisch den Release `v0.3.27` erstellen.

## Variante ohne Git lokal

1. ZIP entpacken.
2. Den Inhalt in das leere GitHub-Repository hochladen.
3. Danach einen Tag `v0.3.27` erstellen, damit die GitHub Action den Release baut.
