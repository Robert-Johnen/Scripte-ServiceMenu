# SendTo-MailRCPT
Scripte und Aktionen für Kontextmenüs von Dateimanagern (Dolphin, Nemo)

- SendTo-MailRCPT - Versand von Dateien als Anhang mit Thunderbird oder per BlueTooth

Alle Scripte werden im Verzeichis ~/bin des aktuellen Users installiert und die
Menüs werden jeweils für den aktuellen Nutzer bereitgestellt.
Das Verzeichnis ~/bin sollte im Suchpfad sein. Es werden keine Root-Rechte
zur Installation benötigt. In jedem Verzeichnis liegt eine Datei _install_.
Der Aufruf erfolgt im Terminal mit

user@linux:~/Pfad/zu/den/entpackten/Dateien/SendTo-MailRCPT> bash ./install

* install (Bash-Script) - Installiert Scripte und Menüs für den angemeldeten Nutzer

* ksm_sendto_mailrcpt (Bash-Script) - Erstellt die Befehlszeile, damit Thunderbird eine neue Mail mit den als Parameter übergebenen Dateien als Anhang generiert und ruft diese dann auf

* sendto_bluetooth.nemo_action - Stellt den Kontextmenübefehl "Senden an... Bluetoothgerät" für Nemo zur Verfügung.

* sendto_mailrcpt.nemo_action - Stellt den Kontextmenübefehl "Senden an... Mailempfänger mit Thunderbird" für Nemo zur Verfügung

* Submenu-Sendto-Mailrcpt.desktop - Stellt die Kontextmenübefehle "Senden an... Bluetoothgerät" und Senden an... Mailempfänger mit Thunderbird" für Dolphin zur Verfügung.

* README.md - Diese Datei
