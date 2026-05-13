# Changelog – heimeliQ Furniture Template

Versionierung folgt [Semantic Versioning](https://semver.org/lang/de/).

- **MAJOR** (`x.0.0`): Breaking Change. Bestehende Möbel-Repos brauchen Migration.
- **MINOR** (`0.x.0`): Neues optionales Feld oder Ordner. Bestehende Repos funktionieren weiter.
- **PATCH** (`0.0.x`): Tippfehler, Klarstellungen, kein strukturelles Update.

## [0.1.0] – initial

- Erste Version des Templates.
- OKH 2.4 als Standard für Möbel-Metadaten.
- **Lizenz-Trennung**: Template selbst unter MIT, daraus erzeugte Möbel-Repos unter CERN-OHL-S-2.0.
- `LICENSE.example` und `README.example.md` als Vorlagen, die im Möbel-Repo zu `LICENSE` bzw. `README.md` umbenannt werden.
- Doku-Struktur unter `docs/de/` mit co-located `.images/`-Ordnern.
- `heimeliq.toml` für projektspezifische Erweiterungen (Reihen, IDs, externe Teile).
- `heimeliq.schema.json` für strenge Validierung.
- GitHub-Action `validate.yml` mit Erkennung Template-Repo vs. Möbel-Repo und kontextabhängigen Checks.
- REUSE-konforme Datei-Lizenzangaben.
