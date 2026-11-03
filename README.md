# MH Design – Webseite

Website für Ricardo Hartleb / MH Design in Mihla. Veröffentlichung über GitHub Pages: https://mh-design-smartrepair.github.io/ . Kein Build und keine Installation nötig.

## Vorschau

`node preview.cjs` startet die Vorschau unter http://127.0.0.1:4173. Der Server unterstützt Video-Streaming mit Byte-Ranges und liefert nur Webdateien aus. Er ist ausschließlich an die lokale Adresse gebunden.

Alternativ `index.html` direkt im Browser öffnen. Für eine vollständige Prüfung einschließlich Fehlerseite und Video-Seeking die HTTP-Vorschau verwenden.

## Aufbau

- `index.html`: Startseite, drei aufklappbare Leistungskarten, zwei Videovorschauen, Vorstellung, Ablauf, sechs FAQ und Kontakt.
- `videoblog.html`: beide Videos mit Sprunglinks und vollständigem Hochformat.
- `styles.css`: gemeinsame Gestaltung, Layouts, Typografie und Handy-Anrufbutton. Keine extern geladenen Schriftarten.
- `service-cards.css` / `site.js`: Leistungskarten, gleiche Höhen der geschlossenen Karten, aktuelle Navigationsposition.
- `motion.css` / `motion.js`: Einstieg und Scrollbewegung, Pause-Schalter und Berücksichtigung reduzierter Bewegung.
- `videos.js`: pausiert das jeweils andere Video und zeigt bei Ladefehlern einen direkten Dateilink.
- `404.html`: Fehlerseite mit absoluten Pfaden ab der Domain-Wurzel.

Die frühere Datei `enhancements.css` und die nicht benötigten Google-Fonts-Imports wurden entfernt. Bestehende Medien und fremde Projektunterlagen bleiben erhalten.

## Medien

- `assets/hero-konzept.webp`: optimierte Version des bisherigen KI-Konzeptbildes, 229.136 statt 2.503.164 Bytes. Auf der Webseite als Symbolbild gekennzeichnet.
- `assets/logo-header.svg`: bestehende transparente Logoversion für den dunklen Kopfbereich.
- `assets/video-humor-poster.webp` und `assets/video-aufbereitung-poster.webp`: Standbilder direkt aus den jeweiligen Videos.
- `assets/mh-design-vollstaendig.mp4`: korrigierter Canva-Export, 1080 × 1920, 15 Sekunden; vollständige Motive mit schwarzen Rändern.
- `assets/mh-design-video-02-ohne-ton.mp4`: 478 × 850, rund 43 Sekunden; Tonspur entfernt, Videodaten ohne Neukodierung erhalten.

Originalmedien bleiben als Quellen erhalten und werden von der Webseite nicht geladen.

## Prüfung

`python scripts/check-site.py` prüft interne Links, Sprungmarken, lokale Medien, eindeutige IDs, Hauptüberschriften und Bildbeschreibungen mit der Python-Standardbibliothek.

`node --check site.js` sowie entsprechende Aufrufe für `motion.js`, `videos.js` und `preview.cjs` prüfen die Syntax.

Browser-Prüfung und Screenshots: siehe `docs/qa/PRUEFBERICHT.md`.

## Veröffentlichung

Kontaktdaten sind vom Nutzer bestätigt. Impressum (impressum.html) und Datenschutzerklärung (datenschutz.html) sind seit 03.11.2026 auf den echten Geschäftsbetrieb umgestellt und im Footer verlinkt. Kleinunternehmer nach § 19 UStG, daher keine USt-ID. Wird ein externer Dienst eingebunden (Schriften, Karten, Formular, Analyse, YouTube), muss die Datenschutzerklärung angepasst werden. GitHub Pages verwendet main und das Stammverzeichnis. Seiten sind seit 03.11.2026 für Suchmaschinen freigegeben (nur 404.html bleibt noindex).

## SEO und Linkvorschau

Stand 19.10.2026: Canonical-URLs und Open-Graph-Vorschauen auf den vier Inhaltsseiten, strukturierte Betriebsdaten auf der Startseite. Bei Domainwechsel die absoluten URLs anpassen.

Seit 03.11.2026 auf Wunsch der Nutzerin für Google freigegeben: noindex entfernt (außer 404.html), robots.txt und sitemap.xml angelegt. Für schnellere Aufnahme die Seite in der Google Search Console anmelden und die Sitemap einreichen.
