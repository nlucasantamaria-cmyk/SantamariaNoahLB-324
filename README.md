# SantamariaNoahLB-324

## Pre-Commit Hooks

In diesem Projekt werden Pre-Commit Hooks verwendet, um die Codequalität automatisch zu überprüfen.

Beim Commit wird der Python-Code automatisch mit Black formatiert.

Beim Push werden die automatisierten Tests mit pytest ausgeführt. Ein Push kann somit nur erfolgreich durchgeführt werden, wenn die Tests ausgeführt werden können.

### Installation

Zuerst müssen die benötigten Python-Abhängigkeiten installiert werden:

```bash
pip install -r requirements.txt
```

Danach wird `pre-commit` installiert:

```bash
pip install pre-commit
```

### Hooks installieren

Der Pre-Commit-Hook wird mit folgendem Befehl installiert:

```bash
pre-commit install
```

Der Pre-Push-Hook wird zusätzlich mit folgendem Befehl installiert:

```bash
pre-commit install --hook-type pre-push
```

### Hooks manuell testen

Der Pre-Commit-Hook kann mit folgendem Befehl für alle Dateien getestet werden:

```bash
pre-commit run --all-files
```

Der Pre-Push-Hook kann mit folgendem Befehl getestet werden:

```bash
pre-commit run --hook-stage pre-push --all-files
```

### Verhalten der Hooks

- Pre-Commit: Black überprüft und formatiert den Python-Code automatisch.
- Pre-Push: pytest führt die vorhandenen automatisierten Tests aus.
