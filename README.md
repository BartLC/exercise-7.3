Maak een nieuwe gebruiker aan ind e standaard container USERS. Met een script pas je de volgende zaken aan:

1° Maakt een nieuwe groep 'Sales' aan in de OU Sint-Niklaas

2° Verplaats de aangemaakte gebruiker naar de OU Sint-Niklaas

3° Vul de eigenschap Department met de waarde 'Sales'

4° Maak de gebruiker lid van de groep 'Sales'



New-ADGroup -GroupScope Global -Name Sales -Path "ou=Sint-Niklaas, dc=MediaTech, dc=lan"
Add-ADGroupMember -Identity Sales -Members BLC
Set-ADUser -Identity BEP -Department Sales
Add-ADGroupMember -Identity IT -Members BLC
