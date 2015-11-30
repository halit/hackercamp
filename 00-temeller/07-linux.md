# Linux

## Kabuk

- Kullanıcının işletim sistemiyle iletişimini sağlayan yorumlayıcıdır.
- Verilen komutları işletim sistemine, komutların çıktılarını da kullanıcıya iletir.
- Birçok uygulaması vardır. Bash, sh, zsh en çok bilinenleridir.

## Komutlar

- **pwd**: bulunulan dizini ekrana basar.
```
pwd
``` 

- **man**: komut hakkında detaylı bilgi almak için kullanılır.
```
man pwd
man grep
```

- **mkdir**: yeni bir dizin oluşturmak için kullanılır.
```
mkdir deneme_dizin
mkdir -p deneme_dizin_diger/alt_dizin
mkdir -p deneme_dizin_deger/{0..9} 
```

- **touch**: yeni bir dosya oluşturur.
```
touch deneme_dosya_diger
touch deneme_dizin_x/{A..Z}
```

- **rm**: dosya veya klasör siler.
```
rm deneme_dosya
rm -r deneme_dizin/
rm -rf deneme_dizin/
```

- **cp**: dosya veya klasör kopyalama için kullanılır.
```
cp deneme_dosya deneme_dosya3
cp deneme_dizin deneme_dizin2 -r
```

- **mv**: dosya veya klasörleri taşımak için kullanılır.
```
mv deneme_dosya deneme_dosya3
```

- **find**: gelişmiş arama aracıdır.
```
find . -name "*.txt"
```

- **cd**: dizin değiştirmek için kullanılır.
```
cd ..
cd
cd deneme/
```

- **ls**: dosya ve dizinleri listeleyip, özelliklerini görüntüler.
```
ls -a
ls -l
ls -r
```

- **cat**: dosya içeriğini görüntüler.
```
cat deneme_dosya
```

- **echo**: ifadeleri ekrana basar.
```
echo "deneme"
echo $HOME
```

- **more**, **less**: içeriği fazla olan, ekrana sığmayan dosyaları görüntüler.
```
more deneme_dosya
less deneme_dosya
```

- **head**: bir dosyanın baştan itibaren istenilen sayıda satırını ekrana basar.
```
head deneme_dosya
head -1 deneme_dosya
```

- **tail**: head gibi çalışır ancak sondan itibaren ekrana basar.
```
tail deneme_dosya
tail -1 deneme_dosya
tail -f deneme_dosya
```

- **grep**: metin dosyaları içerisinde belirli değerleri aramak için kullanılır.
```
grep "kelime" deneme_dosya
grep "kelime" . -R
grep "Kelime" deneme_dosya -i
```

- **uname**: sistem bilgilerini görüntüler.
```
uname
uname -a
```

- **chown**: dosya veya klasörlerin sahibi ve grubunu değiştirir.
```
chown halit:users deneme_dosya
chown -R halit:users deneme_dizin/
```

- **service**: servislerin yönetilmesi için kullanılır.
```
service apache2 start
service apache2 status
```

- **mount**: diskleri sisteme bağlar.
```
mount
mount /dev/sdb1 mnt
```

## Çıktı Yönlendirme

- Komutların çıktıları dosyalara yönlendirilebileceği gibi, dosya içerikleri de komutlara yönlendirilebilir.
- Doğrudan bir çıktı **>** işareti ile yönlendirilir. Yönlendirildiği yerdeki diğer içeriği siler.
- Aynı işlem **>>** işareti ile yapılsaydı, içeriğin sonuna ekleme yapılacaktı.
- Komutlara girdi vermek için **<** işareti kullanılır.
- Bir komutun çıktısını diğer komuta vermek için **|** kullanılır.

```
echo "deneme2" > deneme_dosya
echo "deneme3" >> deneme_dosya
cut -d ":" -f1 < /etc/passwd
cat /etc/passwd | cut -d ":" -f1
cat /etc/passwd | cut -d ":" -f1 | grep root
```

## Dosya Sistemi

