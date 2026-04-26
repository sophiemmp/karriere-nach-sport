# Vorlage für einen Multimediabeitrag

Diese Vorlage ist für Studierende im Modul **Schreiben und Sprechen** (Studiengang MMP, FHGR) gedacht.  
Ziel ist, multimediales Storytelling mit einer klaren, wiederverwendbaren Struktur umzusetzen:

- sauber gegliederter Einstieg
- Kombination aus Text, Bild und Audio
- barriereärmere Aufbereitung durch zusätzliche Textinhalte (z. B. Transkription)

## Zweck des Repos

Das Repository stellt zwei zentrale Dateien bereit:

- `vorlagen.html`: eine **Arbeitsvorlage** mit Platzhaltern und Kommentaren.
- `index.html`: ein **ausgefülltes Beispiel**, das zeigt, wie ein fertiger Beitrag aussehen kann.

Dazu kommen die zugehörigen Styles und Medienordner:

- `css/style.css`: visuelle Gestaltung.
- `assets/images/`: Beispiel- und Projektbilder.
- `assets/audio/`: Beispiel- und Projektaudios.

## Schnellstart (empfohlenes Vorgehen)

1. `vorlagen.html` als Ausgangspunkt nutzen.
2. Datei als neue `index.html` oder Projektdatei speichern.
3. Platzhaltertexte ersetzen:
   - Oberzeile
   - Titel
   - Lead
   - Autor:innenzeile + Datum
   - Textblöcke und Zwischentitel
4. Medien austauschen:
   - Bilder in `assets/images/` ablegen
   - Audios in `assets/audio/` ablegen
   - `src`-Pfade im HTML anpassen
5. Beitrag in Browser prüfen (Desktop + mobil).

## Grundprinzip der Struktur

Die Vorlage trennt den Beitrag in:

- **fixen Einstiegsteil, ein Audiobeitrag kann vorangestellt werden** (didaktisch vorgegeben)
- **flexiblen Hauptteil** (frei anpassbar und erweiterbar)

So bleibt der redaktionelle Aufbau konsistent, während inhaltliche Dramaturgie im Hauptteil variieren kann.

## Aufbau in `vorlagen.html` im Detail

### 1) Kopfbereich der Seite (`<head>`)

- Sprache ist auf `de-CH` gesetzt.
- Meta-Angaben für Zeichensatz und responsive Darstellung sind gesetzt.
- Die CSS-Datei ist bereits eingebunden.

Nutzen: standardisierte technische Basis für alle Beiträge.

### 2) Seitenkopf (`.site-header`)

- enthält die einfache Marken-/Projektkennzeichnung "Multimediabeitrag".
- dient als wiederkehrendes Gestaltungselement.

### 3) Hauptinhalt (`<main>` + `<article>`)

Der eigentliche Beitrag liegt in einem semantischen `<article>`.

#### 3.1 Optionaler Audio-Teaser (ganz oben)

- Position: vor Oberzeile und Titel.
- Zweck: schneller akustischer Einstieg in Thema oder Stimmung. Auch ein moderierter Teaser oder ein O-Ton ist möglich.
- Umsetzung: `<audio controls preload="metadata">`.

#### 3.2 Fixer Content-Header (Reihenfolge vorgegeben)

Die Reihenfolge bis inkl. erstem Textblock ist verbindlich:

- Verortung (Oberzeile)
- Hauptaussage (Titel)
- Kurzinhalt (Lead)
- Absender (Autorenzeile + Datum)
- Einstieg (erster Textblock)

Warum fix?  
Damit alle Beiträge mit derselben publizistischen Logik starten.

#### 3.3 Flexible Inhaltsblöcke (danach frei kombinierbar)

Ab dem Hauptteil können Bausteine umsortiert oder mehrfach genutzt werden:

- Zwischentitel + Text (`<section class="text-block">`)
- Einzelbild + Bildlegende (`<figure>`, `<figcaption>`)
- Audio-Einspieler / O-Ton / Atmo
- optionales Abschluss-Audio (Fazit, Ausblick)
- optionaler Toggle-Block (`<details>`) für Transkription/Zusammenfassung

Damit kann der Beitrag je nach Thema eher textlastig, bildlastig oder audiolastig aufgebaut werden.

#### 3.4 Optionaler Artikel-Footer

- kurzer Copyright- oder Projekthinweis.
- kann zusätzliche Angaben enthalten (z. B. Quelle, Kurs, Jahrgang).

## Bedeutung der einzelnen Bestandteile (redaktionell)

