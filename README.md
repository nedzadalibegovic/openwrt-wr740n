# OpenWrt builds for TP-Link TL-WR740N v4

OpenWrt builds for the TP-Link TL-WR740N v4 with removed PPPoE and IPv6 support.

All builds are compiled using the docker imagebuilder image:
```bash
docker run --rm -v "$(pwd)"/bin/:/home/build/openwrt/bin -it openwrtorg/imagebuilder:ath79-tiny-19.07.7
sudo make image PROFILE="tplink_tl-wr740n-v4" PACKAGES="uhttpd uhttpd-mod-ubus libiwinfo-lua luci-base luci-app-firewall luci-mod-admin-full luci-theme-bootstrap -ppp -ppp-mod-pppoe -ip6tables -odhcp6c -kmod-ipv6 -kmod-ip6tables -odhcpd-ipv6only"
```
