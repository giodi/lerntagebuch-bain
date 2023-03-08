---
title: "Lerneinheit 03: Open Refine"
date: 2023-02-28
---
In der Lerneinheit wurde hauptsächlich die Software [OpenRefine](https://openrefine.org/) behandelt. Der Einstieg bestand aus Exkursen in diverse Themengebiete und Literaturempfehlungen.

## Literaturempfehlungen
Wie im [ersten]({{< ref "/posts/le_00" >}} "Wo bin ich 
gestartet?") Blog geschildert, bin ich besonders erpicht auf Hinweise zu
 weiterführenden Ressourcen. Mich freute, dass sich neben der bereits in der ersten Unterrichtseinheit präsentierte [Library Carpentry 
Lessons](https://librarycarpentry.org/lessons/), mit den [Programming Historian Lessons](https://programminghistorian.org/en/lessons/) ein Äquivalent für Archive vorgestellt wurde.

## Exkurs zu Open Source Health
Das komplexe Ökosystem von Open-Source-Software mit deren Akteuren und Implikationen (wie jüngst die Kontroverse um [core-js](https://github.com/zloirock/core-js/blob/master/docs/2023-02-14-so-whats-next.md) zeigte) interessiert mich sowohl aus persönlicher als auch aus beruflicher Sicht. Bei Archivsoftware scheint mir das Thema sehr akut. Während der Suche nach Software für den Pre-Ingest, stellte ich öfters fest, dass die in der Fachliteratur genannten Anwendungen oft ungepflegt in Repositorien vor sich hin existieren (z. B. [bagger](https://github.com/LibraryOfCongress/bagger)). Dass anhand von OpenRefine auf mögliche Problematiken im Gebrauch von Open-Source-Software sensibilisiert wurde, werte ich als eine sinnvolle Verknüpfung.

## OpenRefine
Bereits im vorherigen Semester, in welchem es galt einen umfangreichen Datensatz zu bearbeiten, hatte ich mir OpenRefine installiert. Allerdings verwarf ich das Vorhaben, die Software für das Projekt zu nutzen, aufgrund des engen Zeitbudgets, welches mir keine Einarbeitungszeit erlaubte. Umso erfreulicher, dass es nun im Rahmen des Unterrichts zu einer Einführung kam.

OpenRefine ist eine Software, welche das Bereinigen und Explorieren von Datensätzen vereinfacht. Dazu stehen u. a. Funktionen zur Facettierung, zum Clustering oder zur Verknüpfung weiterer Daten, z. B. via Web-Services wie Wikidata, zur Verfügung.

### Arbeiten mit OpenRefine
OpenRefine kennt die zwei Darstellungsmodi  "rows" und "records". Dies hat seine Tücke, wie das folgende, im Unterricht behandelte, Beispiel demonstriert.

Verwendet wurde ein [Datensatz](https://raw.githubusercontent.com/LibraryCarpentry/lc-open-refine/gh-pages/data/doaj-article-sample.csv), welcher wissenschaftliche Publikationen mit Angaben, wie Titel, DOI oder Autorenschaft enthielt. Die Zellen der Spalte "Authors" führten teils mehrere Autor:innen auf. Dabei wurden die Namen, mit einer vertikalen Linie (|) getrennt. Über die Funktion "Edit cells"  → "Split multi-valued cells…"  besteht die Möglichkeit anhand eines Separators, in diesem Fall die vertikale Linie, das Feld aufzutrennen. Dadurch vermehrte sich die Anzahl Zeilen von 1001 auf 4009 (Abb. 1). 

{{< figure src="rows.png" alt="Screenshot von OpenRefine in der Rows-Ansicht." caption="Abb. 1. Nachdem die Zellen der Spalte 'Authors' aufgetrennt wurden, sind insgesamt 4009 Zeilen vorhanden. Dabei verfügen die neuen Zeilen nur in den Zellen der Spalte 'Authors' einen Wert, wie hier im Screenshot auf der zweiten Zeile zu sehen." >}}

Die neuen Zeilen verfügten jeweils nur in der Spalte "Authors" einen eingefüllten Wert, was etwas kontraintuitiv anmutet. Die Lösung dazu bietet OpenRefine mit der "records"-Ansicht. Ein Record kann sich aus mehr als einer Zeile zusammensetzen (Abb. 2). Dabei ist zu beachten: 

> OpenRefine understands records based on the content of the first column, what we call the “key column.” Splitting a row into a multi-row record will base all association on the first column in your dataset. 
> [-- Dokumentation OpenRefine](https://openrefine.org/docs/manual/exploring#rows-vs-records)

{{< figure src="records.png" alt="Screenshot von OpenRefine in der Records-Ansicht." caption="Abb. 2. Wird in die Records-Ansicht gewechselt, werden die aufgetrennten Zeilen anhand der ersten Spalte, als eine Einheit angezeigt. Dadurch verringert sich die Anzahl der Gesamteinträge." >}}

Besteht die erste Spalte nicht aus einem eindeutigen Indentifikationswert für jede Zeile, kann dies zu Fehlschlüssen führen. Sind Duplikate oder leere Felder vorhanden, werden diese in der Records-Ansicht fälschlicherweise alle in einem einzigen Record zusammengeführt. Dies birgt das Risiko von Fehlinterpretationen, insbesondere nach Anwendung weiterer Transformationen oder Filter.

Das motivierte mich dazu herauszufinden, wie in OpenRefine am einfachsten eine ID-Spalte generiert werden kann. Eine dedizierte Funktion dafür gibt es nicht. Allerdings lässt sich über die Funktion "Edit column" → "Add column based on this column…" das gewünschte Resultat bewerkstelligen. Dabei besteht die Möglichkeit, mittels einer "Expression" in der General Refine Expression Language (GREL) Anweisungen auf die zu generierende Spalte auszuführen. Über die [Variable](https://openrefine.org/docs/manual/expressions#variables) ``rowIndex`` wird in die Zelle die jeweils aktuelle Zeilenzahl eingefügt (Abb. 3). Abschliessend ist die neue Spalte per  "Edit column" → "Move column to beginning" an erste Stelle zu verschieben.


{{< figure src="add-col-2.png" alt="Screenshot von Dialog zum generieren einer neuen Spalte." caption="Abb. 3. Im Dialog zum Generieren einer neuen Spalte wird eine Vorschau der neuen Spalte angezeigt, womit sich Expressions testen lassen." >}}

## Fazit zur Lerneinheit
Für mich reiht sich OpenRefine zwischen Tabellenkalkulationsprogrammen wie Excel und komplexeren Systemen wie dem [Elastic Stack](https://www.elastic.co/de/elastic-stack/). Ich kann mir den künftigen Einsatz im Arbeitsalltag für die Bearbeitung von umfangreicheren Datensätzen gut vorstellen. Etwa für die Zusammenführung und Auswertung, von Nutzungsstatistiken, der verschiedenen Plattformen. Nichtsdestoweniger war die Einführung insbesondere wertvoll, um Fallstricke der Software kennenzulernen.