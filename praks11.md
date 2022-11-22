1. Masina nime (hostname), PowerShelli versiooni ja Windowsi versiooni

![image](https://user-images.githubusercontent.com/92860669/203316691-025c1fc4-1339-44d7-b6fc-a40d3aa4af7d.png)

2. Võrgu konfiguratsioon (IP-aadress, võrgu mask (network mask), gateway, kas DHCP on lubatud ja MAC aadress (vihje vaata näidet juhendist).

Get-WmiObject Win32_NetworkAdapterConfiguration -Filter "IPEnabled='True'" | Select-Object DHCPEnabled, MACAddress, Description, IPAddress, IPSubnet, DefaultIPGateway | Sort-Object DHCPEnabled | Format-List | Out-File -FilePath "C:\Users\jens\Desktop\test.txt"
