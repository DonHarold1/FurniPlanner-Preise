# Online-Preisliste

`preise.json` ist die Preisliste, die FurniPlanner Pro bei jedem Start lädt.
Die App holt sie von einer **öffentlichen** Adresse (Rohadresse dieser Datei in diesem Repository),
der letzte gültige Stand gilt offline weiter.

**Preise aktualisieren:** Werte ändern, `stand` auf das heutige Datum setzen, hier committen und pushen.
Ein App-Update ist nicht nötig.

- Schlüssel: `kantholz`, `diele` (€/m), `schraube`, `beschlag` (€/Stück), `spiegel`, `rueckwand` (€/m²),
  `platte|<Material>|<Stärke>` (€/m², Material wie in der App: Multiplex, Siebdruck, MDF, Leimholz Buche).
- Fehlende Schlüssel behalten den eingebauten Richtwert; unbekannte Schlüssel und Werte unter 0 werden übergangen.
- Eigene Standardpreise in der App und Preise einzelner Projekte haben immer Vorrang.
