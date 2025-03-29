# Enumeration

**Grab Website Banner**
```bash
curl -IL https://www.inlanefreight.com
```

**Directory scan**
```bash
gobuster dir -u http://10.10.10.121/ -w /usr/share/dirb/wordlists/common.txt
```

**Sub-domain scan**
```bash
gobuster dns -d inlanefreight.com -w /usr/share/SecLists/Discovery/DNS/namelist.txt
```

**Webserver / Certificates details**
```bash
whatweb 10.10.10.121
```

Check potential directories in `robots.txt` : `curl 10.10.10.121/robots.txt`
