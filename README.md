# Homepage des Fablab Region Nürnberg

2019-04-05: Als neues Projekt angelegt zwecks Ersatz der aktuellen Homepage 


## Lokale Installation

1. Nikola lokal installieren gemäß https://getnikola.com/getting-started.html
   * Falls es Probleme mit `virtualenv`gibt wegen fehlendem `disutils.spawn`: Das Modul distutils für python3 nachinstallieren, z. B. durch `sudo apt install python3-distutils`
   
2. Anstelle von Schritt 2 von getnikola.com (Initialisierung einer Seite), dieses Repository hier klonen:
   * `git clone https://github.com/fablabnbg/homepage-nikola.git`

3. In das Verzeichnis homepage-nikola wechseln:
   * `nikola build` zum Erstellen der Seite ausführen
   * `nikola server` um einen lokalen Webserver zu starten

4. --> fun & profit
   * Änderungen bitte lokal testen und dann `git add .`, `git commit`, `git push`
