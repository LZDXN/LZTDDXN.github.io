https://github.com/hwdsl2/setup-ipsec-vpn/blob/master/docs/clients.md#configure-linux-vpn-clients-using-the-command-line

## Start VPN connection(At home):
```shell
#Create xl2tpd control file:
mkdir -p /var/run/xl2tpd
touch /var/run/xl2tpd/l2tp-control

#Restart services:
service strongswan restart
service xl2tpd restart

# Ubuntu and Debian
ipsec up myvpn
echo "c myvpn" \> /var/run/xl2tpd/l2tp-control

#Check existing route
ip route

#Exclude your VPN server's IP from the new default route
route add 47.240.54.55 gw 192.168.3.1

#(If remote server, uncomment this)
route add 120.235.12.223 gw 192.168.3.1

#Add a new default route to start routing traffic via the VPN server：
route add default dev ppp0

#Finally, verify that if traffic is being routed properly
wget -qO- http://ipv4.icanhazip.com; echo

```

Without comment:
```shell
mkdir -p /var/run/xl2tpd
touch /var/run/xl2tpd/l2tp-control
service strongswan restart
service xl2tpd restart
ipsec up myvpn
echo "c myvpn" > /var/run/xl2tpd/l2tp-control
ip route
route add 47.240.54.55 gw 192.168.3.1
route add 120.235.12.223 gw 192.168.3.1

route add default dev ppp0
wget -qO- http://ipv4.icanhazip.com; echo
```

## Stop the VPN connection:
```shell
route del default dev ppp0
# Ubuntu and Debian
echo "d myvpn" \> /var/run/xl2tpd/l2tp-control
ipsec down myvpn
```