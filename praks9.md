1. Võrrelge Administrator ja SYSTEM privileege ning kirjutage vähemalt üks tegevus mille jaoks on vaja SYSTEM õigusi.

![image](https://user-images.githubusercontent.com/92860669/200566359-a8ab2a74-d038-404b-b609-961da6d37af1.png)

Näiteks SeTimeZonePrivilege, ehk Time Zone-i saab muuta SYSTEM privileegidega, kuid mitte Administratorina.

2. Ekraanivaade turvalise kausta seadetest (ainult üks kasutaja saab teha kõike ja Ülemus ainult lugeda)

![image](https://user-images.githubusercontent.com/92860669/200574905-78b3d69b-05dc-43c8-8100-7acad502e872.png)

3. Kirjuta praktikumi aruandesse vähemalt 3 soovitust (muudatust), mida Microsoft soovitab Windowsi turve seadete juures parandada, suurendamaks Windows operatsioonisüsteemi turvalisust.

Esiteks Microsoft soovitab Windowsi turve seadete juures esiteks teha ohu kiirkontroll, sest seda varem poldud tehtud.
Teiseks ta soovitab logida sisse Microsoft kontoga, turvalisuse ning muude eelistuste huvides.
Kolmandaks Microsoft soovitab tuumade isoleerimist.

4. Sobiv kasutajakonto kontrolli seadistus koos põhjendusega (Süsteem ja turve)

![image](https://user-images.githubusercontent.com/92860669/200578299-80354c22-bca6-42e1-9382-b088cda04361.png)

Valisin maksimaalse kasutajakonto kontrolli, sest kunagi ei tea mis tarkvara kästakse installida praktikumi juhendajate poolt ning olen seetõttu rohkem kaitstud.

5. Kirjelda 3 Local Security Policy lisaseadistust turvalisuse tagamiseks, koos põhjendustega.

  1) Minimum password length	8 characters - Lühike parool on väga kergesti sissetungitav ning mitteturvaline.
  2) Audit account management	Success - When creating accounts or groups, it is a good habit to audit it in order to catch new account creations without your consent.
  3) Password must meet complexity requirements	Enabled - Long passwords are easily crackable when they don't include any numbers or specialised characters.

6. Minimaalselt 2 ekraanivaadet testimise käigus esinenud keeluteavitustest, koos selgitusega mida ning millise kasutajaga tehti.

![image](https://user-images.githubusercontent.com/92860669/200590376-135362ab-5407-4d22-aeaf-069ee1152668.png)
5 valet paroolisisestust.

![image](https://user-images.githubusercontent.com/92860669/200591340-5ef0830a-6d9b-469d-b964-04153f3074d8.png)
tootaja1 kasutajana üritamas ligi pääseda tootaja2 kasutaja kausta.

7. Ekraanivaade Event Vieweri aknast, kus näha ebaõnnestunud sisselogimiskatsete logikirje

![image](https://user-images.githubusercontent.com/92860669/200594118-c27cf16e-b06b-4558-a75a-f047e7b9544e.png)

8. Tehke ekraanivaade DisplayLastLogonInfo registrivõtmest koos väärtusega 1.

![image](https://user-images.githubusercontent.com/92860669/200596281-df4e3216-fc60-4ca5-b2e7-1ae8194197b8.png)
