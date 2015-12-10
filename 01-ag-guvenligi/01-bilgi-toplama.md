# Bilgi Toplama

## Komutlar

```
nmap 10.0.3.7
nmap 10.0.3.7 -O
nmap -sV -p 80 10.0.3.7
nmap -sV -p 80 10.0.3.7 -v
nmap -sS 10.0.3.7 -p 1-100 
nmap -sP 10.0.3.7
nmap -A 10.0.3.7
nmap -p- -n -v -T4 10.0.3.7
nmap -p- -n -v -T4 10.0.3.7 -sV
nmap -sA 10.0.3.7 -p 80
nmap -p- -n -v -T4 10.0.3.7 -oG results.txt
nmap --spoof-mac 10:10:10:10:10:10
nmap -D 10.3.3.3,10.3.3.4,10.3.3.5 10.0.3.7
nmap -p 445 -n -v -T4 -sV --script smb-enum-shares 10.0.3.6
nc 10.0.3.6 9999
netdiscover  -r 10.0.3.0/24
```

## Ödevler

- **zmap** ve **masscan** araçlarının kullanımlarını öğreniniz.
- **Nmap** aracı ile birlikte nasıl güvenlik duvarlarının atlatıldığını araştırınız.
- **nc** ile nasıl port tarama yapılabileceğini araştırınız.
- **arpscan** aracının kullanımını araştırınız.
