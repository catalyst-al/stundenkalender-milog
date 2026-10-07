# Stundenkalender - MiLoG

Ein einfacher, browserbasierter Stundenkalender für die Arbeitszeiterfassung nach MiLoG. Arbeitszeiten werden automatisch berechnet; das offizielle PDF wird mit einem Klick erzeugt.

## Live

https://catalyst-al.github.io/stundenkalender-milog/

## Für GitHub Pages veröffentlichen

1. Bei GitHub ein neues Repository erstellen, zum Beispiel `stundenkalender-milog`.
2. Das Repository bei Bedarf auf **Public** setzen.
3. Diese Dateien in die oberste Ebene des Repositories hochladen:
   - `index.html`
   - `README.md`
   - `.gitignore`
4. Im Repository **Settings** -> **Pages** öffnen.
5. Bei **Build and deployment** `Deploy from a branch` auswählen.
6. Den Branch `main` und den Ordner `/(root)` auswählen und speichern.
7. Nach kurzer Zeit erscheint dort der öffentliche Link, zum Beispiel:
   `https://BENUTZERNAME.github.io/stundenkalender-milog/`

## Nutzung

1. Monat auswählen und die Mitarbeiterdaten einmal eintragen.
2. Auf dem Handy öffnet sich die **🗓️ Woche** (Wochenansicht wie in einer Dienstplan-App):
   - Oben **KW** mit Datum und Wochensumme; mit **‹ ›** oder durch **Wischen** die Woche wechseln, **Heute** springt zur aktuellen Woche.
   - Jeder Tag zeigt seine Schicht als farbige Karte (Zeit, Pause, Stunden). Nachtschichten sind mit **+1** markiert (Ende am Folgetag).
   - Tag antippen → von unten öffnet sich das Tagesblatt: Schicht wählen (Nacht, Früh, Früh lang, Spät, Spät lang, Urlaub, Frei), Zeiten mit **−15 / +15** anpassen oder eigene Zeit tippen (`630-15`, `2230-7 p3`, `630-14 / 1430-2230`). **Weiter →** springt zum nächsten Tag.
   - **Zwei Schichten an einem Tag:** im Tagesblatt unter **➕ 2. Schicht** wählen. Beide Schichten erscheinen als eigene Karten („1. Schicht“ / „2. Schicht“) mit Tagessumme; ✕ entfernt die zweite.
   - **⧉ Woche in nächste kopieren** überträgt die Woche in die leeren Tage der Folgewoche; **↶ Rückgängig** macht jeden Schritt rückgängig.
   - Eine Woche über den Monatswechsel (z. B. 28.09.–04.10.) speichert jeden Tag in seinem eigenen Monat. Das PDF bleibt pro Monat.
3. Schichten eintragen – am Computer am schnellsten im Modus **⚡ Schnell**:
   - Unten eine Schicht wählen: 🌙 Nacht 22:30–07:00, 🌅 Früh 06:30–14:00, 🌄 Früh lang 06:30–15:00, 🌇 Spät 14:30–22:30, 🌆 Spät lang 14:30–23:00 – oder 🏖️ Urlaub bzw. 🧽 Frei.
   - Tage antippen oder mit Finger/Maus über mehrere Tage ziehen. Nochmals tippen = Tag löschen.
   - **➕ 2. Schicht** einschalten, um an einem Tag eine zweite Schicht hinzuzufügen (wird automatisch zeitlich sortiert; Überschneidungen werden gemeldet).
   - 🏖️ Urlaub markiert den Tag im Kalender, zählt keine Arbeitsstunden und erscheint nicht im MiLoG-PDF.
   - Lange drücken bzw. Rechtsklick öffnet die Details (eigene Zeiten, Entlohnungsart).
   - **🔁 Erste Woche wiederholen** überträgt Tag 1–7 auf alle leeren Tage des Monats; **↶ Rückgängig** macht jeden Schritt rückgängig.
   - Tastatur: Pfeiltasten wählen den Tag, `1`–`5` tragen die Schicht ein, `U` Urlaub, `0` löscht, `+` schaltet die 2. Schicht um, `Strg`+`Z` macht rückgängig.
4. Einzelne Tage genau anpassen im Modus **✏️ Detail** (Tagesliste):
   - Jeder Tag ist eine Zeile mit Zeitleiste (04:00 bis 08:00 am Folgetag). Tag antippen öffnet die Bearbeitung darunter.
   - **Schnell tippen** und mit `Enter` zum nächsten Tag: `630-15` (06:30–15:00), `2230-7 p3` (Pause ab 03:00), `630-14 / 1430-2230` (zwei Schichten), `u` = Urlaub, `0` = frei. Ohne `p` wird die Pause automatisch gesetzt (30 Min. ab 6 Std., 45 Min. ab 9 Std.; bei bekannten Schichten deren Pause).
   - In der Leiste die **Enden ziehen** = Beginn/Ende, den **gestreiften Block ziehen** = Pause verschieben (15-Min.-Schritte).
   - Knöpfe **−15 / +15 / +30** für Beginn, Ende und Pause; Schicht-Chips; **➕ 2. Schicht**; **⧉ Wie Vortag**; **⋯ Details** öffnet den bisherigen Tagesdialog. Darunter steht das Freitextfeld **Entlohnungsart** – der eingetragene Text erscheint im Formular/PDF in der letzten Spalte.
   - ⚠️ Hinweise bei mehr als 10 Std. Arbeitszeit, zu kurzer Pause, weniger als 11 Std. Ruhezeit oder überschneidenden Schichten (nur Hinweise, keine Rechtsberatung).
5. Unter **Formular (Druck / PDF)** auf **Offizielles PDF erzeugen** klicken.
6. Das fertige MiLoG-PDF herunterladen und an die Buchhaltung weitergeben.

## Datenschutz und Sicherung

Die Daten werden nur im Browser auf dem jeweiligen Gerät gespeichert. Sie werden nicht an GitHub übertragen. Für einen Gerätewechsel oder als Sicherung bitte regelmäßig die JSON-Backup-Funktion in der Anwendung verwenden.
