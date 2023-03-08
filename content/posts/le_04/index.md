---
title: "Lerneinheit 04: Funktion und Aufbau von Bibliothekssystemen 1/2"
date: 2023-03-07
---

Die Lerneinheit war Einstieg in den zweiteiligen Block "Aufbau von Bibliothekssystemen".  Betrachtet wurden insbesondere MARC21 und die Bibliothekssoftware Koha.

## MARC21
Dem bibliografischen Datenformat [MARC21](https://www.loc.gov/marc/bibliographic/) begegne ich in der Regel nur, wenn ich mich bei der Recherche in [Swisscovery](https://swisscovery.slsp.ch/), in der Detailansicht im Abschnitt "Links" mich verklicke und den Eintrag ["Quelldaten"](https://swisscovery.slsp.ch/discovery/sourceRecord?vid=41SLSP_NETWORK:VU1_UNION&docId=alma991170412202005501&recordOwner=41SLSP_NETWORK) aufrufe. Beruflich hatte ich damit noch nie zu tun, worüber ich froh bin, denn dem Standard fehlt m. E.  Wahrlich an Ästhetik. 

Ich muss ehrlich gestehen, dass sich mir der Nutzen von MARC21 nur teilweise erschliesst, zumal in der [Praxis](https://docs.google.com/presentation/d/e/2PACX-1vRU4J_rln00UVD7pNPT0_02NOad0HfSk_UKqRI0v29y8QkMAplEDlyjc0Ot_VE_paV6WBW29Fh_V-iN/pub?start=false&loop=false&delayms=3000&slide=id.g574306292a_0_35) die Verwendung immer wieder vom Standard abweicht. Ebenfalls für mich unverständlich, dass das Dateiformat sowohl in binärer als auch in Text kodierter Form (XML) existiert. 

Dem im Jahr 1999 verabschiedeten Format ist das Alter anzuspüren. Immerhin leuchtet mit [BIBFRAME](https://www.loc.gov/bibframe/), welches auf [RDF](https://www.w3.org/RDF/) basiert, ein Hoffnungsschimmer am Horizont. Mich interessierte, ob BIBFRAME bereits im produktiven Einsatz ist. Während ich in den Katalogen der Library of Congress und auf Swisscovery nur auf die üblichen MARC Datensätze stiess, verfügt der Katalog der deutschen Nationalbibliothek jeweils zusätzlich über eine [RDF-Repräsentation](https://d-nb.info/1254981578/about/lds) (Abb. 1), welche tatsächlich eine einzige Property (projectedProvisionDate) von BIBFRAME verwendet. Bei der weiteren Recherche staunte ich nicht schlecht, als ich erfuhr, dass die DNB bereits seit 2012  an BIBFRAME mitwirkt.

{{< figure src="screenshot-dnb.png" alt="Screenshot des Online-Katalogs der deutschen Nationalbibliothek." caption="Abb. 1. Im Katalog der deutschen Nationalbibliothek steht neben MARC21 zusätzlich eine RDF-Repräsentation zur Verfügung." >}}

## Koha
Die [Koha Library Software](https://koha-community.org/) hatte ich bereits einmal installiert, weil ich auf der Suche nach einer Anwendung war, in welcher ich meine private Bibliothek verwalten konnte. Obwohl ich die in der Programmiersprache Perl geschriebene Software erstaunlicherweise auf meinem Shared-Hosting zum Laufen gebracht hatte, stiess mich damals, wie auch heute nach erneuter Begutachtung während des Unterrichtes, sowohl das User-Interface als auch die User-Experience ab.

Was an Koha imponiert, ist die Kontinuität, welche das Projekt aufweist. Die Statistiken zum Projekt auf dem Portal [Open Hub](https://www.openhub.net/p/koha) lassen sich sehen: Das Projekt ist bereits 22 Jahre alt, 573 Entwickler:innen haben an den 588 071 Zeilen Code mitgearbeitet und die Commits sind über die Jahre hinweg insgesamt stabil.  Auch in einem [Vergleich](https://www.openhub.net/p/_compare?project_0=Invenio&project_1=Koha+Library+Automation+Package&project_2=Evergreen) mit den konkurrenzierenden ILS,  "Invenio" und "Evergreen" behauptet sich Koha als das insgesamt beständigste Projekt.

## Fazit
Insgesamt hinterlässt Teil 1 zur Lerneinheit "Funktion und Aufbau von Bibliothekssystemen", bei mir wenig Begeisterung. Einerseits, weil ich im Berufsalltag keine Berührungspunkte mit der Materie habe und sich mir deshalb der Zweck nur zu geringen Anteilen erschliesst. Andererseits lässt es mich zweifeln, ob es überhaupt gute ILS gibt. Obwohl Koha zwar ständig weiterentwickelt wird, erscheint mir das Projekt, in der Zeit stillgestanden. Ich frage mich, ob dies etwa damit zusammenhängt, dass in erster Linie ein Format (MARC21) verwendet wird, welches seine besten Zeiten hinter sich hat...