---
title: "Einführung"
date: 2023-02-15T13:21:57+01:00
---
# Einführung
Als gelernter Mediamatiker und nach meiner langjährigen Berufstätigkeit als Webentwickler, gehört die Informatik schon lange zu meinem täglich Brot. Seit Juni 2022 arbeite ich als Digitaler Archivar in der [Burgerbibliothek Bern](https://burgerbib.ch). Mit dem Stellenwechsel eröffnete sich mir eine neue Facette in der Welt der Informationstechnologie. Zu meinen Verantwortungen gehören die Betreuung sämtlicher Fachapplikationen und Web-Plattformen, als auch die Einführung neuer Workflows und Software, insbesondere vor dem Hintergrund der digitalen Langzeitarchivierung. 

In meinem Berufsalltag bin ich tagtäglich mit Fragen der Archivinformatik konfrontiert. Eine der zentralen Anwendungen in unserem Betrieb ist die Archivsoftware «scopeArchive», welche ich administriere. Aufgrund der proprietären Natur der Software beschränkt sich meine Arbeit allerdings eher darauf, dass ich Support-Tickets verfasse, weil Änderungswünsche oft Anpassungen am Quellcode erfordern. Jüngst beschäftigten mich im Rahmen der Überarbeitung der Digitalisierungsstrategie (im Sinne der digitalen Reproduktion), verschiedene Metadatenstandards (IPTC und XMP), vorwiegend mit dem Ziel, die Auffindbarkeit unsere Digitalisate zu verbessern. Langfristiges Ziel ist es, die Digitalisate mittels IIIF interoperabel anzubieten. Unser [OAIS](https://de.wikipedia.org/wiki/OAIS) befindet sich im Aufbau resp. in der Planung und Workflows fehlen. Zurzeit beschäftige ich mich deshalb stark mit Pre-Ingest Verfahren, indem ich Fallstudien anhand bestehender zwischengelagerten Datenablieferungen, welche mehrheitlich aus privaten Dateiablagen stammen, anfertige. Dabei ist mir aufgefallen, dass es bisher keine Software zu geben scheint, welche effektiv und effizient alle Aufgaben, die i. d. R. während des Pre-Ingests anfallen, zu bewältigen vermag. Als Beispiel: Bei der letzten Fallstudie, welche den Nachlass einer Schriftstellerin untersuchte, die Textdokumente (MSDOS-Word) auf 99 Disketten und einem USB-Stick beinhaltetet, war eine Vielzahl an Tools nötig. Um einen Eindruck zu vermitteln, nachfolgend ein Auszug davon:

* [Ubuntu WSL](https://learn.microsoft.com/de-de/windows/wsl/install)
* [detox](https://github.com/dharple/detox)
* [rsync](https://manpages.ubuntu.com/manpages/bionic/man1/rsync.1.html)
* [find](https://manpages.ubuntu.com/manpages/trusty/de/man1/find.1.html)
* [dupeGuru](https://dupeguru.voltaicideas.net/)
* [docuteam Packer](https://docs.docuteam.ch/packer/6.4/de/index)
* [ExifTool](https://exiftool.org/)
* [AntiWord](https://en.wikipedia.org/wiki/Antiword)
* [DROID](https://www.nationalarchives.gov.uk/information-management/manage-information/preserving-digital-records/droid/)
* [TrId](https://mark0.net/soft-trid-e.html)
* [TeraCopy](https://www.codesector.com/teracopy)

Für mich als fortgeschrittener Anwender stellt die Verwendung all dieser Tools, welche teilweise nur über die Kommandozeile zu bedienen sind, keine Schwierigkeit dar. Allerdings bin ich auf der ständigen Suche nach Möglichkeiten der Automatisierung und Vereinfachung, damit auch weitere Mitarbeitende, mit weniger technischem Know-How einfache Bestände bearbeiten können.

Bei Recherchen finde ich es immer wieder schwer abzuschätzen, welche Standards, Formate oder Software noch über Relevanz verfügen oder bereits als obsolet zu betrachten sind. Ich hoffe, dass ich nach dem Besuch des Moduls über etwas mehr Orientierung in der Welt der Bibliotheks- und Archivsinformatik verfüge. Gemeint ist damit auch die Vermittlung von Hilfe zur Selbsthilfe – Etwa durch Hinweise, welche Personen, Communities, Kompetenznetzwerke, Konsortien oder sonstige Organisationen es sich zu verfolgen lohnt oder über welche Kanäle diese erreicht werden können. Meine bisherige Erfahrung ist, dass die entsprechenden Netzwerke oft etwas «versteckt» sind und vieles nur halböffentlich ist (z. B. letztens bei Recherchen zur Digital Preservation Suite [aaru](https://aaru.app), zeigte sich, dass viele der Konversationen über IRC oder auf einem Discord Server stattfinden). Ich bin mir sicher, dass der Kurs für mich erkenntnisreich sein wird und ich glaube auch, dass ich Tools kennenlerne werde, welche ich hoffentlich in den Arbeitsalltag der Burgerbibliothek integrieren kann.