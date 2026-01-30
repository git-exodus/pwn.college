# Ethical Considerations
Remember that hacking into devices without permission is illegal and unethical.\
Always ensure you have the necessary permissions and are conducting these activities in a\
controlled environment for educational or security assessment purposes.

# Playing with programs
## Talking web

<details>
<summary style="cursor:pointer">HTTP // netcat</summary>

- GET → I want to get something
- / → mainpage
- HTTP/1.1 → I want the HTTP-Protokoll in Version 1.1
```
hacker@talking-web~http-netcat:~$ nc -v challenge.localhost 80
Connection to challenge.localhost (127.0.0.1) 80 port [tcp/http] succeeded!
GET / HTTP/1.1           

HTTP/1.1 200 OK
Server: Werkzeug/3.0.6 Python/3.8.10
Date: Fri, 30 Jan 2026 22:15:44 GMT
Content-Type: text/html; charset=utf-8
Content-Length: 84
X-Flag: pwn.college{gu0Z....
Connection: close

```
How to:
```
nc -v ADDRESS PORT

GET / HTTP/1.0
or
GET / HTTP/1.1
```
</details>
