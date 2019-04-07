# Nikola-Source der Homepage des Fablab Region Nürnberg e. V. [![Build Status](https://travis-ci.org/fablabnbg/homepage-nikola.svg?branch=master)](https://travis-ci.org/fablabnbg/homepage-nikola)

## Changelog

- 2019-04-05: Als neues Projekt angelegt zwecks Ersatz der aktuellen Homepage 

## Ziel des Projekt

- Die aktuelle Homepage des Fablab (basierend auf Wordpress) soll durch eine neue Homepage ersetzt werden, da sich die Installation als schlecht wartbar erwiesen hat und es umständlich ist, neue Inhalte hinzuzufügen.

- Als Ersatz soll ein "static site generator" verwendet werden, also ein Tool, welches aus Vorlagen automatisiert Webseiten mit statischem Inhalt erzeugt.

- Als Tool wurde [Nikola](https://getnikola.com) ausgesucht. Dieses basiert auf Python, es stehen viele Erweiterungen zur Verfügung und ist auch für unsere Zwecke leicht erweiterbar.

## Lokale Installation

1. Nikola lokal installieren gemäß https://getnikola.com/getting-started.html
   * Falls es Probleme mit `virtualenv`gibt wegen fehlendem `disutils.spawn`: Das Modul distutils für python3 nachinstallieren, z. B. durch `sudo apt install python3-distutils`
   
1. Anstelle von Schritt 2 von getnikola.com (Initialisierung einer Seite), dieses Repository hier klonen:
   * `git clone https://github.com/fablabnbg/homepage-nikola.git`
   
1. Installation der benötigten Plugins:
   * `nikola plugin -i ical`

## Lokales erstellen der Homepage

1. In das Verzeichnis homepage-nikola wechseln:
   * `nikola build` zum Erstellen der Seite ausführen
   * `nikola server` um einen lokalen Webserver zu starten

1. --> fun & profit
   * Änderungen bitte lokal testen und dann `git add .`, `git commit`, `git push`
   

## Hilfe & Regeln zum Erstellen der Seiten

--> siehe [Wiki](https://github.com/fablabnbg/homepage-nikola/wiki)

## Deployment

- In der ersten Entwicklungsphase wird die Seite auf github-pages unter der URL https://fablabnbg.github.io/homepage-nikola deployed. Dies erfolgt automatisch durch [Travis-CI](https://travis-ci.org/fablabnbg/homepage-nikola).
- Sobald ein neuer Commit im github-Repository erfolgt (also entweder durch editieren auf der github-Seite oder durch den `push` eines lokalen Commit), erstellt travis-ci automatisch die neue Homepage und committed/pusht sie in den gh-pages branch.
- Dieser branch wird von "github pages" verwendet, um den Inhalt auf github.io anzuzeigen.
- Sobald die neue Homepage den Status erreicht hat, die alte zu ersetzen, werden wir ein Deployment aufsetzen, was direkt auf unseren Webserver deployed.
- Solange nur die Webseite auf github-pages verwendet wird, hat jeder, der "Member" der Organisation "fablabnbg" ist, auch Schreibzugriff über github. Wenn die Homepage "live" ist, wird der Zugang eingeschränkt.
