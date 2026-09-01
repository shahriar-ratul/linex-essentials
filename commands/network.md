# 🌐 Networking & Remote Access

## 📡 Connectivity & Info

Check connectivity/latency to a host (`Ctrl+C` to stop)

```bash
ping google.com
```

Show network interfaces and IP addresses (modern)

```bash
ip a
```

Show network interfaces (older, may need install)

```bash
ifconfig
```

Show this machine's hostname

```bash
hostname
```

Show this machine's IP address(es)

```bash
hostname -I
```

Show listening ports and the processes using them (older)

```bash
netstat -tulnp
```

Show listening ports and processes (modern replacement for netstat)

```bash
ss -tulnp
```

Show the network path (hops) to a host

```bash
traceroute google.com
```

## 📤 Transferring Data

Fetch a URL, print response to terminal

```bash
curl https://example.com
```

Download a file, keep its original name

```bash
curl -O https://example.com/file.zip
```

Fetch headers only

```bash
curl -I https://example.com
```

Download a file

```bash
wget https://example.com/file.zip
```

Copy a file to a remote server over SSH

```bash
scp file.txt user@host:/path/
```

Copy a folder recursively over SSH

```bash
scp -r folder user@host:/path/
```

Sync files/folders efficiently (only changes)

```bash
rsync -avz src/ user@host:/dest/
```

## 🔑 Remote Login

Log in to a remote server

```bash
ssh user@host
```

Log in using a specific private key

```bash
ssh -i key.pem user@host
```

Log in on a non-default port

```bash
ssh -p 2222 user@host
```

Generate a new SSH key pair

```bash
ssh-keygen -t ed25519
```

Copy your public key to a remote server for passwordless login

```bash
ssh-copy-id user@host
```
