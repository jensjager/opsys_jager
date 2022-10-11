Praktikum 5 vastused:

1. Missuguseid õigusi (r,w,x) on Unixis omanikul (u) minimaalselt vaja (d - directory, f - fail). Grupiõigusi (g) ja ülejäänute others (o) õigusi ei ole siin vaja määrata ainult kausta/faili omaniku (user) õigusi.

a) kataloogile /d faili /d/f lugemiseks - Kataloogil on vaja "execute" (x) õigust.
b) failile /d/f faili /d/f lugemiseks - Failil on vaja "read" (r) õigust.
c) kataloogile /d faili /d/f kustutamiseks - Kataloogi kustutamiseks on vaja "write" (w) õigust.
d) failile /d/f faili /d/f kustutamiseks? - Faili kustutamiseks on vaja "write" (w) õigust.

2. Miks chmod a=x skriptifail ei ole piisav õigus shelli skriptifaili käivitamiseks? Millist õigust lisaks käivitamisele veel vaja läheb skriptifaili käivitamiseks? Põhjendage lühidalt? - Skriptifaili käivitamiseks läheb veel vaja faili lugemisõigust, sest masin peab suutma skripti lugeda.

3. Milleks on kasulik see, et igal kasutajal on omanimeline grupp? - Selle eesmärk on leevendada turvaprobleeme, uus loodud kasutaja pannes tema oma gruppi, kus on tal oma õigused, mille määrab "umask".

4. Milliseid on minimaalsed õigused (rwx), mis on vajalikud teie tavakasutajal (kuulub gruppi majasisene) (mitte root või peeter kasutajal, kausta ja faili omanikud) uusfail.txt sisu kuvamiseks. Esita ekraanivaade id, ls -la ja cat uusfail.txt käskude väljundist tõestamaks lahendust. 

![image](https://user-images.githubusercontent.com/92860669/192531475-27941f1d-efd5-4fbc-8b38-e3552106a059.png)

5. Tehke screenshot tulemusest, kus oleks näha hinded.txt failiõigused ja jukuisa käivituskäsk koos väljundiga ning lisage see oma viki lehele. Milleks on vaja setuid õigust? - setuid kasutatakse et anda õiguseid teisele kasutajale, et teine kasutaja saaks kasutada rakendusi.

![image](https://user-images.githubusercontent.com/92860669/195081250-69e98239-18cc-4990-95c9-da65e2aa7d8d.png)

6. Kas setuid või setgid kasutamine võib vähendada süsteemi turvalisust? Kui jah, siis kuidas? - setuid ja setgid võivad anda valele kasutajale juurjuurdepääsu või juurdepääsu programmi käitamiseks.

7. Kirjutage oma viki lehele kõik kasutajaid, kes saavad sticky bit õigustega yhiskaust kataloogist nüüd peeter kasutaja loodud faile kustutada. (vihje: õige vastus sisaldab vähemalt 3 eri kasutajat). - peeter, opetaja, root

8. Uurige käsuga ls -la faili hinded.txt õigusi - mida märkate? Seejärel uurige õigusi täpsemalt, kasutades käsku getfacl ning kopeerige see tulemus oma vikilehele.

Omanikul ja grupil on read ja write õigused ning pluss märk lõpus tähendab, et on veel ACL õigused.

/# file: hinded.txt
/# owner: opetaja
/# group: opetaja
user::rw-
group::---
group:direktor:rw-
mask::rw-
other::---

9. Kes saab chattr +i parameetriga faili sisu modifitseerida (kirjutada)? Milliste käskudega saate kustutada testfail-2 nimelise faili (ehk kuidas siiski kustutada +i parameetriga faili). - mitte keegi ei saa selle faili sisu modifitseerida
