# Übung HV02 - NAT-Switch erstellen

## Neuen Switch erstellen
    New-VMSwitch -SwitchName "ITCon" -SwitchType Internal

## Netzwerkadapter auflisten und ifIndex von "ITCon" Switch notieren
    Get-NetAdapter

## NAT Gateway konfigurieren - Switch eine IP geben damit er als Router/Gateway fungieren kann
    New-NetIPAddress -IPAddress 10.0.0.1 -PrefixLength 24 -InterfaceIndex <ifIndex von ITCon>

## NAT Netzwerk konfigurieren
    New-NetNat -Name ITConNAT -InternalIPInterfaceAddressPrefix 10.0.0.0/24
