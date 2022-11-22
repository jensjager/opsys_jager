1. Masina nime (hostname), PowerShelli versiooni ja Windowsi versiooni
```
$hostname = hostname 
$Pversion = $PSVersionTable.PSVersion 
$Wversion = Get-Computerinfo | select windowsversion 
"Hostname: "+ $hostname | Out-File C:\Users\jens\Desktop\test.txt 
"Powershell Version: "+ $Pversion 1 Add-Content C:\Users\jens\Desktop\test.txt 
$Wversion | Add-Content C:\Users\jens\Desktop\test.txt 
```

2. Võrgu konfiguratsioon (IP-aadress, võrgu mask (network mask), gateway, kas DHCP on lubatud ja MAC aadress (vihje vaata näidet juhendist).
```
Get-WmiObject Win32_NetworkAdapterConfiguration -Filter "IPEnabled='True'" | Select-Object DHCPEnabled, MACAddress, Description, IPAddress, IPSubnet, DefaultIPGateway | Sort-Object DHCPEnabled | Format-List | Out-File -FilePath "C:\Users\jens\Desktop\test.txt"
```

3. Arvuti protsessori kirjeldus ja põhimälu RAM kogus (leiab: Win32_ComputerSystem)
```
Get-CimInstance -ClassName Win32_ComputerSystem | select TotalPhysicalMemory, Description | Format-List | Out-File -FilePath "C:\Users\jens\Desktop\test.txt"
```

4. Graafikakaardi nimi, draiveri versioon, kuupäev ja ekraani lahutus (märksõna VideoController)
```
Get-CimInstance -ClassName Win32_VideoController -Property * | select Name, DriverVersion, DriverDate, VideoModeDescription | Format-List | Out-File -FilePath "C:\Users\jens\Desktop\test.txt"
```

5. Arvuti kõvaketaste informatsioon (partitisoonitabel, mitu GB on arvuti kettad mahutavuselt, mitu GB vaba ruumi on C: kettal)
```
Get-CimInstance -ClassName Win32_VideoController -Property * | select Name, DriverVersion, DriverDate, VideoModeDescription | Format-List | Out-File -FilePath "C:\Users\jens\Desktop\test.txt"
```

6. PCI siinil olevate seadmete draiverite info (kirjeldus, tootja ja versioon) (Vihje: vaata pikka PDF juhendit, seal on näide olemas)
```
Get-WmiObject –Class Win32_PnpSignedDriver | Where-Object {$_.DeviceID –like „PCI*“}| Select-Object Description, DriverVersion, DriverProviderName | Format-List | Out-File -FilePath "C:\Users\jens\Desktop\test.txt"
```

7. Arvutis olevad kasutajad (nimi, kirjeldus, kas on lokaalne kasutaja (LocalAccount) ja kas on keelatud (Disabled))
```
Get-LocalUser | select Name, Description, PrincipalSource, Enabled | Format-List | Out-File -FilePath "C:\Users\jens\Desktop\test.txt"
```

8. Käimasolevate protsesside arv
```
(Get-Process).Count| Format-List | Out-File -FilePath "C:\Users\jens\Desktop\test.txt"
```

10. 10 viimasena käivitatud protsessi (nimi, PID ja käivitamise aeg (StartTime). Sorteerimise aluseks võtta StartTime parameeter.
```
Get-Process | select name, id, starttime | Sort-Object starttime | Select-Object -Last 10 | Format-List | Out-File -FilePath "C:\Users\jens\Desktop\test.txt"
```

12. Arvuti kuupäev ja kellaaeg.
```
Get-Date | Format-List | Out-File -FilePath "C:\Users\jens\Desktop\test.txt"
```
