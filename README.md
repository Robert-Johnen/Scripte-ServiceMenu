# Scripte-ServiceMenu
Scripte und Aktionen für Kontextmenüs von Dateimanagern (Dolphin, Nemo)

- SendTo-Drucker - Text-, PDF- und Office-Dateien per Kontextmenü am Standarddrucker drucken

- SendTo-MailRCPT - Versand von Dateien als Anhang mit Thunderbird oder per BlueTooth

- SendTo-mplayerPlaylist - Mediendatei in einer Einmal-Playlist mit MPlayer abspielen

- Submenu-PDF - verschiedene Menüaktionen mit PDF-Dateien

Alle Scripte werden Verzeichis ~/bin des aktuellen Users installiert und die
Menüs werden jeweils für den aktuellen Nutzer bereitgestellt.
Das Verzeichnis ~/bin sollte im Suchpfad sein. Es werden keine Root-Rechte
zur Installation benötigt. In jedem Verzeichnis liegt eine Datei _install_.
Der Aufruf erfolgt im Terminal mit

user@linux:~/Pfad/zu/den/entpackten/Dateien/SendTo-Drucker> bash ./install

user@linux:~/Pfad/zu/den/entpackten/Dateien/SendTo-MailRCPT> bash ./install

user@linux:~/Pfad/zu/den/entpackten/Dateien/SendTo-mplayerPlaylist> bash ./install

user@linux:~/Pfad/zu/den/entpackten/Dateien/Submenu-PDF> bash ./install
