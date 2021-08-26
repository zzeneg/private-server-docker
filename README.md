# private-server-docker
Docker-compose for a private server

## Components
- [OpenVPN server](https://github.com/kylemanna/docker-openvpn) on 443 UDP port with TCP fallback so it works on every network
- [L2TP/IPSec PSK VPN](https://github.com/hwdsl2/docker-ipsec-vpn-server) which is natively supported by most OS's
- [AdGuardHome](https://github.com/AdguardTeam/AdGuardHome) to serve as Android adblocker by using Private DNS and DNS-over-TLS
- [Portainer](https://github.com/portainer/portainer) to control/view all Docker containers
- [Traefik](https://github.com/traefik/traefik) as a reverse-proxy with [OAuth authentication](https://github.com/thomseddon/traefik-forward-auth) to protect all public-facing resources 
- example of static website served with nginx