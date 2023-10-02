# Code Beispiel zum erstellen von Benutzern

    # Define a list of user names and display names
    $users = @(
        @{Name="Michael"; DisplayName="Michael Trebo"; Surname="Trebo"; UPN="michael.trebo@itcon.arpa"},
        @{Name="John"; DisplayName="John Smith"; Surname="Smith"; UPN="john.smith@itcon.arpa"},
        @{Name="Jane"; DisplayName="Jane Doe"; Surname="Doe"; UPN="jane.doe@itcon.arpa"},
        @{Name="Alice"; DisplayName="Alice Johnson"; Surname="Johnson"; UPN="alice.johnson@itcon.arpa"},
        @{Name="Bob"; DisplayName="Bob Williams"; Surname="Williams"; UPN="bob.williams@itcon.arpa"},
        @{Name="Emily"; DisplayName="Emily Brown"; Surname="Brown"; UPN="emily.brown@itcon.arpa"},
        @{Name="David"; DisplayName="David Wilson"; Surname="Wilson"; UPN="david.wilson@itcon.arpa"},
        @{Name="Sarah"; DisplayName="Sarah Anderson"; Surname="Anderson"; UPN="sarah.anderson@itcon.arpa"},
        @{Name="Ryan"; DisplayName="Ryan Davis"; Surname="Davis"; UPN="ryan.davis@itcon.arpa"},
        @{Name="Laura"; DisplayName="Laura Martinez"; Surname="Martinez"; UPN="laura.martinez@itcon.arpa"}
    )

    # Loop through the list and create users
    foreach ($user in $users) {
        New-ADUser -Name $user.Name -DisplayName $user.DisplayName -Surname $user.Surname -UserPrincipalName $user.UPN
    }