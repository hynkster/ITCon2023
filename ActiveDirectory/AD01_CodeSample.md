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

# Version Armir

# Define the list of first names and surnames
$firstNames = "John", "Jane", "Michael", "Emma", "William", "Olivia", "James", "Ava", "Benjamin", "Sophia"
$surnames = "Doe", "Smith", "Johnson", "Williams", "Brown", "Jones", "Miller", "Davis", "Garcia", "Rodriguez"  # Replace with actual surnames

 

# Define the Organizational Unit where users will be created

    $OU = 'OU=IT,DC=ITCon,DC=com'  # Please confirm the distinguished name of your desired OU

    # Iterate over both firstNames and surnames and create users
    for ($i = 0; $i -lt $firstNames.Length; $i++) {
        $name = $firstNames[$i]
        $surname = $surnames[$i]

        # Check if the combined length of name and surname is less than or equal to 30 characters
        if(($name + $surname).Length -le 30) {
            $displayName = "$name $surname"
            $userPrincipalName = "${name}.${surname}@itcon.com"
            $samAccountName = "${name}${surname}"
            $accountPassword = ConvertTo-SecureString 'P@ssword123' -AsPlainText -Force

            # Create the new user in the specified OU
            New-ADUser -Name $displayName -GivenName $name -Surname $surname -DisplayName $displayName -UserPrincipalName $userPrincipalName -SamAccountName $samAccountName -Path $OU -AccountPassword $accountPassword -Enabled $true -PassThru
        } else {
            Write-Host "Error: The combined length of $name and $surname exceeds 30 characters." -ForegroundColor Red
        }
    }

    # Output a message indicating that the users have been created
    Write-Host 'User creation process has completed!' -ForegroundColor Green