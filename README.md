# Jarkom-Modul-4-A13-2021

## CPT - VLSM

### Topologi

![image](https://user-images.githubusercontent.com/68369091/143685136-610c9211-c151-45f6-b668-8bb9755cc605.png)

### Perhitungan

![image](https://user-images.githubusercontent.com/68369091/143685169-4e339077-7c44-4906-9f41-b7c7a57c2a36.png)

### VLSM Tree

![jarkom](https://user-images.githubusercontent.com/68369091/143685177-442408e6-eb64-4579-bdc2-9d414e1e7e09.jpg)

## GNS3 - CIDR

### Topologi

![image](https://user-images.githubusercontent.com/68369091/143685136-610c9211-c151-45f6-b668-8bb9755cc605.png)

### CIDR Tree

![tree](https://user-images.githubusercontent.com/62832487/143685708-6f075d3c-5020-4aa1-ae32-b286a1947546.jpg)

### Setting GNS3
**Router**
- **FOOSHA**
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 192.175.192.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 192.175.64.1
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 192.175.160.1
	netmask 255.255.255.252

auto eth4
iface eth4 inet static
	address 69.69.79.105
	netmask 255.255.255.252
```

- **WATER7**
```
auto eth0
iface eth0 inet static
	address 192.175.64.2
	netmask 255.255.255.252
	gateway 192.175.64.1

auto eth1
iface eth1 inet static
	address 192.175.32.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 192.175.16.1
	netmask 255.255.255.252
```

- **PUCCI**
```
auto eth0
iface eth0 inet static
	address 192.175.16.2
	netmask 255.255.255.252
	gateway 192.175.16.1

auto eth1
iface eth1 inet static
	address 192.175.0.1
	netmask 255.255.248.0

auto eth2
iface eth2 inet static
	address 192.175.8.1
	netmask 255.255.255.128
```

- **GUANHAO**
```
auto eth0
iface eth0 inet static
	address 192.175.160.2
	netmask 255.255.255.252
	gateway 192.175.160.1

auto eth1
iface eth1 inet static
	address 192.175.132.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 192.175.128.1
	netmask 255.255.254.0

auto eth3
iface eth3 inet static
	address 192.175.152.1
	netmask 255.255.255.252
```

- **ALABASTA**
```
auto eth0
iface eth0 inet static
	address 192.175.128.2
	netmask 255.255.254.0
	gateway 192.175.128.1

auto eth1
iface eth1 inet static
	address 192.175.130.1
	netmask 255.255.255.240
```

- **OIMO**
```
auto eth0
iface eth0 inet static
	address 192.175.152.2
	netmask 255.255.255.252
	gateway 192.175.152.1

auto eth1
iface eth1 inet static
	address 192.175.144.1
	netmask 255.255.255.0

auto eth2
iface eth2 inet static
	address 69.69.79.109
	netmask 255.255.255.252
```

- **SEASTONE**
```
auto eth0
iface eth0 inet static
	address 192.175.144.2
	netmask 255.255.255.0
	gateway 192.175.144.1

auto eth1
iface eth1 inet static
	address 192.175.148.1
	netmask 255.255.252.0
```

**Client**
- **BLUENO**
```
auto eth0
iface eth0 inet static
	address 192.175.192.2
	netmask 255.255.252.0
	gateway 192.175.192.1
```

- **CIPHER**
```
auto eth0
iface eth0 inet static
	address 192.175.32.2
	netmask 255.255.252.0
	gateway 192.175.32.1
```

- **CALMBELT**
```
auto eth0
iface eth0 inet static
	address 192.175.0.2
	netmask 255.255.248.0
	gateway 192.175.0.1
```

- **COURTYARD**
```
auto eth0
iface eth0 inet static
	address 192.175.0.3
	netmask 255.255.248.0
	gateway 192.175.0.1
```

- **JIPANGU**
```
auto eth0
iface eth0 inet static
	address 192.175.8.2
	netmask 255.255.255.128
	gateway 192.175.8.1
```

- **JABRA**
```
auto eth0
iface eth0 inet static
	address 192.175.132.2
	netmask 255.255.252.0
	gateway 192.175.132.1
```

- **MAINGATE**
```
auto eth0
iface eth0 inet static
	address 192.175.128.3
	netmask 255.255.254.0
	gateway 192.175.128.1
```

- **JORGE**
```
auto eth0
iface eth0 inet static
	address 192.175.130.2
	netmask 255.255.255.240
	gateway 192.175.130.1
```

- **ENIESLOBBY**
```
auto eth0
iface eth0 inet static
	address 192.175.144.3
	netmask 255.255.255.0
	gateway 192.175.144.1
```

- **ELENA**
```
auto eth0
iface eth0 inet static
	address 192.175.148.2
	netmask 255.255.252.0
	gateway 192.175.148.1
```

**Server**
- **DORIKI**
```
auto eth0
iface eth0 inet static
	address 69.69.79.106
	netmask 255.255.255.252
	gateway 69.69.79.105
```

- **FUKUROU**
```
auto eth0
iface eth0 inet static
	address 69.69.79.110
	netmask 255.255.255.252
	gateway 69.69.79.109
```

### Routing
- **FOOSHA**
```
route add -net 192.175.0.0 netmask 255.255.192.0 gw 192.175.64.2
route add -net 192.175.128.0 netmask 255.255.224.0 gw 192.175.160.2
route add -net 69.69.79.108 netmask 255.255.255.252 gw 192.175.160.2
```

- **WATER7**
```
route add -net 192.175.0.0 netmask 255.255.240.0 gw 192.175.16.2
```

- **GUANHAO**
```
route add -net 192.175.130.0 netmask 255.255.255.240 gw 192.175.128.2
route add -net 192.175.144.0 netmask 255.255.248.0 gw 192.175.152.2
route add -net 69.69.79.108 netmask 255.255.255.252 gw 192.175.152.2
```

- **OIMO**
```
route add -net 192.175.148.0 netmask 255.255.252.0 gw 192.175.144.2
```

Pada router FOOSHA, jalankan:
```
iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 192.175.0.0/16
```

Pada semua node (router dan client) selain FOOSHA, jalankan:
```
echo nameserver 192.168.122.1 > /etc/resolv.conf
```


## Penderitaan
- Susah mas materinya
- Routing bingungin
- VLSM dan CIDR bingungin
- tidak paham cisco nya
