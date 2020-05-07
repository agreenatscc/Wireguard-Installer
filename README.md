# Wireguard-Installer
 WireGuard installer for Ubuntu, Debian, Fedora, CentOS, Arch Linux
 
 WireGuard installer
This project is a bash script that aims to setup a WireGuard VPN on a Linux server, as easily as possible!

WireGuard is a point-to-point VPN that can be used in different ways. Here, we mean a VPN as in: the client will forward all its traffic trough an encrypted tunnel to the server. The server will apply NAT to the client's traffic so it will appear as if the client is browsing the web with the server's IP.

The script supports both IPv4 and IPv6. Please check the issues for ongoing development, bugs and planned features!

WireGuard does not fit your environment? Check out openvpn-install.

Requirements
Supported distributions:

Ubuntu
Debian
Fedora
CentOS
Arch Linux
I recommend these cheap cloud providers for your VPN server:

Vultr: Worldwide locations, IPv6 support, starting at $3.50/month
PulseHeberg: France, unlimited bandwidth, starting at €3/month
Digital Ocean: Worldwide locations, IPv6 support, starting at $5/month
Usage
Download and execute the script. Answer the questions asked by the script and it will take care of the rest.

curl -O https://raw.githubusercontent.com/agreenatscc/Wireguard-Installer/master/wireguard-install.sh
chmod +x wireguard-install.sh
./wireguard-install.sh
It will install WireGuard (kernel module and tools) on the server, configure it, create a systemd service and a client configuration file.

To generate more client files, run the following:

./wireguard-install.sh add-client
Make sure you choose different IPs for you clients.

Contributions are welcome!
