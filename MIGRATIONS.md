# Migrationsanleitungen

Wenn diese Vorlage auf eine neue **Major-Version** gehoben wird (z. B. `0.x.x` → `1.0.0`), beschreibt dieser Abschnitt, was bestehende Möbel-Repos tun müssen, um auf die neue Vorlagen-Version umzustellen.

Bestehende Repos werden nicht automatisch migriert – Stabilität geht vor.

## Reihenfolge bei einer Migration

1. Im Möbel-Repo einen Branch `migration-template-x.y.z` anlegen.
2. Diesem Dokument folgen.
3. Lokale Validierung laufen lassen (siehe `validate.yml`).
4. Im Möbel-Repo `heimeliq.toml` → `heimeliq-template-version` auf neue Version setzen.
5. Eintrag in `changelog.md` (klein, im Möbel-Repo) ergänzen.
6. Branch mergen, neuen SemVer-Tag setzen.

---

## 0.x → 1.0 (noch nicht erschienen)

*Wird ergänzt, sobald die erste Major-Version veröffentlicht wird.*
