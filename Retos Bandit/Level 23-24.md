# Level 23-24
## Objetivo

A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…
## Datos de acceso al nivel

> [!IMPORTANT]
> **Host:** bandit.labs.overthewire.org
> **User:** bandit23
> **Password:** QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
> **Port:**  2220
## Solución

``` shell
C:\Users\Marco De Avila>ssh bandit23@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit23@bandit.labs.overthewire.org's password:
bandit23@bandit:~$ cd /etc/cron.d/
bandit23@bandit:/etc/cron.d$ ls
cronjob_bandit15_root  cronjob_bandit22  cronjob_bandit24       e2scrub_all  sysstat
cronjob_bandit17_root  cronjob_bandit23  cronjob_bandit25_root  otw-tmp-dir
bandit23@bandit:/etc/cron.d$ cat cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:/etc/cron.d$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo || exit 1
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -rf ./$i
    fi
done

bandit23@bandit:/etc/cron.d$ which bash
/usr/bin/bash
bandit23@bandit:/etc/cron.d$ ls -la
total 56
drwxr-xr-x   2 root root  4096 Apr 23 18:05 .
drwxr-xr-x 108 root root 12288 Aug 12 08:42 ..
-rw-r--r--   1 root root    62 Apr 23 18:04 cronjob_bandit15_root
-rw-r--r--   1 root root    62 Apr 23 18:04 cronjob_bandit17_root
-rw-r--r--   1 root root   120 Apr 23 18:04 cronjob_bandit22
-rw-r--r--   1 root root   122 Apr 23 18:04 cronjob_bandit23
-rw-r--r--   1 root root   120 Apr 23 18:04 cronjob_bandit24
-rw-r--r--   1 root root    62 Apr 23 18:04 cronjob_bandit25_root
-rw-r--r--   1 root root   201 Jan  8  2022 e2scrub_all
-rwx------   1 root root    52 Apr 23 18:05 otw-tmp-dir
-rw-r--r--   1 root root   102 Mar 23  2022 .placeholder
-rw-r--r--   1 root root   396 Feb  2  2021 sysstat
bandit23@bandit:/etc/cron.d$ cat /var/spool/bandit24/foo
cat: /var/spool/bandit24/foo: Permission denied
bandit23@bandit:/etc/cron.d$ cd /var/spool/bandit24/foo
bandit23@bandit:/var/spool/bandit24/foo$ ls
ls: cannot open directory '.': Permission denied
bandit23@bandit:/var/spool/bandit24/foo$ mkdir /tmp/tux
bandit23@bandit:/var/spool/bandit24/foo$ cd /tmp/tux
bandit23@bandit:/tmp/tux$ nano script.sh
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/tmp/tux$ ls
script.sh
bandit23@bandit:/tmp/tux$ ls -la
total 10564
drwxrwxr-x   2 bandit23 bandit23     4096 Sep 23 23:46 .
drwxrwx-wt 697 root     root     10801152 Sep 23 23:47 ..
-rw-rw-r--   1 bandit23 bandit23       63 Sep 23 23:46 script.sh
bandit23@bandit:/tmp/tux$ cat script.sh
#!/bin/bash

cat /etc/bandit_pass/bandit24 > /tmp/tux/password
bandit23@bandit:/tmp/tux$ touch password
bandit23@bandit:/tmp/tux$ ls
password  script.sh
bandit23@bandit:/tmp/tux$ ls -la
total 10564
drwxrwxr-x   2 bandit23 bandit23     4096 Sep 23 23:47 .
drwxrwx-wt 697 root     root     10801152 Sep 23 23:47 ..
-rw-rw-r--   1 bandit23 bandit23        0 Sep 23 23:47 password
-rw-rw-r--   1 bandit23 bandit23       63 Sep 23 23:46 script.sh
bandit23@bandit:/tmp/tux$ chmod 777 -R /tmp/tux
bandit23@bandit:/tmp/tux$ ls -l
total 4
-rwxrwxrwx 1 bandit23 bandit23  0 Sep 23 23:47 password
-rwxrwxrwx 1 bandit23 bandit23 63 Sep 23 23:46 script.sh
bandit23@bandit:/tmp/tux$ cp script.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/tux$ cat password
bandit23@bandit:/tmp/tux$ cat password
bandit23@bandit:/tmp/tux$ date
Sat Sep 23 11:50:35 PM UTC 2023
bandit23@bandit:/tmp/tux$ date
Sat Sep 23 11:50:43 PM UTC 2023
bandit23@bandit:/tmp/tux$ cat password
bandit23@bandit:/tmp/tux$ cat password
bandit23@bandit:/tmp/tux$ cat password
bandit23@bandit:/tmp/tux$ cat password
bandit23@bandit:/tmp/tux$ date
Sat Sep 23 11:51:01 PM UTC 2023
bandit23@bandit:/tmp/tux$ cat password
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
bandit23@bandit:/tmp/tux$ exit
```

**Password encontrado:** VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
## Notas adicionales

No entendí el material de la clase pero seguí un video para resolverlo.
## Referencias

[(21) OverTheWire | Bandit (Nivel 23) - YouTube](https://www.youtube.com/watch?v=lPtL7kqLyDA&list=PLuYfa_nCnOPURyDp4aDT4TIhKr2XqxgLd&index=8)