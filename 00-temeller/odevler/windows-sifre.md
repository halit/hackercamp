# Kali Linux ile Windows Kullanýcý Hesabý Crackleme

## Niçin Kali?

- Kali seçmemizin sebebi usb'den veya CD/DVD rom'dan live olarak yani kurulum yapmadan direkt çalýþtýrýlabilir olmasýdýr.
- Kali seçmemizin bir diðer nedeni ise kullanýcaðýmýz bazý hazýr paketlerin içerisinde kurulu olarak gelmesi.

## Adým Adým Kullanýcý Hesabý Crackleme
- Kali linux'u boot ettiðinizi ve kali linux masaüstüne eriþtiðinizi varsayýyorum.
- Öncelikle disk yolunu öðrenmeniz gerekiyor disk yolunu öðrenebilmeniz için dosya yöneticisini açýp windowsun kurulu olduðu dizinde bir dosyanýn üzerine sað týklayýn ve özelliklere girin.
- "/root/493542/" benzeri yer alan ifadeyi alt taraftaki kodda **"DISKYOLU"** kýsmýna yerleþtirerek terminalde bu komutu çalýþtýrýn.

![1. adým](images/windows-sifre/1.png)

```
cd /media/**DISKYOLU**/Windows/System32/config
````



- Geldiðimiz klasörde windows'un kullanýcý hesabý bilgilerinin depolandýðý .sam dosyalarý vardýr. Alt satýrda verdiðim kodla bu dosyalarý görebilirsiniz.

![2. adým](images/windows-sifre/2.png)
```
ls -l SAM* sam*
```

- Bu gördüðünüz sam dosyalarýnýn içini görme vaktimiz geldi.
![3. adým](images/windows-sifre/3.png)
```
chntpw -l SAM
```

- Ekranda görmüþ olduðunuz listede hesaplar ve hesaplarýn bazý özellikleri yazmaktadýr. Düzenlemek istediðiniz hesabý aþaðýdaki koda yerleþtirerek çalýþtýrýnýz. Ben Camp kullanýcýsýný seçtim.

![4. adým](images/windows-sifre/4.png)
```
chntpw -u **Administrator** SAM
```

- Gelen ekranda bize seçtiðimiz kullanýcý hesabýyla alakalý daha ayrýntýlý bilgiler veriliyor.
- Bu ekranda 1,2,3,4,5 ve q komutlarýný kullanarak bazý iþlemleri gerçekleþtirebiliyoruz.

1- Kullanýcýnýn þifresini kaldýr
2- Kilidi kaldýr ve hesabý aktif et(burada hesabýn aktif durumunu gösteriyor)
3- Hesabý yükselt yani hesaba admin yetkilerini ver
4- Bir gruba kullanýcý hesabý ekle
5- Bir gruptan kullanýcý sil
q- Çýkýþ

- Burdan dilediðiniz iþlemleri uyguladýktan sonra q seçimini yaparak çýkabilirsiniz. "q" seçimini yaptýktan sonra deðiþiklikleri onaylýyorsanýz "y" seçip kaydediniz.
- Ardýndan bilgisayarýnýzý yeniden baþlatýp uyguladýðýnýz deðiþikliklerin sonuçlarýný alabilirsiniz.

