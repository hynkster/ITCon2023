# Übung WEB01 - Webserver

## Setzt einen Webserver auf auf Windows Basis auf!

## Erstellt eine VM

* Name:             Web01
* Generation:       02
* Arbeitsspeicher:  4096MB; dynamisch
* Netzwerk:         Default Switch
* VHD:              Web01.vhdx; 32GB
* Installation:     Von Imagedatei; Server2022.iso

## Startet die VM und installiert Windows Server 2022

* Language to install:      English
* Time & currency:          Germany
* Keyboard Input:           German
* Operating System:         Windows Server 2022 Standard Evaluation
* Installation Type:        Custom
* Hard Disk:                1 Partition; 32GB

## Richtet den Internet Information Service (IIS) ein

* Sucht eine passende Anleitung und installiert IIS auf Windows Server 2022
* Testet die Installation im Anschluss am Localhost und anschließend von einer anderen VM
* Konfiguriert den DNS so, dass der Webserver über den Domainnamen Web01.home.arpa erreichbar ist