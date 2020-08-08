## Mailversand mehrerer Anhaenge mit Thunderbird oder per BlueTooth
### _Submenu-Sendto-Mailrcpt.desktop_ (Dolphin)
erstellt das Kontextmenü Senden an... mit den Unterpunkten Mailempfänger und Bluetooth
(für den Mailversand wird das Script _ksm_sendto_mailrcpt_ irgendwo im Suchpfad erwartet, für den Versand per Bluetooth muss bluedevil installiert sein)
### _sendto_mailrcpt.nemo_action_ und *sendto_bluetooth.nemo_action* (Nemo)
machen das gleiche für Nemo
### _ksm_sendto_mailrcpt_
Bash-Script, dass alle übergebenen Dateien als Mailanhänge in eine neu Mail in Thunderbird packt.
Wird von _Submenu-Sendto-Mailrcpt.desktop_ und _sendto_mailrcpt.nemo_action_ benötigt
(muss im Suchpfad untergebracht werden)

## Installation:
```
# fuer KDE5-Dolphin
[ -d ~/.local/share/kservices5/ServiceMenus] || mkdir -p ~/.local/share/kservices5/ServiceMenus
cp Submenu-Sendto-Mailrcpt.desktop ~/.local/share/kservices5/ServiceMenus/
kbuildsycoca5
kbuildsycoca4
# fuer Nemo
[ -d ~/.local/share/nemo/actions ] || mkdir -p ~/.local/share/nemo/actions
cp sendto_*.nemo_action ~/.local/share/nemo/actions/
nemo -p
nemo
# ~/bin sollte eigentlich im Pfad sein
[ -d ~/bin ] || mkdir ~/bin
cp ksm_sendto_mailrcpt ~/bin/
chmod u+x ~/bin/ksm_sendto_mailrcpt
```
