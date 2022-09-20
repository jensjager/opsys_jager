| Küsimus                                         | Linux                                                                  | Linuxis kasutatud käsklus                                 |
|-------------------------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------|
| Mitu protsessi kokku arvutis käib?              | 203                                                                    | ps -aux \| wc -l                                          |
| Milline on kõige esimesena käivitatud protsess? | /sbin/init splash                                                      | ps axo pid,cmd,comm,etime                                 |
| Milliste kasutajate protsesse arvutis käib?     | avahi, colord, jens, kernoops, message+, root, rtkit, syslog, systemd+ | ps aux \| awk '{ print $1 }' \| sed '1 d' \| sort \| uniq |
| Kui kaua on arvuti järjest töötanud (up time) ? | 1h 3min                                                                | uptime                                                    |
