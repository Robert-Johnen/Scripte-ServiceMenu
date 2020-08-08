ksm_pdf_tool
===

Bash-Script zur Analyse und zum Auseinanderpflücken einer PDF-Datei in ihre Bestandteile

Aufruf:
---
  user@linux:~> ksm_pdf_tool PDF-Dokument PARAMETER1 PARAMETER2 PARAMETER3
  
  PDF-Dokument
  ---
  eine PDF-Datei beliebigen Formates / beliebiger Version
  
  moegliche Werte PARAMETER1:
  ---
  INFO     --> 	ermittelt soviele Informationen wie moeglich schreibt sie in PDF-Dokumentname.pdfinfo
  
  TEXTEXT  --> 	extrahiert den in der PDF-Datei enthaltenen Text
		        in PDF-Dokumentname.txt
	        Zur Texterkennung per OCR muss mindestens PARAMETER2
	        angegeben werden:
                    wird PARAMETER2 angegeben und ist eine natuerliche
                    Zahl zwischen 150 und 600 wird er als dpi-Angabe fuer die
                    Texterkennung per OCR interpretiert.
                    Sollte PARAMETER2 keine nat. Zahl sein, wird er als
                    Sprachangabe fuer die Texterkennung per OCR
                    interpretiert und Standardaufloesung (150dpi) gesetzt.
                    Wird PARAMETER3 angegeben, wird dieser als 
                    Sprachangabe fuer die Texterkennung genutzt.
                    Ansonsten wird als Standardsprache deutsch (deu) genutzt
  
  IMGEXT   --> 	extrahiert alle im PDF-Dokument vorhandenen Bilder in
                Originalaufloesung nach dem Schema:
	                    Dateiname-Seitenzahl-Bildnummer.[png|tiff|jpg|jp2|ppm]
	        und extrahiert aus den Bildern vorhandene Farbprofile
  
  SEPPAGES --> 	Erstellt aus jeder Seite der PDF-Datei ein eigenes PDF-Dokument
                nach dem Schema Dateiname-Seitenzahl.pdf
  
  DETACH   --> 	extrahiert alle Dateianhaenge (falls denn welche existieren)
  
  ATTACH   --> 	haengt eine Datei als Attachment an die PDF-Datei an
                (das Original der angehaengten Datei wird geloescht)
  
  HTML     --> 	Erstellt aus der PDF-Datei ein HTML-Dokument (nicht schoen)
  
  PS       --> 	Erstellt aus der PDF-Datei eine PostScript-Datei
  
  ALLES    --> 	Alles was INFO, TEXTEXT IMGEXT, SEPPAGES, DETACH, HTML und PS
	        machen. Des weiteren werden vorhandene Schriftdaten extrahiert,
	        Einzelseiten in SVG- und PostScript-Dateien gewandelt, damit
	        evtl. vorhandene Vektordaten daraus haendisch extrahiert werden
	        koennen und alle Dateien in entsprechende Unterverzeichnisse
	        einsortiert.
<pre>
Die Verzeichnisstruktur sieht so aus:
PDF-Dateiname
	├── Audiodaten
	│   └── SoundFonts
	├── Ausgabe
	├── Backup
	│   └── Rohdaten
	├── Bilddaten
	│   ├── Animationen
	│   ├── Grafiken
	│   ├── Paletten
	│   ├── Profile
	│   └── Videos
	├── Dateianhaenge
	├── Seriendruckdaten
	└── Textdaten
    	    ├── HTML
    	    ├── Schriften
    	    ├── Stile
    	    └── Tabellen
    Ja aber da ist ja jede Menge unnötiger Kram bei...
    Weiß ich, aber ich nutze die Verzeichnisstruktur auch für
    andere Dinge (u.A. z.B. in Scribus zum Layouten und ordnen der Datenablage)</pre>
  PDFA1B   --> 	Erstellt eine Datei im Format PDF-A-1b
  
  ROTL     --> 	rotiert alle Seiten um 90° gegen den Uhrzeigersinn
                im Verhaeltnis zur Ausrichtung der Originaldatei
  
  ROTR     --> 	rotiert alle Seiten um 90° im Uhrzeigersinn
                im Verhaeltnis zur Ausrichtung der Originaldatei
  
  ROTD     --> 	rotiert alle Seiten um 180° 
                im Verhaeltnis zur Ausrichtung der Originaldatei
  
  REVERSE  -->	kehrt die Seitenreihenfolge um
  
  M2S      --> 	erstelle PDF mit 2 Seiten pro Blatt
  
  M4S      --> 	erstelle PDF mit 4 Seiten pro Blatt
  
  ALLFEAT  --> 	hebt alle Restriktionen innerhalb der PDF auf
                (Drucken erlaubt, Kommentiern erlaubt, usw.)
  
  CONVPNG  -->	konvertiert alle Seiten zu PNG-Pixelgrafiken mit der
                in PARAMETER2 angegebenen Aufloseung. Sollte PARAMETER2
                keine nat. Zahl zwischen 150 und 600 sein, wird die
                Standardaufloesung von 150dpi gesetzt
  
  CONVJPG  -->	konvertiert alle Seiten zu JPG-Pixelgrafiken  mit der
                in PARAMETER2 angegebenen Aufloseung. Sollte PARAMETER2
                keine nat. Zahl zwischen 150 und 600 sein, wird die
                Standardaufloesung von 150dpi gesetzt

  Benoetigt werden folgende Programme:
  realpath, basename, dirname, tr, grep, awk, ls, mv, mkdir, rm, cp, sort, file,
  uniq, pdfinfo, oyranos-icc, podofopdfinfo, pdffonts, pdfimages, pdfdetach,
  pdfseparate, pdftops, pdftocairo, pdftohtml, pdftotext, pdftoppm, pdftk,
  pdfjam, cfftot1, mutool, tesseract, qpdf, convert, rsync
  
Dolphin-Submenu-PDF.desktop
===
Integriert das ksm_pdf_tool in das Kontextmenü jeder PDF-Datei im KDE-Dateimnager Dolphin

pdf_tool.nemo_action
===
wie Dolphin-Submenu-PDF.desktop, nur für Dateimanager Nemo
