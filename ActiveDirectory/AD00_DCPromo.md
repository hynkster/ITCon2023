# Übung AD00 - Domain Controller Promotion

## Prmoted den Server DC01 zum Domain Controller
* Gebt dem Server eine fixe IP Adresse (10.0.0.10). Der Server muss dazu mit dem Netzwerk ITCon verbunden sein!
* Installiert über den Servermanager "Active Directory Domain Services" und "DNS" und startet im Anschluss die VM neu.
* Nach dem Neustart ist im Servermanager ein Benachrichtigung über die, die Promotion durchgeführt werden kann.
* Erstellt eine neuen Forest mit dem Domain Namen "itcon.arpa".
* Erstellt das Directory Restore Passwort.
* Die übrigen Einstellungen können auf default belassen werden.
* Es folgt ein Check der Voreinstellungen. Ist dieser erfolgreich abgeschlossen kann die Installation durchgeführt werden.
* Nach Abschluss der Installation und einem Neustart, kontrolliert mit "Get-ADDomainController" in Powershell ob die Installation erfolgreich war. 