# SUID Biti

- Bir kullanıcının, bir programı kendisine tanınmış haklardan daha fazla izne sahip olarak çalıştırması gerektiği durumlarda kullanılmaktadır
- Yani herhangi bir program herhangi bir kullanici tarafından program sahibinin haklarıyla çalıştırılabilir.
- Örnek olarak kullanıcıların şifrelerinin tutulduğu /etc/shadow dosyasına sadece root kullanıcısı olarak erişebiliriz.
- Aşağıda deneme1 adlı kullanıcı oluşturulup **su** komutu ile kullanıcıya geçiş yapılmıştır.

![1](images/suid/1.png) 

- **passwd** komutu ile bir kullanıcıya parola atamak için kullanılır. 
- Yani bu komutu kullanarak şifresini değiştiren bir kullanıcı shadow dosyası üzerinde değişiklik yapmış olur.

![2](images/suid/2.png) 

- Yetkimizin olmadığı bir dosyada değişiklik yapabilmemizin nedeni /usr/bin/passwd dosyasında **suid** bitinin etkinleştirilmiş olmasından kaynaklanıyor.
- Aşağıda yer alan izin diziliminde geçen 's' biti suid bitinin aktifliğini göstermektedir.

![3](images/suid/3.png) 

- SUID biti  durumu dikkat edilmesi gereken bir konudur.
- Çünkü kötü amaçlı bir kimse bu biti aktif edilmiş bir programda kendini root yapmaya çalışabilir.
- Sistemdeki suid biti aktif edilmiş dosyalara aşağıdaki komut ile ulaşılanabilir. 

```
sudo find / -perm -u+s -type f -exec ls -l {} \ ;
```

![4](images/suid/4.png) 

- Sistem de çalışan süreçleri ve bu süreçlerin id lerini görüntülemek için ps komutundan yararlanılabilir.
- Aşağıdaki script ile parametre olarak verilen processin çalışıp çalışmadığının kontrolü yapılıp ilgili bilgileri ekrana yazdırılıyor.

![5](images/crontab/6.png) 

![6](images/crontab/7.png) 

# Crontab

- Crontab belirlenen bir zaman diliminde istenilen scriptlerin ya da programların çalışmasını sağlar.Yani bir görev planlayıcısıdır.
- Mesala belli zaman aralıklarında dosyalarımızın yedeklerini almak için kullanabiliriz.
- Aşağıdaki resimde /etc dizini altındaki crontab dosyasının içeriği gösterilmektedir.

![7](images/crontab/8.png) 

- Aşağıdaki komut ile **crontab** dosyasını editleyebiliriz. **nano** kullanarak yapabilirsiniz.

![8](images/crontab/9.png) 

- Sonra planlamak istediğiniz görevi aşağıdaki gibi ekleyebilirsiniz.
- Burada sondan itibaren ilk * karakteri : Haftanın Günleri (0-6 Pazar:0)
- İkinci : Ay(1-12)
- Ucuncu : Ayın Günleri(1-31)
- Dorduncu : Saat(0-23)
- Besinci : Dakika(0-59)
- Aşağıda script2 dosyasının her 2 dakikada bir çalıştırmaya ayarlanması gösterilmektedir.

![9](images/crontab/10.png) 

- **du**  komutu bulunduğu dizinin alt klasörlerde dahil toplam boyutunu verir.
- **sort** komutu ise sıralama yapar.
- **wc** komutu parametre olarak verilen dosyadaki satır, kelime ve karakter sayısını gösterir.
- Bu komutların birlikte kullanımı aşağıdaki resimden görülebilir.

![10](images/crontab/11.png) 





