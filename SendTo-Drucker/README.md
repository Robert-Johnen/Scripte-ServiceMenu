# SendTo-Drucker
Scripte und Aktionen für Kontextmenüs von Dateimanagern (Dolphin, Nemo)

- Text-, PDF- und Office-Dateien per Kontextmenü am Standarddrucker drucken

Alle Scripte werden Verzeichis ~/bin des aktuellen Users installiert und die
Menüs werden jeweils für den aktuellen Nutzer bereitgestellt.
Das Verzeichnis ~/bin sollte im Suchpfad sein. Es werden keine Root-Rechte
zur Installation benötigt. In jedem Verzeichnis liegt eine Datei _install_.
Der Aufruf erfolgt im Terminal mit

user@linux:~/Pfad/zu/den/entpackten/Dateien/SendTo-Drucker> bash ./install

Enthaltene Dateien:
* install 
** Bash-Script -Installiert Scripte und Menüs für den angemeldeten Nutzer

* nemowrapper_printfile - wird aufgerufen von sendto_printer_office.nemo_action und 
                          sendto_printer_pdftxt.nemo_action

-rw-r--r-- 1 robert users 1064  9. Aug 01:29 README.md
-rw-r--r-- 1 robert users 1053  7. Aug 15:29 sendto_printer_office.nemo_action
-rw-r--r-- 1 robert users  312  7. Aug 15:29 sendto_printer_pdftxt.nemo_action
-rw-r--r-- 1 robert users 1337 16. Feb 2018  Submenu-Sendto-Officefile2print.desktop
-rw-r--r-- 1 robert users  449  2. Mär 2018  Submenu-Sendto-PDFTXTPS2print.desktop
