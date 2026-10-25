FamilyBoard 0.2 – Google Kalender + Google Tasks

START
1. Die Dateien auf einem HTTPS-Webserver hosten (z.B. GitHub Pages).
   NICHT einfach index.html als file:// öffnen: Google OAuth benötigt einen registrierten HTTPS-Ursprung.
2. In Google Cloud Console ein Projekt anlegen. Google Calendar API und Google Tasks API aktivieren.
3. OAuth-Zustimmungsbildschirm konfigurieren; ggf. Testnutzer hinzufügen.
4. OAuth-Client vom Typ 'Webanwendung' anlegen. Unter 'Autorisierte JavaScript-Quellen'
   die exakte HTTPS-Origin der App eintragen, z.B. https://BENUTZER.github.io
   (ohne Pfad). OAuth Client-ID in FamilyBoard eintragen.
5. Pro Tablet eigenes Profil wählen. Google verbinden.
6. Auf dem Familien-Tablet mit dem eigenen Konto anmelden. Freundin gibt ihren
   Kalender in Google Kalender für dieses Konto frei. Danach beide Kalender auswählen.
7. Auf Tylers Tablet mit seinem Konto anmelden und seine Aufgabenliste auswählen.

WICHTIGE GRENZEN
- Google-Zugriffstoken nur im Arbeitsspeicher, keine dauerhafte Anmeldung nach Neuladen.
- Ein Google-Konto pro Tablet-Sitzung. Profilwechsel trennt die Sitzung.
- Google Tasks API liefert wiederkehrende Aufgaben nicht immer gleich wie die Google-Tasks-Oberfläche;
  Wiederholungsregeln werden in Google Tasks verwaltet. Abhaken wirkt auf Google Tasks.
- Keine zuverlässige Google-Anmeldung auf jedem alten Android-8.1-Browser garantiert.
- Kalender werden nur gelesen. Google Tasks werden gelesen und bearbeitet.
- Lokale Testaufgaben (ohne Google) sind nicht mit Google synchronisiert.
- Kalender-Monatsansicht zeigt maximal vier Termine pro Tag, max. 250 je Kalender/Monat.
- Keine Hintergrundsynchronisierung bei geschlossenem Browser.
- Der Profilwechsel ist keine Kindersicherung; dafür braucht es später eine echte Benutzerverwaltung.


GOOGLE-VERBINDUNG (GitHub Pages)
1. In Google Cloud die Google Calendar API und Google Tasks API aktivieren.
2. OAuth-Client vom Typ Webanwendung: Autorisierte JavaScript-Quelle https://sebastianhuxdorf-tech.github.io
3. Auf der FamilyBoard-Seite die OAuth-Client-ID in das sichtbare Feld eintragen und auf „Google-Konto verbinden“ klicken.
4. OAuth-Berechtigungen: https://www.googleapis.com/auth/calendar.readonly und https://www.googleapis.com/auth/tasks. Die zweite ist nötig, damit Aufgaben hinzugefügt, abgehakt und gelöscht werden können. Nur tasks.readonly reicht dafür nicht.
5. Falls der Google OAuth-Zustimmungsbildschirm auf Test steht, Google-Konto als Testnutzer eintragen.
6. Die App benötigt keinen OAuth-Client-Schlüssel im Browser. Niemals einen Client-Schlüssel in HTML oder GitHub hochladen.
7. Die index.html muss direkt im Hauptverzeichnis des GitHub-Repositories liegen, nicht in einem Unterordner familyboard.

Wetter: Nennhausen, Open-Meteo (ohne API-Schluessel), aktuelle Werte und drei Folgetage. Internetverbindung erforderlich.
