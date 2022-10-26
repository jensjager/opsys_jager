1.  Miks andmekandjad vajavad lähtestamist? (sisukas vastus võiks omada põhjendust)

Esiteks lähtestamine on vajalik ainult siis, kui ketas on uus ja sellel pole failisüsteeme. Lähtestamise eesmärgiks on valmistada andmekandja windowsi kasutamiseks. Pärast lähtestamist on võimalik luua partitsioone kettale ning neid vormindada.

2.  Millised on GPT kasutamise eelised ja puudused võrreldes MBR'iga? (välja tuua vähemalt 3 eelist)

GPT võimaldab lõpmatult palju partitsiooni, kuid MBR võimaldab maksimaalselt 4.
MBR maksimaalne kettaruum on 2TB, kuid GPT on miljonites kordades suurem.
GPT ei tööta vanemate windows versioonide peal, kuid MBR töötab.
MBR salvestab kogu info ühte kohta, võrreldes GPT-ga, mis salvestab erinevatesse kettaaladele. Seega andmekorruptsiooni korral on GPT parem.

3.  Lisage link https://kodu.ut.ee/~TÜ_kasutajatunus/hdd.png praktikumi aruandesse tõestuseks, et olete Ülesande TÜ võrguketta haakimine Windowsis edukalt lahendanud.

https://kodu.ut.ee/~jensjaag/hdd.png

4.  Lisage ls -la /mnt/ut/public_html käsu väljundi pilt aruandesse

![image](https://user-images.githubusercontent.com/92860669/197867514-21aa615c-0bd4-4a9d-a0e6-d8dd3134ac5f.png)


5.  Mida mõjutasid mount käsu parameetrid "-o ro" ja "-t auto"?

"-o ro" - paneb root, ehk juurkausta read-only

"-t auto" - automaatselt leiab, kus kohas kasutatav failisüsteem on seadmes

6.  mount käsu väljundist leidke üles, mis väärtusega Ubuntu asendas auto parameetri?

NTFS

7.  Tehke ekraanipilt /etc/fstab faili sisust pärast iseseisva ülesande lahendamist (või muu tõestus/seadistamise juhend, et 4TB ketas haagitaks automaatselt kausta /mnt/bigdata Ubuntu käivitamisel).

![image](https://user-images.githubusercontent.com/92860669/198029785-0b204755-aaeb-4790-8c76-532760e2f272.png)
