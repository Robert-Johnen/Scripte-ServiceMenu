# SendTo-mplayerPlaylist
Scripte und Aktionen für Kontextmenüs von Dateimanagern (Dolphin, Nemo)

- Mediendatei in einer Einmal-Playlist mit MPlayer abspielen

Alle Scripte werden im Verzeichis ~/bin des aktuellen Users installiert und die
Menüs werden jeweils für den aktuellen Nutzer bereitgestellt.
Das Verzeichnis ~/bin sollte im Suchpfad sein. Es werden keine Root-Rechte
zur Installation benötigt. In jedem Verzeichnis liegt eine Datei _install_.
Der Aufruf erfolgt im Terminal mit

user@linux:~/Pfad/zu/den/entpackten/Dateien/SendTo-mplayerPlaylist> bash ./install

* install (Bash-Script) - Installiert Scripte und Menüs für den angemeldeten Nutzer

* ksm_sendto_add2mplayerplaylist (Bash-Script) - Legt einen Link für jede als Parameter übergebene Mediendatei 
ins Verzeichnis ~/.mplayer/playlist, startet mplayer mit diesem Verzeichnisinhalt als Playlist und löscht den 
Link nachdem die Datei abgespielt wurde.

* Submenu-Sendto-Mediaplayer.desktop - Integriert die Punkte "Senden an MPlayer Playlist" und Sendan an 
MPlayer sofort" ins Kontextmenü jeder Mediendatei in Dolphin.

* README.md - Diese Datei

