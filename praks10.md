Ülesanne 3:
```
#!/bin/sh -x

echo "Sisesta oma nimi:"

read nimi

echo "Sisesta oma eriala:"

read eriala

echo "Sisesta oma matrikli number:"

read matrikkel

echo "Tere $nimi, sa õpid $eriala ning su matrikkel on $matrikkel"
```
![image](https://user-images.githubusercontent.com/92860669/201925826-c24d6280-bdc3-4ae5-9652-57a9b896f4c1.png)

Ülesanne 4:
```
#!/bin/bash -x
echo "Sisesta laiend mida muuta:"
read A
echo "Sisesta laiend milleks muuta:"
read B
for i in $(ls)
do
    if [ ${i##*.} = $A ]
    then
        mv $i ${i/$A/$B}
    fi
done
```

![image](https://user-images.githubusercontent.com/92860669/201926468-87e00e76-8010-4c55-97d8-6987002235df.png)
