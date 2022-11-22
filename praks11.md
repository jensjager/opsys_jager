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

4. 
