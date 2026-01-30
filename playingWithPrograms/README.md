# Ethical Considerations
Remember that hacking into devices without permission is illegal and unethical.\
Always ensure you have the necessary permissions and are conducting these activities in a\
controlled environment for educational or security assessment purposes.

# Playing with programs
## Talking web

<details>
<summary style="cursor:pointer">HTTP (netcat)</summary>

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

<details>
<summary style="cursor:pointer">HTTP Paths (netcat)</summary>

```
cat /challenge/server >> find /task
```  
How to:
```
nc -v 127.0.0.1 80
[Success]
GET /task HTTP/1.1
[Flag]
```
</details>

<details>
<summary style="cursor:pointer">HTTP (curl)</summary>
Next, we'll practice making HTTP requests with one of the most common commandline tools for HTTP: curl.
Unlike netcat, curl is made specifically for HTTP, and you don't have to write raw HTTP commands.
Instead, you must learn to use the right program options to achieve what you want.
Here, you must simply make a GET request to the right endpoint!

How to:
```
curl http://challenge.localhost/trial
```  

```
127.0.0.1 - - [30/Jan/2026 22:43:30] "GET /trail HTTP/1.1" 404 - <<< I AM DUMP typo.
127.0.0.1 - - [30/Jan/2026 22:44:16] "GET / HTTP/1.1" 404 -
127.0.0.1 - - [30/Jan/2026 22:45:54] "GET /trial HTTP/1.1" 200 - <<<< CORRECT
```
</details>

<details>
<summary style="cursor:pointer">HTTP (python)</summary>
Finally, we'll learn the fourth tool in our HTTP toolbox: Python's requests library.
This, along with the browser, will likely be the two most heavily used tools in your HTTP toolbox. 
Requests lets you script complex web interactions, and this will be necessary to pull off tricky hacks later. 
For now, things are simple: pull up Python, import requests, and GET the flag!

- start the server in an extra Terminal.
- use "cat /challenge/server" to know which site to GET

How to "one-liner":
```
python3 -c 'import requests; r = requests.get("http://challenge.localhost/task"); print(r.text)'
```  
or as script:
```
import requests
r = requests.get("http://challenge.localhost/task")
print(r.text)
```
</details>

<details>
<summary style="cursor:pointer">HTTP Host Header (python)</summary>

```
import requests
r = requests.get("http://challenge.localhost/task")
print(r.text)
```
</details>
