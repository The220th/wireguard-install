# WireGuard installer

WireGuard installer without IPv6 and client config changed.

Forked from [https://github.com/angristan/wireguard-install](https://github.com/angristan/wireguard-install).

**This project is a bash script that aims to setup a [WireGuard](https://www.wireguard.com/) VPN on a Linux server, as easily as possible!**

WireGuard is a point-to-point VPN that can be used in different ways. Here, we mean a VPN as in: the client will forward all its traffic through an encrypted tunnel to the server.
The server will apply NAT to the client's traffic so it will appear as if the client is browsing the web with the server's IP.

WireGuard does not fit your environment? Check out [openvpn-install](https://github.com/angristan/openvpn-install).

## Requirements

Supported distributions:

- AlmaLinux >= 8
- Arch Linux
- CentOS Stream >= 8
- Debian >= 10
- Fedora >= 32
- Oracle Linux
- Rocky Linux >= 8
- Ubuntu >= 18.04

## Usage

Download and execute the script. Answer the questions asked by the script and it will take care of the rest.

```bash
# ~/.local/bin must be exist and must be in $PATH
wget -O ~/.local/bin/wireguard-install https://raw.githubusercontent.com/The220th/wireguard-install/master/wireguard-install.sh && chmod u+x ~/.local/bin/wireguard-install

# And run
wireguard-install
```

It will install WireGuard (kernel module and tools) on the server, configure it, create a systemd service and a client configuration file.

Run the script again to add or remove clients!
