# Hinweise zu diesem Fork

Fork von [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills), angelegt am 19.08.2026 als Sicherung fuer den Coder-Workspace.

Alle 49 Skills liegen unveraendert im Repo. Abweichung vom Original: In `.claude-plugin/plugin.json` ist die Liste `skills` von `./skills` (alle) auf 14 Pfade gekuerzt, das Website-Paket:

seo-audit, ai-seo, schema, site-architecture, content-strategy, copywriting, copy-editing, cro, analytics, signup, popups, lead-magnets, social, public-relations

Grund: Alle 49 Beschreibungen zusammen kosten rund 8.700 Token in jeder Sitzung, auch bei Arbeiten ohne Marketingbezug. Das Website-Paket liegt bei rund 2.500.

Weitere Skills freischalten: Pfad in `.claude-plugin/plugin.json` ergaenzen, pushen, dann `claude plugin marketplace update marketingskills` und das Plugin neu installieren (ein blosses `plugin update` zieht nur bei geaenderter Versionsnummer).

Abgleich mit dem Original: `gh repo sync immo24/marketingskills`. Konflikte sind nur in `.claude-plugin/plugin.json` zu erwarten.
