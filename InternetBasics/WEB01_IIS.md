# Übung WEB01 - Webserver

## Setzt einen Webserver auf auf Windows Basis auf!

## Erstellt eine VM

* Name:             Web01
* Generation:       02
* Arbeitsspeicher:  4096MB; dynamisch
* Netzwerk:         ITCon
* VHD:              Web01.vhdx; 32GB
* Installation:     Von Windows Server 2022 Imagedatei

## Startet die VM und installiert Windows Server 2022

* Language to install:      English
* Time & currency:          Germany
* Keyboard Input:           German
* Operating System:         Windows Server 2022 Standard Evaluation (Desktop Experience)
* Installation Type:        Custom
* Hard Disk:                1 Partition; 32GB

## Vergebt eine statische IP und den Server der Domain hinzu

* IP:          10.0.0.12
* Subnetmask:  255.255.255.0
* Gateway:     10.0.0.1
* Domain:      itcon.arpa 

## Richtet den Internet Information Service (IIS) ein

* Sucht eine passende Anleitung und installiert IIS auf Windows Server 2022
* Testet die Installation im Anschluss von Localhost und Win01