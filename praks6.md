1. Käivita gedit käsurealt, nüüd peata programmi töö ajutiselt CTRL+Z klahvikombinatsiooniga, veendu et gediti aken on hangunud, seejärel saada talle SIGCONT signaal ning veendu, et gediti aken toimib jälle. Pane oma vikilehele ekraanitõmmis käskude käivitamisest oma terminaliaknas.

![image](https://user-images.githubusercontent.com/92860669/197034328-c614ce4d-3ece-4acd-9817-fb2cfa5ba364.png)

2. Käivita gedit taustal & võtmega, saada sellele SIGHUP signaal ja veendu, et aken sulgus. Seejärel käivita gedit nohup käsuga, saada sellele uuesti SIGHUP signaal ning veendu, et gedit jääb käima. Nüüd sisesta käsk millega saad nohup käivitatud gedit protsessi sulgeda. Pane oma vikilehele ekraanitõmmis käskude käivitamisest oma terminaliaknas, sh tõestuseks protsessi kadumise või allesjäämise kohta ps käsu väljund.

![image](https://user-images.githubusercontent.com/92860669/197043678-413c43db-d5bc-43c6-82d8-394032a92701.png)

3. Koosta ja lisa wikisse käsujada, mis kuvab (modifitseerib) ps -axu | grep daemon väljundi nii et tulemuseks oleksid ainult programminimed koos lisaparameetritega

Käsk: ps -axu | tr -s " " | cut -d" " -f11- | grep daemon
![image](https://user-images.githubusercontent.com/92860669/197044997-4fcdbf3c-7d71-4c43-be47-166c24e89d0d.png)

4. Koosta ja lisa wikisse käsujada (ip a | grep ...| ... | cut ... jne), mis kuvab ekraanile vastuseks ainult arvuti ip aadressi (enamasti 10.0.2.15) ip a käsu väljundi põhjal.

Käsud:
ps -axu | tr -s " " | cut -d" " -f11- | grep snap

ip address show dev enp0s3 | grep "inet " | cut -d" " -f8-8

ip address show dev enp0s3 | grep "inet " | cut -d" " -f8-8 >ipaddress.txt

xargs -n1 ping -c 2 -b < ipaddress.txt

![image](https://user-images.githubusercontent.com/92860669/197053559-dfc99796-3f97-479f-8590-71836ca92aba.png)
