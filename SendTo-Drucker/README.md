# SendTo-Drucker
Scripte und Aktionen für Kontextmenüs von Dateimanagern (Dolphin, Nemo)

- Text-, PDF- und Office-Dateien per Kontextmenü am Standarddrucker drucken

Alle Scripte werden im Verzeichis ~/bin des aktuellen Users installiert und die
Menüs werden jeweils für den aktuellen Nutzer bereitgestellt.
Das Verzeichnis ~/bin sollte im Suchpfad sein. Es werden keine Root-Rechte
zur Installation benötigt. In jedem Verzeichnis liegt eine Datei _install_.
Der Aufruf erfolgt im Terminal mit

user@linux:~/Pfad/zu/den/entpackten/Dateien/SendTo-Drucker> bash ./install

## Enthaltene Dateien:

* install (Bash-Script) - Installiert Scripte und Menüs für den angemeldeten Nutzer

* sendto_printer_wrapper.nemo_script (Bash-Script) - Wird aufgerufen von sendto_printer_office.nemo_action und sendto_printer_pdftxt.nemo_action.</br>
Dieses Script enthält die eigentliche Druckfunktion. Je nach übergebenem Parameter wird die Druckfunktion für Office-Dateien oder für Textdateien</br>
aufgerufen für alle an das Script übergebenen Dateien. Der Wrapper ermöglicht insbesondere für das Drucken der Office-Dateien eine Mehrfachauswahl,</br>
da die Headless-Druckfunktion von LibreOffice nur den Druck einer einzelnen datei pro aufruf zulässt. 

* Submenu-Sendto-Officefile2print.desktop - Menüerweiterung Office-Dateien an Standarddrucker senden für Dateimanager Dolphin

* Submenu-Sendto-PDFTXTPS2print.desktop - Menüerweiterung Text-, PDF-, INI- und Script-Dateien an Standarddrucker senden für Dolphin

* sendto_printer_office.nemo_action - Menüerweiterung Office-Dateien an Standarddrucker senden für Dateimanager Nemo

* sendto_printer_pdftxt.nemo_action - Menüerweiterung Text-, PDF-, INI- und Script-Dateien an Standarddrucker senden für Nemo

* README.md - Diese Datei hier
