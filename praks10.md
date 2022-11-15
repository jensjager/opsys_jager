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

Ülesanne 5:
```
#!/bin/bash
IFS=$'\n'

echo "Sisesta protsessi nimi:"
read CMD
for line in $(ps -A | grep $CMD)
do
    id=$(echo $line | tr -s ' ' | cut -d ' ' -f2)
    name=$(echo $line | tr -s ' ' | cut -d ' ' -f5)
    echo "PID: $id name: $name"
done
```
![image](https://user-images.githubusercontent.com/92860669/201931351-a556976c-4f0c-46c2-94b7-8ea0d79bcc1c.png)

Ülesanne 6:
```
#!/bin/bash
astandamine () {
    a=1
    for i in $(seq $2 $END)
    do
        a=$(($a*$1))
    done
    echo $a
}

echo "Sisesta astendatav: "
read astendatav
echo "Sisesta astendaja: "
read astendaja

echo $(astandamine $astendatav $astendaja)
```

![image](https://user-images.githubusercontent.com/92860669/201934063-f0702229-abc0-4f63-b9c1-ed9ac45daeb1.png)
