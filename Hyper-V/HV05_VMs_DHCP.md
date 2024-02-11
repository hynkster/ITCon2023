# Übung HV05 - DHCP Server installieren

## Installiert auf DC01 die Rolle DHCP Server

## Richtet den DHCP Server mit den folgenden Einstellungen ein

* Authorisiert den DHCP Server (dc01.itcon.arpa) sofern noch nicht geschehen
* Erstellt einen Adressbereich (Scope) 
    * Name:         ITConClients
    * Start IP:     10.0.0.100
    * End IP:       10.0.0.200
    * Subnet mask:  255.255.255.0

## Ändert das Netzwerk der folgenden VMs auf "ITCon"

* DC01
* Win01
* Core01

## Kontrolliert ob die VMs eine korrekte IP zugewiesen bekommen

Nutzt dazu:
* ipconfig
* ping
* tracert 

