FamilyBoard 2.0 – Firebase Live Einkaufslisten

1. Lade index.html und manifest.json ins GitHub Pages Repository (Root).
2. Firebase Console > Authentication > Settings > Authorized domains: sebastianhuxdorf-tech.github.io hinzufügen.
3. In der App den Reiter Einkaufslisten öffnen, mit der in Firebase Authentication angelegten E-Mail und dem Passwort anmelden.
4. Bestätigungs-E-Mail senden, Link öffnen, dann „Bestätigung prüfen“ anklicken.
5. Danach werden beide Listen live mit Firestore synchronisiert.

WICHTIG: Die bereits veröffentlichten Firestore-Regeln erlauben ausschließlich die bestätigte E-Mail sebastianhuxdorf@gmail.com. Andere Nutzer müssen später ausdrücklich in Regeln und Authentication eingerichtet werden. Die Datenbank darf NICHT auf öffentliche Regeln umgestellt werden.

Das ist eine Web-App, noch keine Android-APK. Google Kalender/Tasks sind weiterhin aus der vorherigen Version und noch nicht unabhängig pro Profil authentifiziert.
