Festool-Oberfräse Einweisung
============================

Einweisung des [FAU FabLab](https://fablab.fau.de) in die Oberfräse Festool OF 1010 EBQ.

Inhalt
------

- Regeln und Sicherheit, Betriebsanweisung BA-OF-01 (Aushang bei der Oberfräse)
- Bedienelemente (Foto mit Bedienhinweisen), Checkliste, Schutzausrüstung, Material, Absaugung, Werkstück spannen
- Fräser wechseln, Frästiefe einstellen, Drehzahl wählen
- Fräsen Schritt für Schritt, Gegenlauf, Aluminium, Verbotsliste
- Seitenanschlag, Führungsschiene, Stangenzirkel
- Infos für Betreuer: typische Fehler, Pflege und Prüfung

Download
--------

Die neueste Version aus [GitHub](https://github.com/fau-fablab/festool-oberfraese-einweisung) ist als PDF abrufbar:

- [Einweisung](https://brain.fablab.fau.de/build/festool-oberfraese-einweisung/einweisung_Oberfraese.pdf)
- [Einweisungsliste](https://brain.fablab.fau.de/build/festool-oberfraese-einweisung/Einweisungsliste_Oberfraese.pdf)
- [Betriebsanweisung](https://brain.fablab.fau.de/build/festool-oberfraese-einweisung/Betriebsanweisung_Oberfraese.pdf) (Aushang bei der Oberfräse)

Außerdem baut eine GitHub Action die PDFs bei jedem Push. Auf dem Hauptbranch entsteht dabei ein
[Release](https://github.com/fau-fablab/festool-oberfraese-einweisung/releases) mit Datums-Version (`vJJJJ.MM.TT`) und den PDFs.

Auschecken und bauen
--------------------

```bash
git clone --recursive git@github.com:fau-fablab/festool-oberfraese-einweisung.git
cd festool-oberfraese-einweisung
make
```

Die PDFs landen in `output/`. Layout, Kopf- und Fußzeile und das Logo des FAU FabLab (mit
FAU-Schriftzug) kommen aus dem Untermodul [fablab-document](https://github.com/fau-fablab/fablab-document),
das Logo wiederum aus dessen Untermodul [logo](https://github.com/fau-fablab/logo). Bei einem bestehenden
Klon die Untermodule mit `git submodule update --init --recursive` laden.

Technische Details zum Buildserver: [fau-fablab/buildserver](https://github.com/fau-fablab/buildserver)

[![Build Status](https://brain.fablab.fau.de/build/festool-oberfraese-einweisung/status.svg)](https://brain.fablab.fau.de/build/festool-oberfraese-einweisung/)
[![TODOs](https://brain.fablab.fau.de/build/festool-oberfraese-einweisung/status-todos.svg)](https://brain.fablab.fau.de/build/festool-oberfraese-einweisung/)
[![PDF bauen](https://github.com/fau-fablab/festool-oberfraese-einweisung/actions/workflows/pdf.yml/badge.svg)](https://github.com/fau-fablab/festool-oberfraese-einweisung/actions/workflows/pdf.yml)

Lizenz
------

[![Lizenz: CC BY-SA 3.0](https://licensebuttons.net/l/by-sa/3.0/de/88x31.png)</br>CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/)

Die Einweisung und die Betriebsanweisung (`betriebsanweisung/ba_oberfraese.tex`, BA-OF-01) sind selbst
formuliert und enthalten keine Texte oder Abbildungen aus der Festool-Betriebsanleitung. Alle Zeichnungen
in `zeichnungen/` sind selbst mit TikZ erstellt; Symbole nur nach ISO 7010 aus `fablab-document`.
Ausnahme: Das Foto `bilder/oberfraese-of1010ebq.jpg` stammt von GoRapid (Wikimedia Commons) und steht
unter CC BY 3.0, siehe [bilder/QUELLEN.md](bilder/QUELLEN.md).
Für Details wird auf die Originalanleitung von Festool verwiesen. **Beim Bearbeiten nichts aus der
Festool-Anleitung übernehmen, auch nicht sinngemäß Satz für Satz.** Bilder bitte selbst zeichnen
oder fotografieren.
