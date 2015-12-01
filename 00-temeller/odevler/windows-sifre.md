# Kali Linux ile Windows Kullanıcı Hesabı Crackleme

## Niçin Kali?

- Kali seçmemizin sebebi usb'den veya CD/DVD rom'dan live olarak yani kurulum yapmadan direkt çalıştırılabilir olmasıdır.
- Kali seçmemizin bir diğer nedeni ise kullanıcağımız bazı hazır paketlerin içerisinde kurulu olarak gelmesi.

## Adım Adım Kullanıcı Hesabı Crackleme
- Kali linux'u boot ettiğinizi ve kali linux masaüstüne eriştiğinizi varsayıyorum.
- Öncelikle disk yolunu öğrenmeniz gerekiyor disk yolunu öğrenebilmeniz için dosya yöneticisini açıp windowsun kurulu olduğu dizinde bir dosyanın üzerine sağ tıklayın ve özelliklere girin.
- "/root/493542/" benzeri yer alan ifadeyi alt taraftaki kodda **"DISKYOLU"** kısmına yerleştirerek terminalde bu komutu çalıştırın.

![1. adım](images/windows-sifre/1.png)

```
cd /media/**DISKYOLU**/Windows/System32/config
````



- Geldiğimiz klasörde windows'un kullanıcı hesabı bilgilerinin depolandığı .sam dosyaları vardır. Alt satırda verdiğim kodla bu dosyaları görebilirsiniz.

![2. adım](images/windows-sifre/2.png)
```
ls -l SAM* sam*
```

- Bu gördüğünüz sam dosyalarının içini görme vaktimiz geldi.
![3. adım](images/windows-sifre/3.png)
```
chntpw -l SAM
```

- Ekranda görmüş olduğunuz listede hesaplar ve hesapların bazı özellikleri yazmaktadır. Düzenlemek istediğiniz hesabı aşağıdaki koda yerleştirerek çalıştırınız. Ben Camp kullanıcısını seçtim.

![4. adım](images/windows-sifre/4.png)
```
chntpw -u **Administrator** SAM
```

- Gelen ekranda bize seçtiğimiz kullanıcı hesabıyla alakalı daha ayrıntılı bilgiler veriliyor.
- Bu ekranda 1,2,3,4,5 ve q komutlarını kullanarak bazı işlemleri gerçekleştirebiliyoruz.

1- Kullanıcının şifresini kaldır
2- Kilidi kaldır ve hesabı aktif et(burada hesabın aktif durumunu gösteriyor)
3- Hesabı yükselt yani hesaba admin yetkilerini ver
4- Bir gruba kullanıcı hesabı ekle
5- Bir gruptan kullanıcı sil
q- Çıkış

- Burdan dilediğiniz işlemleri uyguladıktan sonra q seçimini yaparak çıkabilirsiniz. "q" seçimini yaptıktan sonra değişiklikleri onaylıyorsanız "y" seçip kaydediniz.
- Ardından bilgisayarınızı yeniden başlatıp uyguladığınız değişikliklerin sonuçlarını alabilirsiniz.