- **/bin**: Kullanıcı ve sistem yöneticisine ait çalıştırılabilir dosyaları barındırır.
- **/dev**: Donanımlara erişebilmek için gerekli dosyaları barındırır.
- **/etc**: Sistem konfigürasyonları için gerekli dosyaları barındırır.
- **/lib**: Sistem kütüphanelerini barındırır.
- **/sbin**: Sistem yöneticisine ait çalıştırılabilir dosyaları barındırır.
- **/home**: Kullanıcılara ait dizindir.
- **/mnt**: Sisteme dışarıdan bağlanacak olan donanım aygıtlarının, bağlantı
noktalarını belirten dizindir.
- **/root**: Bir sistemde en yetkili kullanıcı olan "root" kullanıcısına ait dizindir.
- **/tmp**: Geçici dosyaların yer aldığı dizindir.
- **/usr**: Paylaşılan dosyaların barındığı dizindir. Burada çalışabilen dosyalar
bulunmakla beraber, döküman ve programlara ait dosyalar da yer almaktadır.
- **/var**: Sistem ve programlara ait log mesajları, email gibi mesajların bulunduğu
dizindir.
- **/proc**: Sistem hakkında gerekli bilgilerin bulunduğu sanal dizindir.
- **/boot**: Linux Kernelini barındıran, sistem haritalarını ve ikinci seviye boot
yükeleyicilerini barındıran dizin.
- **/opt**: Add-on yazılımların bulunduğu alandır.

## Dosya İzinleri

- Her dosya ve klasörün hem sahibi hem de grubu vardır.
- Bu izinler read(4), write(2), execute(1) olmaktadır.
- İzinler verilirken sahip, gurup ve herkes olarak belirlenir.

```
chmod 777 deneme_dosya
chmod +x deneme_uygulama
chmod g+wx deneme_uygulama
```

## Network Ayarları

- **ifconfig**: mevcut ağ arayüzlerinin yönetimi için kullanılır.
- **dhclient**: DHCP'den ip talebinde bulunur.

```
ifconfig
ifconfig eth0
ifconfig eth0 192.168.2.2 netmask 255.255.255.0
dhclient eth0
```

## Kullanıcı Yönetimi

- **/etc/passwd**: Kullanıcı bilgileri tutulur.
- **/etc/shadow**: Kullanıcıların şifre özetleri tutulur.

```
useradd osman
cat /etc/passwd
userdel osman
```

## Süreç Yönetimi

- Çalışmakta olan her program süreç olarak adlandırılır.
- Her sürecin kendine has bir PID numarası vardır.

```
ps
ps -aux
top
jobs -l
fg
bg
./uygulama &
kill -9 1139
```

## Paket Yönetimi

```
apt-get install paket
apt-cache search paket
apt-get update
apt-get upgrade
apt-get remove paket
```

## Kaynak Koddan Kurulum

```
./configure
make
make install
```

## Sistem Bilgisi

```
lsblk
df -h
cat /proc/cpuinfo
cat /proc/meminfo
netstat
netstat -antl
```

## Ödev

- Bash script nedir ve nasıl nasıl yazılır?
- Basit düzeyde bash script örnekleri yazıp, inceleyiniz. (dosya okuma, for, while, if)
- Touch ile oluşturulma tarihi farklı dosya oluşturunuz.
- SUID bit kavramını araştınız.
- SUID biti set edilmiş dosyaları bulan komutu yazınız.
- Tüm sistem içerisindeki en büyük 10 dosyayı bulan komutu yazınız.
- /proc/ dizini altında yer alan dosyaların ve klasörleri inceleyiniz.
- Firefox ile izlenen bir youtube videosunu /proc/ dizini altından çıkarınız.
- fdisk ve cfdisk araçlarının kullanımlarını öğreniniz. USB diskler üzerinde deneme yapınız.
- gparted aracını kurup, inceleyiniz.
- zsh kabuğunu kurunuz ve oh-my-zsh eklentisi ile birlikte kullanınız.
- top ve htop araçlarını kullanınız.
- Yazılan bir scripti başlangıçta çalışacak şekilde ayarlayınız.
- Yazılan bir scripti 10 dakikada bir çalışacak şekilde ayarlayınız.
- Çalıştırılan bir uygulama içerisinde ortaya çıkan hata mesajlarını /dev/null dosyasına yönlendiriniz.
- ./program1 & ile ./program1 && ./program2 komutu arasındaki farkı kavrayınız.
- dpkg ile apt-get uygulamaları arasındaki farkı araştırınız.
- Ubuntu için paket yöneticisi apt-get ise, archlinux, redhat, fedora, centos ve gentoo için ne olduğu araştırınız.
- Bootloader nedir? Kullandığınız işletim sisteminin bootloaderi nedir?
- tr, wc, sort, uniq, awk ve sed araçlarının kullanımını öğreniniz.
- wget ve curl kullanımını araştırınız.
- Bir dosyanın yanlışlıkla silinmesini önlemek için ne yapılabilir?
