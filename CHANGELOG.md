# Changelog – heimeliQ Furniture Template

Versionierung folgt [Semantic Versioning](https://semver.org/lang/de/).

- **MAJOR** (`x.0.0`): Breaking Change. Bestehende Möbel-Repos brauchen Migration.
- **MINOR** (`0.x.0`): Neues optionales Feld oder Ordner. Bestehende Repos funktionieren weiter.
- **PATCH** (`0.0.x`): Tippfehler, Klarstellungen, Bug-Fixes, kein strukturelles Update.

## [0.1.1] – TOML-Reihenfolge-Bugfix in `okh.toml`

Behebt einen latenten Bug in der Beispiel-`okh.toml`: Einige Top-Level-Felder (`mass`, `manufacturing-instructions`, `bom`, `readme`) standen nach Section-Headern und wurden dadurch laut TOML-Spezifikation als Sub-Felder dieser Sections interpretiert. Dasselbe galt für `[part.outer-dimensions]`, das bei mehreren `[[part]]`-Einträgen mehrdeutig wird.

**Behoben:**

- Alle Top-Level-Felder stehen jetzt vor der ersten Section.
- `outer-dimensions` innerhalb `[[part]]` wird als Inline-Table notiert (`outer-dimensions = { width = 0, depth = 0, height = 0 }`), was bei mehreren Bauteilen eindeutig bleibt.
- Erklärender Kommentar zur TOML-Reihenfolge in der Datei ergänzt.

**Migration:** Bestehende Möbel-Repos sollten ihre `okh.toml` auf dieselbe Reihenfolge umstellen. Da das Original-Manifest in den meisten Fällen noch keine echten Werte enthält, ist die Migration trivial. Eine sauber durchlaufende `validate.yml` zeigt an, dass alles passt.

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
