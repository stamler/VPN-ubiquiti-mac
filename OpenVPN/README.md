# OpenVPN between Ubiquiti EdgeRouter and macOS with p2p and shared secret

1. SSH into the EdgeRouter and run the commands in EdgeRouter.commands, substituting values appropriate for your situation (i.e. different IPs or firewall config)
2. Copy the key generated in step 1 to the mac as follows:
    1. `sudo cat /config/auth/openvpn.static.secret`
    2. copy the text to a new file on the mac and name it static.key
3. On the mac, brew install openvpn
4. copy MacClient.ovpn to the same directory as static.key from step 2.2
5. Make the directory in step 4 your working directory (`cd`).
5. `sudo openvpn MacClient.ovpn`
