# Hinweise zu diesem Fork

Fork von [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills), angelegt am 19.08.2026 als Sicherung fuer den Coder-Workspace.

Alle 49 Skills liegen unveraendert im Repo, allerdings im Ordner `skills-all/` statt `skills/`. Abweichung vom Original: In `.claude-plugin/plugin.json` ist die Liste `skills` von `./skills` (alle) auf 14 Pfade gekuerzt, das Website-Paket:

seo-audit, ai-seo, schema, site-architecture, content-strategy, copywriting, copy-editing, cro, analytics, signup, popups, lead-magnets, social, public-relations

Grund: Alle 49 Beschreibungen zusammen kosten rund 8.700 Token in jeder Sitzung, auch bei Arbeiten ohne Marketingbezug. Das Website-Paket liegt bei rund 2.500.

Weitere Skills freischalten: Pfad in `.claude-plugin/plugin.json` ergaenzen, pushen, dann `claude plugin marketplace update marketingskills` und das Plugin neu installieren (ein blosses `plugin update` zieht nur bei geaenderter Versionsnummer).

Abgleich mit dem Original: `gh repo sync immo24/marketingskills`. Konflikte sind nur in `.claude-plugin/plugin.json` zu erwarten.

## Warum der Ordner umbenannt ist

Claude Code laedt jeden Unterordner von `skills/` automatisch, zusaetzlich zu den in `plugin.json` aufgezaehlten Pfaden. Die Auswahl wirkt deshalb nur, wenn der Ordner anders heisst. Gemessen: mit `skills/` werden 49 Skills geladen (rund 13.000 Token je Sitzung), mit `skills-all/` genau die 14 aufgezaehlten (rund 2.500).

Beim naechsten `gh repo sync` landen neu hinzugekommene Skills des Anbieters wieder unter `skills/` und wuerden dann alle geladen. Nach jedem Sync also pruefen: neue Ordner nach `skills-all/` verschieben, `skills/` leeren.
