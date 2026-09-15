# herzstueckmanufaktur.de

Die öffentliche Website. **Eigenes Repository** (`Melina1902/herzstueckmanufaktur`),
liegt nur zufällig im Ordner des JL-VA-Kits. Ein Push hier ändert sofort die
Seite im Netz, deshalb wird vorher gefragt.

Ausgeliefert über GitHub Pages, die Domain steht in `CNAME`.

## ⛔ Die feste QR-Adresse /karte

**Der QR-Code auf der gedruckten Klappvisitenkarte verweist dauerhaft auf
`https://herzstueckmanufaktur.de/karte`. Diese Adresse darf nicht geändert oder
gelöscht werden.**

Das jeweils aktuelle Ziel wird **ausschließlich** in `/data/karte-ziel.json` im
Feld `ziel` gepflegt. Dadurch kann das Ziel ausgetauscht werden, ohne den
QR-Code oder die Druckdatei zu verändern.

| Datei | Aufgabe |
|---|---|
| `karte/index.html` | liest das Ziel und leitet weiter. **Nicht anfassen.** |
| `data/karte-ziel.json` | hier und nur hier wird das Ziel geändert |

Ein neues Ziel eintragen heißt: `ziel` ändern, `bezeichnung` und `aktualisiert`
mitpflegen, committen, pushen. Mehr ist nicht zu tun.

Erlaubt sind eigene Pfade (`/irgendwas.html`) und vollständige Adressen
(`https://…`). Alles andere wird von der Seite abgelehnt und führt zur
Fehlerseite, damit ein Tippfehler die Karte nicht auf etwas Fremdes schickt.

Gedruckt und geprüft am 15.09.2026: Der Code in
`Herzstueckmanufaktur_Klappvisitenkarte_Druckdatei.pdf` enthält genau diese
Adresse.

## Abnahme

⛔ Vor jedem „fertig" läuft `/website-abnahme`. Kurzfassung:
`python3 ../../../ressourcen/website-check.py herzstueckmanufaktur.de`, danach
**jedes Formular wirklich absenden** und prüfen, ob die Mail ankommt.

*Warum:* Das Kontaktformular war acht Wochen funktionslos, ohne dass man es der
Seite ansehen konnte.
