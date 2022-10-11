Praktikum 5 vastused:

Missuguseid õigusi (r,w,x) on Unixis omanikul (u) minimaalselt vaja (d - directory, f - fail). Grupiõigusi (g) ja ülejäänute others (o) õigusi ei ole siin vaja määrata ainult kausta/faili omaniku (user) õigusi.

a) kataloogile /d faili /d/f lugemiseks - Kataloogil on vaja "execute" (x) õigust.
b) failile /d/f faili /d/f lugemiseks - Failil on vaja "read" (r) õigust.
c) kataloogile /d faili /d/f kustutamiseks - Kataloogi kustutamiseks on vaja "write" (w) õigust.
d) failile /d/f faili /d/f kustutamiseks? - Faili kustutamiseks on vaja "write" (w) õigust.

Miks chmod a=x skriptifail ei ole piisav õigus shelli skriptifaili käivitamiseks? Millist õigust lisaks käivitamisele veel vaja läheb skriptifaili käivitamiseks? Põhjendage lühidalt? - Skriptifaili käivitamiseks läheb veel vaja faili lugemisõigust, sest masin peab suutma skripti lugeda.

Miks on igal kasutajal omanimeline grupp? - Selle eesmärk on leevendada turvaprobleeme, uus loodud kasutaja pannes tema oma gruppi, kus on tal oma õigused, mille määrab "umask".

Milliseid on minimaalsed õigused (rwx), mis on vajalikud teie tavakasutajal (kuulub gruppi majasisene) (mitte root või peeter kasutajal, kausta ja faili omanikud) uusfail.txt sisu kuvamiseks. Esita ekraanivaade id, ls -la ja cat uusfail.txt käskude väljundist tõestamaks lahendust. 

![image](https://user-images.githubusercontent.com/92860669/192531475-27941f1d-efd5-4fbc-8b38-e3552106a059.png)

Tehke screenshot tulemusest, kus oleks näha hinded.txt failiõigused ja jukuisa käivituskäsk koos väljundiga ning lisage see oma viki lehele. Milleks on vaja setuid õigust?
<img width="371" alt="image" src="https://user-images.githubusercontent.com/92860669/195081250-69e98239-18cc-4990-95c9-da65e2aa7d8d.png">
