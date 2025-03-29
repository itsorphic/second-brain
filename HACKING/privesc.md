# Privilege Escalation

**List available sudo privileges**
```bash
sudo -l
```
To run a command with `sudo`: `sudo -u user /bin/echo Hello World!`

**Create a new SSH key**
```bash
ssh-keygen -f key

# Add the generated public key to the user
echo "ssh-rsa AAAAB...SNIP...M= user@parrot" >> /root/.ssh/authorized_keys

# SSH to the server with the generated private key
ssh root@10.10.10.10 -i key
```