- **Audio-Teaser (optional):** holt Publikum sofort ab; ideal für starke O-Töne oder atmosphärische Einstiege.
- **Oberzeile:** ordnet Thema/Fokus ein, noch vor der eigentlichen Headline.
- **Titel:** zentrale Aussage oder Hauptversprechen des Beitrags.
- **Lead:** Aufbau je nach Darstellungsform, führt immer ins Thema ein und schafft Leseanreiz.
- **Autor:innenzeile + Datum:** nennt Autorenschaft und Zeitpunkt der Veröffentlichung.
- **Erster Textblock:** Szenischer Einstieg bei Reportage und Feature, zentrale Informationen beim Bericht.
- **Zwischentitel + Textblock:** strukturieren den Verlauf in verdauliche Abschnitte.
- **Bild + Bildlegende:** liefert visuelle Evidenz; Legenden schaffen Bildbezug und bieten Zusatzinformationen.
- **Audio-Einspieler / O-Ton:** bringt Stimmen, Perspektiven, Atmosphäre und Glaubwürdigkeit.
- **Abschluss-Audio (optional):** verdichtet Erkenntnisse oder setzt einen klaren Schluss.
- **Mehr-lesen-Bereich (optional):** verbessert Zugänglichkeit durch Textalternative für Audio.
- **Footer (optional):** rechtliche/organisatorische Zusatzinfos.

## Medien korrekt ersetzen

### Bilder

- Eigene Bilddateien nach `assets/images/` legen.
- Bildpfad im HTML in `src` anpassen.
- Aussagekräftigen `alt`-Text schreiben.
- Bildlegende inkl. Foto-/Quellenangabe ergänzen.

### Audio

- MP3-Dateien nach `assets/audio/` legen.
- Pfad im jeweiligen `<source src="...">` anpassen.
- Klarheit, was man hört oder wer spricht (z.B. durch Anmoderation oder redaktionelle Einbettung im Text wie "Sie erinnert sich an diesen Moment:" )
- Bei relevanten O-Tönen nach Möglichkeit Transkript oder Zusammenfassung im `details`-Block bereitstellen.

## Didaktische Empfehlungen für den Unterricht

Mögliche Kriterien für Aufgabenstellung oder Bewertung:

- **Struktur:** klarer roter Faden vom Lead bis zum Schluss.
- **Medienlogik:** Audio/Bild ergänzen den Text inhaltlich und wiederholen ihn nicht.
- **Textqualität:** präzise Sprache, nachvollziehbare Quellen, saubere Übergänge.
- **Zugänglichkeit:** aussagekräftige Alt-Texte und (wenn nötig) Transkription.
- **Formalia:** korrekte Autor:innenangabe, Datum, Quellenhinweise.

## Typische Fehler und wie man sie vermeidet

- **Fehler:** nur Platzhalterpfade genutzt (`pfad/zum/...`).  
  **Lösung:** echte Dateien im `assets`-Ordner ablegen und Pfade aktualisieren.

- **Fehler:** leere Platzhaltertexte bleiben stehen.  
  **Lösung:** alle Dummy-Inhalte vor Abgabe systematisch ersetzen.

- **Fehler:** Bildlegenden ohne Mehrwert ("Symbolbild").  
  **Lösung:** Bezug zu Bildinhalt schaffen, Zusatzinfos einbetten, Quellverweis integrieren.

- **Fehler:** Audio ohne Einordnung.  
  **Lösung:** stimmige Übergänge schaffen, auf logischen Aufbau achten.

- **Fehler:** unstrukturierte Hauptteile.  
  **Lösung:** pro Teilaspekt einen Zwischentitel setzen.

## Unterschiede zwischen `vorlagen.html` und `index.html`

- `vorlagen.html`:
  - neutral, mit Platzhaltern
  - als Startpunkt für neue Beiträge gedacht
  - kommentiert, damit Bausteine schnell gefunden werden

- `index.html`:
  - ausgefüllter Beispielbeitrag
  - zeigt konkrete Nutzung von Audio, Bild und Text
  - dient als Referenz für Layout und dramaturgische Reihenfolge

## Technische Hinweise

- Die Vorlage funktioniert ohne Build-Prozess direkt im Browser.
- Klassen in HTML und CSS sollten konsistent bleiben, damit das Layout erhalten bleibt.
- Bei Erweiterungen möglichst semantische HTML-Elemente weiterverwenden (`section`, `figure`, `details`).

## Lizenz und Verantwortung (anpassbar)

Bitte für reale Publikationen immer prüfen:

- Nutzungsrechte für Bilder und Audios
- korrekte Quellen- und Urheberangaben
- inhaltliche und rechtliche Verantwortung der Autor:innen/Redaktion
