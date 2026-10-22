# Online-Preisliste

`preise.json` ist die Preisliste, die FurniPlanner Pro lädt, sobald ein Werkstück fertiggestellt wird.
Die App holt sie von einer **öffentlichen** Adresse (`Preisliste.adresse` in `Quellen/Kern/Preisliste.swift`),
der letzte gültige Stand gilt offline weiter.

**Preise aktualisieren:** Werte ändern, `stand` auf das heutige Datum setzen, Datei an der öffentlichen Adresse ersetzen.
Ein App-Update ist nicht nötig.

- Schlüssel: `kantholz|<Maß>x<Maß>` (€/m je Querschnitt, größeres Maß zuerst, z. B. `kantholz|80x60`),
  `kantholz`, `diele` (€/m), `schraube`, `beschlag` (€/Stück), `spiegel`, `rueckwand` (€/m²),
  `platte|<Material>|<Stärke>` (€/m², Material wie in der App: Multiplex, Siebdruck, MDF, Leimholz Buche).
- Kantholz-Querschnitte, die nicht in der Liste stehen, rechnet die App vom nächstliegenden Querschnitt
  nach Fläche um. Plattenstärken ohne Listenpreis werden aus den gelisteten Stärken desselben Materials interpoliert.

## Erhebung 22.10.2026 (Hornbach online, Markt Mönchengladbach-Eicken)

- **Kantholz:** „Kantholz Duo verleimt“ (80 × 40/60/80) und „Konsta Kantholz Fichte gehobelt“, Preis je m.
- **Siebdruck:** Siebdrucksperrholz Birke Sieb/Film 2500 × 1250 (9–21 mm mit Online-Zuschnitt, 24 mm ohne).
- **Multiplex:** Multiplexplatte Birke BB/BB 3000 × 1500 – bei Multiplex bietet Hornbach keinen Online-Zuschnitt an.
- **MDF:** MDF roh 2800 × 2070 (12, 16, 18 mm).
- **Leimholz Buche:** Leimholzplatte Buche A/B massiv keilgezinkt 4200 × 800 (Preis je m ÷ 0,8 m), günstigste Ganzplatte je Stärke.
- **Rückwand:** Dünn-MDF einseitig grau 2440 × 1220 × 3 mm.
- Nicht erhoben (eingebaute Richtwerte): Terrassendiele, Edelstahlschraube, Spiegelglas, Wandbeschlag.
- Fehlende Schlüssel behalten den eingebauten Richtwert; unbekannte Schlüssel und Werte unter 0 werden übergangen.
- Eigene Standardpreise in der App und Preise einzelner Projekte haben immer Vorrang.
