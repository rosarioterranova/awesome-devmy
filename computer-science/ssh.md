# SSH

SSH (Secure Socket Shell) is a protocol to launch shell commands in another computer.

[Setup a Linux Machine for SSH access](https://phoenixnap.com/kb/ssh-to-connect-to-remote-server-linux-or-windows)

`ssh {user}@{host}`

You can connect to your github repo with SSH.-

## Generate public/private rsa key pair

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

You can share the pub key to anyone, but never share the private key.

1. Copy you machine's public key in the server's `.ssh` folder
2. In your machine, copy the server's public key in your .ssh folder with `ssh.add /.ssh/your_id_rsa_digitalocean`

## Secure Copy

Copy file from server to local host:

```
scp user@127.0.1.1:/home/user/test.txt .
```

Copy file to server:

```
scp test.txt user@127.0.1.1:/home/user/
```

[How to Use SCP Command to Securely Transfer Files](https://linuxize.com/post/how-to-use-scp-command-to-securely-transfer-files/)