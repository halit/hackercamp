# Temel Network

## Komutlar

- Interface yönetimi
```
ip link
ifconfig
ifconfig eth0 192.168.10.12 netmask 255.255.255.0
```

- IP talebi
```
dhclient eth0
dhcpd eth0
```

- Arp tablosu içeriğini görüntelemek
```
arp -a
```

- Statik arp kaydı girmek
```
arp -s 192.168.1.4 00-10-54-CA-E1-40
```

- ICMP echo pakedi gönderme
```
ping 8.8.8.8
ping google.com
ping 8.8.8.8 -c 1
```

- DNS sorguları
```
nano /etc/resolv.conf
dig a halit.ninja
dig aaaa 6.halit.ninja
dig txt question.halit.ninja
nslookup halit.ninja
nslookup halit.ninja 8.8.8.8
```

- Netcat aracı ile HTTP isteği gönderme
```
nc halitalptekin.com 80

GET / HTTP/1.1
Host: halitalptekin.com
```

- Curl aracı ile HTTP isteği gönderme
```
curl -v http://halitalptekin.com
```

- Traceroute aracı ile paket takibi
```
traceroute google.com
```

- Host aracı ile hostname öğrenme
```
host 8.8.8.8
```

## Ödevler

- **mitmf** aracını kullanarak man in the middle saldırısı gerçekleştiriniz.
- **wireshark** ile networkünüzde oluşan trafiği inceleyiniz.
- **fragroute** aracının kullanımını öğreniniz. Hangi amaçla kullanılabileceğini araştırınız.
- ICMP üzerinden trafik tünellemenin nasıl yapılacağını araştırınız.
- DNS üzerinden trafik tünellemenin nasıl yapılacağını araştırınız.
- DNS kaynaklı gerçekleştirilebilecek saldırıları araştırınız.
- DHCP kaynaklı gerçekleştirilebilecek saldırıları araştırınız.
- İstediğiniz bir programlama dilinde ARP veya DNS üzerinden man in the middle saldırısı yapabilecek araç geliştiriniz.
- İstediğiniz bir programlama dilinde traceroute aracının benzerini gerçekleştiriniz.

## Kaynaklar

- https://technet.microsoft.com/tr-tr/library/cc786900(v=ws.10).aspx
- http://microchip.wikidot.com/tcpip:detailed-tcpip-communication
- http://selimozdem.com/ositcpip-1-2-notlari.html/
- http://www.hotspotshield.com/learn/what-is-ip-address
- http://www.highteck.net/EN/Network/Addressing_the_Network-IPv4.html
- http://wiki.mikrotik.com/wiki/Manual:Connection_oriented_communication_(TCP/IP)
