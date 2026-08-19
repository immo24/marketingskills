# Hinweise zu diesem Fork

Fork von [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills), angelegt am 19.08.2026 als Sicherung fuer den Coder-Workspace.

Alle 49 Skills liegen unveraendert im Repo. Abweichung vom Original sind nur zwei Manifest-Dateien: In `.claude-plugin/marketplace.json` (Plugin-Eintrag) und in `.claude-plugin/plugin.json` ist die Liste `skills` auf 14 Pfade gekuerzt, das Website-Paket:

seo-audit, ai-seo, schema, site-architecture, content-strategy, copywriting, copy-editing, cro, analytics, signup, popups, lead-magnets, social, public-relations

Grund: Alle 49 Beschreibungen zusammen kosten rund 13.000 Token in jeder Sitzung, auch bei Arbeiten ohne Marketingbezug. Das Website-Paket liegt bei rund 3.600.

Wichtig: Massgeblich ist die Liste im **Plugin-Eintrag der `marketplace.json`**. Fehlt sie dort, laedt Claude Code jeden Unterordner von `skills/` automatisch, und die Liste in `plugin.json` allein aendert daran nichts (am 19.08.2026 gemessen: 49 statt 14).

Weitere Skills freischalten: Pfad in beiden Manifesten ergaenzen, pushen, dann `claude plugin marketplace update marketingskills` und das Plugin neu installieren (ein blosses `plugin update` zieht nur bei geaenderter Versionsnummer).

Abgleich mit dem Original: `gh repo sync immo24/marketingskills`. Konflikte sind nur in den beiden Manifest-Dateien zu erwarten. Neue Skills des Anbieters werden nicht automatisch geladen, sie muessen bewusst in die Listen aufgenommen werden.
