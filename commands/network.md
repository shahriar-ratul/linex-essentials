# Networking & Remote Access

## Connectivity & Info

ping google.com             // check connectivity/latency to a host (Ctrl+C to stop)
ip a                         // show network interfaces and IP addresses (modern)
ifconfig                     // show network interfaces (older, may need install)
hostname                     // show this machine's hostname
hostname -I                  // show this machine's IP address(es)
netstat -tulnp               // show listening ports and the processes using them (older)
ss -tulnp                    // show listening ports and processes (modern replacement for netstat)
traceroute google.com        // show the network path (hops) to a host

## Transferring Data

curl https://example.com               // fetch a URL, print response to terminal
curl -O https://example.com/file.zip   // download a file, keep its original name
curl -I https://example.com            // fetch headers only
wget https://example.com/file.zip      // download a file
scp file.txt user@host:/path/          // copy a file to a remote server over SSH
scp -r folder user@host:/path/         // copy a folder recursively over SSH
rsync -avz src/ user@host:/dest/       // sync files/folders efficiently (only changes)

## Remote Login

ssh user@host                 // log in to a remote server
ssh -i key.pem user@host       // log in using a specific private key
ssh -p 2222 user@host          // log in on a non-default port
ssh-keygen -t ed25519          // generate a new SSH key pair
ssh-copy-id user@host           // copy your public key to a remote server for passwordless login
