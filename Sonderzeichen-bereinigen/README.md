# Sonderzeichen-bereinigen

Ersetzen von Sonderzeichen in einem kompletten Verzeichnisbaun für alle Dateien und Verzeichnisse
Das Kontextmenü erscheint in Dolphin, wenn eines oder mehrere Verzeichisse ausgewählt wird und in Nemo,
wenn genau ein Verzeichnis ausgewählt ist. Grund für dieses Script war die Anschaffung einer Digitaldruck-Anlage
von Konica-Minolta. Diese läuft unter Linux, hat allerdings Probleme mit Datei- und Verzeichnisnamen, die 
unter Windows mit Sonderzeichen erstellt wurden (falsche Codierung der Sonderzeichen beim Übertragen der Dateien).
Die Drucksoftware weigert sich, Dateien mit Sonderzeichen im Dateinamen zu drucken.
Um dieses Problem zu umgehen habe ich dieses Miniscript geschrieben.

* Folder_detox.desktop - Kontextmenüeintrag für Dateimanager Dolphin

* folder_detoxdirs.nemo_action - Kontextmenü für Dateimanager Nemo (nur Verzeichnisse bereinigen)

* folder_detoxfiles.nemo_action - Kontextmenü für Dateimanager Nemo (nur Dateien bereinigen)

* install (Bash-Script) - installiert Scripte und Menüs für den angemeldeten Benutzer

* ksm_detox (Bash-Script) - Kurzes Script zum Umbenennen einer Datei, bei dem die Sonderzeichen in der Konfigurationsdatei _.detoxrc_ entsprechend ersetzt werden

* .detoxrc - Konfigurationsdatei für das Script ksm_detox

* README.md - Diese Datei
