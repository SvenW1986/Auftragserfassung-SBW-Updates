# SBW Auftragserfassung – Update-Repository

Dieses Repository dient ausschließlich zur Bereitstellung öffentlicher Update-Bundles für die **SBW Auftragserfassungs-App**.

Feste Updatequelle in der App:

```text
SvenW1986/Auftragserfassung-SBW-Updates
```

## Struktur

```text
.github/workflows/release.yml
Releases/SBW_Auftragserfassung_UpdateBundle_<version>.zip
README.md
.gitignore
```

## Update veröffentlichen

1. Neues UpdateBundle in `Releases/` ablegen.
2. Änderungen committen und pushen.
3. Git-Tag passend zur Version erstellen, zum Beispiel:

```bash
git tag v0.3.27
git push origin v0.3.27
```

4. GitHub Actions erstellt automatisch einen Release und hängt das passende Bundle an.

## Wichtig

Die Bundle-ZIP wird **nicht entpackt**.

Namensschema:

```text
SBW_Auftragserfassung_UpdateBundle_0.3.xx.zip
```

Die App prüft später:
- Produktcode
- Version
- Mindest-/Maximalversion
- SHA-256
- Signatur des enthaltenen `.sbwupdate`
