# Scripte-ServiceMenu
Scripte und Menüeinträge für das Kontextmenü der Dateimanager Dolphin und Nemo

- SendTo-Drucker - Sende Text-, PDF-, Script- und Officedateien an den Standarddrucker (Nemo und Dolphin)

- SendTo-MailRCPT - Sende Dateien per BlueTooth oder als Mailanhang mit Thunderbird (Nemo und Dolphin)

- SendTo-mplayerPlaylist - Sende Mediendatei zum Abspielen an eine Einmal-Playlist für MPlayer

- myPDF-Tool - [https://github.com/Robert-Johnen/myPDF-Tool] Analysiere und Modifikation von PDF-Dateien (Nemo und Dolphin)

In jedem Unterverzeichnis liegt eine Datei _install_. Durch den Aufruf von
``` 
user@host:~/entpackte/Dateien> bash ./install
```
im jeweiligen Unterverzeichnis werden die entsprechenden Menüeinträge generiert und die Scripte in das
Verzeichnis ~/bin kopiert. Sollte ein entsprechendes Unterverzeichnis noch nicht existieren, wird es angelegt.

* README.md - Diese Datei