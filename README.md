# Cloudflare WARP Installer

A Bash script that automatically installs and configures CloudFlare WARP in Linux, connects to WARP networks with WARP official client or WireGuard.

## Features

- Automatically install CloudFlare WARP Official Linux Client
- Quickly enable WARP Proxy Mode, access WARP network with SOCKS5
- Automatically install WireGuard related components
- Configuration WARP IPv4 Network interface (WireGuard Mode)
- Configuration WARP IPv6 Network interface (WireGuard Mode)
- Configuration WARP Dual Stack Network interface (WireGuard Mode)
- ...

## Requirements

### WARP Official Linux Client

Official WARP client support is currently limited to x86_64 platforms, see OS Support for details: https://pkg.cloudflareclient.com

### WARP WireGuard Network Mode

Supported distributions:

- Debian >= 10
- Ubuntu >= 16.04
- Fedora
- CentOS
- Oracle Linux
- Arch Linux
- Other similar distributions

Supported platform architecture:

- x86(i386)
- x86_64(amd64)
- ARMv8(aarch64)
- ARMv7(armhf)

## Usage

```bash
bash <(curl -fsSL https://raw.githubusercontent.com/ReturnFI/Warp/main/warp.sh) [SUBCOMMAND]
# or
wget https://raw.githubusercontent.com/ReturnFI/Warp/main/warp.sh
bash warp.sh [SUBCOMMAND]
```

### Subcommands

```
install         Install Cloudflare WARP Official Linux Client
uninstall       uninstall Cloudflare WARP Official Linux Client
restart         Restart Cloudflare WARP Official Linux Client
proxy           Enable WARP Client Proxy Mode (default SOCKS5 port: 40000)
unproxy         Disable WARP Client Proxy Mode
masque          Set WARP tunnel protocol to MASQUE (HTTP/3)
wg              Install WireGuard and related components
wg4             Configuration WARP IPv4 Global Network (with WireGuard)
wg6             Configuration WARP IPv6 Global Network (with WireGuard)
wgd             Configuration WARP Dual Stack Global Network (with WireGuard)
wgx             Configuration WARP Non-Global Network (with WireGuard)
rwg             Restart WARP WireGuard service
dwg             Disable WARP WireGuard service
status          Prints status information
version         Prints version information
help            Prints this message
```

### Example

- Install and automatically configure the Proxy Mode feature of the WARP client, enable the local loopback port 40000, and use an application that supports SOCKS5 to connect to this port.
    ```
    bash <(curl -fsSL https://raw.githubusercontent.com/ReturnFI/Warp/main/warp.sh) proxy
    ```

- Install and automatically configure WARP IPv6 Network (with WireGuard)，Giving your Linux server access to IPv6 networks.
    ```
    bash <(curl -fsSL https://raw.githubusercontent.com/ReturnFI/Warp/main/warp.sh) wg6
    ```

- This Bash script is also a good WireGuard installer.
    ```
    bash <(curl -fsSL https://raw.githubusercontent.com/ReturnFI/Warp/main/warp.sh) wg
    ```

## Credits

- [Cloudflare WARP](https://1.1.1.1/)
- [WireGuard](https://www.wireguard.com/)
- [ViRb3/wgcf](https://github.com/ViRb3/wgcf)

## License

[MIT](https://github.com/P3TERX/warp.sh/blob/main/LICENSE)

## Notice of Non-Affiliation and Disclaimer

We are not affiliated, associated, authorized, endorsed by, or in any way officially connected with Cloudflare, or any of its subsidiaries or its affiliates. The official Cloudflare website can be found at https://www.cloudflare.com/.

The names Cloudflare Warp and Cloudflare as well as related names, marks, emblems and images are registered trademarks of their respective owners.
