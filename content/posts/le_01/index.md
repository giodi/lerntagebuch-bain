---
title: "Lerneinheit 01 und 02: Technische Grundlagen"
date: 2023-02-15T13:22:57+01:00
---
Die ersten beiden Unterrichtsblöcke beschäftigten sich, wie meist üblich, insbesondere mit dem gegenseitigen Kennenlernen, organisatorischen Fragen und Einführungen zu verschiedenen Plattformen und Tools, welche für den Unterricht verwendet werden.

## Aufbau Kurs
Eine für mich positive Überraschung sind die im Kurs eingesetzten Tools. Die Software HedgeDoc kannte ich bisher nicht. Die Plattform unterscheidet sich allerdings nicht wesentlich von anderen kollaborativen Dokumenten-Editoren, welche ich bereits nutze (z. B. [Cryptpad](https://cryptpad.fr) -- wie sich nach einer kurzen [Recherche](https://docs.hedgedoc.org/) herausstellte, ist HedgeDoc u. a. von Etherpad inspiriert). Ein Blick auf den [Funktionsumfang](https://pad.gwdg.de/features) offenbart mir altbekannt aber auch neue JavaScript-Bibliotheken. Bis auf [mermaid](https://mermaid-js.github.io/mermaid/) hatte ich alle bereits in meinen Lesezeichen abgespeichert.

Für den Unterricht, welcher bis auf den ersten Termin nur noch Online stattfinden wird, erscheint mir der Einsatz eines kollaborativen Dokuments sinnvoll. Im Gegensatz zu den sonst als PDF abgespeicherten Powerpoint Folien, empfinde ich die Form als übersichtlicher und barrierefreier: Hyperlinks sind sauber gesetzt (ungültige Links in abgegebenen Unterrichtsfolien, waren keine Seltenheit, bedingt durch aufgrund der URL-Länge automatisch eingefügten Umbrüchen ...), sauberes Einbetten von Multimedia-Inhalten ist möglich und für mich am wichtigsten -- mittels der Suchfunktion des Webbrowsers ({{< kbd Ctrl >}} + {{< kbd F >}}) kann alles rasch aufgefunden werden. Eigentlich schade, dass die FHGR keine eigene Instanz für die Studierenden betreibt und stattdessen oft Google Docs genutzt wird. Ich bin gespannt, inwiefern der Funktionsumfang der Software während des Semesters ausgenutzt wird, bisher beschränkte sich der Einsatz darauf, dass wir unsere Namen in eine Liste eintragen, um zu signalisieren, wenn wir mit einer Übung durch sind.

## Schaubild zu Lehrinhalten
{{< figure src="schaubild.png" alt="Ein Diagramm, welches ein Schaubild der Lerninhalte zeigt." caption="Abb. 1. Schaubild Lerninhalte." >}}

Das Schaubild zu den Lerninhalten (Abb. 1) dient als Übersicht zum Inhalt, welcher uns in den nächsten Monaten beschäftigen wird. Einige der im Diagramm erwähnten Systeme hatte ich in der Vergangenheit bereits einmal zum Testen installiert (Koha, Archivespace, Open Refine und Solr) allerdings habe ich mich in keine der Software-Dokumentationen besonders vertieft resp. die Software dann effektive in eine produktive Umgebung übernommen. Ebenfalls sind mir der Dublin Core Standard und EAD bereits bekannt, welche ich aber nur gelegentlich verwende. Die restlichen Tools und Standards kenne ich nur dem Namen nach (VuFindHarvest, MARC21-XML, marcEdit, VuFind).

Der Aufbau deutet auf einen praktisch orientierten Unterricht hin, was ich begrüsse. Ich finde es leichter ein Verständnis für Standards (z. B. EAD) zu gewinnen, wenn diese gleich im Kontext einer Anwendung gestellt werden, als nur eine trockene Spezifikation vorgestellt zu bekommen. 

## Markdown
Die Markdown-Syntax ist mir geläufig aus dem Grund, dass ich sie regelmässig für das Erstellen meiner Notizen verwende. Ich nahm mir deshalb die Freiheit, die Übung zu überspringen.

## Einrichtung der Arbeitsumgebung
GitHub Codespaces hatte ich bisher noch nie verwendet. Eine Neuheit ist das Prinzip trotzdem nicht -- sowohl im Beruf als auch während des Studiums, sind immer wieder mal VMs aus der Cloud (meist von VMware) im Einsatz. Mir war das Installieren von Software für den Unterricht schon oft ein Ärgernis. Mein Erlebnis ist, dass der Zeitaufwand für die Inbetriebnahme und Deinstallation in keinem Verhältnis zum Nutzen stand, weshalb ich die Lösung mit Codespaces als optimal ansehe. Während des Unterrichts habe ich einen Codespace kurz angeworfen und sogleich wieder gelöscht, weil auf meinem Rechner bereits Ubuntu Linux lief und ich deshalb für die zu erledigenden Übungen nicht darauf angewiesen war.

## Unix Shell 
Die Unix Shell gehört zu meinem Berufsalltag. Früher als Webentwickler, vorwiegend um Konfigurationen anzupassen oder um Web-Tooling zu betreiben, heute mehrheitlich, um Stapelverarbeitung vorzunehmen, wofür die Unix Shell sehr komfortabel ist. Aber auch Privat nutze ich sie häufig -- auf meinem Rechner läuft meistens Ubuntu wobei das Terminal meist geöffnet ist, für meine "self-hosted" Applikationen auf meinem Heimserver und Webserver ist die Verwendung der Shell unabdingbar. Trotzdem habe ich betreffend der Shell noch lange nicht ausgelernt. Bei der Durchsicht der Abschnitte der entsprechenden [Library Carpentry ](https://librarycarpentry.org/lc-shell/) Lektion erstaunt mich, dass keine Editoren wie vi, vim oder nano erwähnt werden. Bekanntlich ist die Wahl des Editors, Gegenstand heiss geführter Debatten (Abb. 2): 

{{< figure src="real_programmers.png" alt="Cartoon Real Programmers von xkcd.com" caption="Abb. 2. Comic von [xkcd.com](https://xkcd.com/378/)." >}}

Interessant waren für mich vor allem die Kapitel 4.--6., welche Befehle enthielten, die ich nur selten benutze oder noch nie gehört hatte.
 Ich entschied mich dafür, die Übung ["Automating the tedious with loops"](https://librarycarpentry.org/lc-shell/04-loops/index.html) durchzuarbeiten, weil ich dies schon länger nicht mehr gemacht hatte und mir dies im Arbeitsalltag am ehesten wiederbegegnen wird. 

Als ich den folgenden Loop schrieb und in einem Ordner voller PDFs ausführte, war ich erst überrascht, dass ich eine leere Ausgabe zur Antwort erhielt:

 `for filename in ?.pdf; do echo "$filename.pdf"; done`

Mir wurde klar, dass ich nicht wusste, wofür das Fragezeichen stand. In einem der im [Cheatsheet für Shell-Scripte](https://devhints.io/bash) verlinkten Seiten fand ich die Antwort und darüber hinaus weitere interessante Hinweise. Beim Fragezeichen handelt es sich demnach um einen [Glob](http://mywiki.wooledge.org/glob), welcher als Platzhalter für genau ein Zeichen steht. Weil es in meinem Verzeichnis kein PDF gab, das über einen Dateinamen mit nur einem Zeichen verfügte, war die Ausgabe infolgedessen leer. Verwendete ich anstatt des Fragezeichens ein Asterisk, welches als Platzhalter für beliebig viele Zeichen steht, entsprach die Ausgabe meinen Erwartungen.

`for filename in *.pdf; do echo "$filename.pdf"; done`

Noch spannender fand ich indes die Verwendung von [extglobs](http://mywiki.wooledge.org/glob#Options_which_change_globbing_behavior), mit welchen sich u. a.  auf einfache Art und Weise Negationen realisieren lassen. Nach Ausführung des abgeänderten Codes wurde richtigerweise nur noch Dateien, die über kein PDF-Suffix verfügten, ausgegeben.

`for filename in !(*.pdf); do echo "$filename"; done`

## Git
Git als auch die verschiedenen Anbieter wie Bitbucket etc. stellen für mich kein Novum dar. Interessanter fand ich indes den Hinweis auf [BibsOnGitHub](https://github.com/axel-klinger/BibsOnGitHub). Insbesondere die Liste mit den [Repositorien](https://axel-klinger.github.io/BibsOnGitHub/repositories.html) habe ich mir sogleich zu den Lesezeichen hinzugefügt, ich kann mir gut vorstellen, dass ich die Liste in Zukunft mal zu Recherchezwecke konsultiere.

## Fazit zur Lerneinheit
Insgesamt enthielten die ersten zwei Unterrichtsblöcke wenig gänzlich Neues für mich bereit. Trotzdem konnte ich einiges wieder auffrischen und Vereinzeltes entdecken. Am interessantesten empfand ich die Verweise auf die Webseiten [Bash scripting cheatsheet](https://devhints.io/bash) und [BibsOnGitHub](https://github.com/axel-klinger/BibsOnGitHub).