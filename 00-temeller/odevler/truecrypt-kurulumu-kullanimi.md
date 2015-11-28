# Truecrypt kurulumu ve kullanımı

## Truecrypt Hakkında

- Sabit disklerin ve özellikle Usb belleklerin şifrelenmesi için tercih edilen bir yazılımdır.
- Bu yazılım kim tarafından geliştirildiği bilinmemektedir. Ancak istihbarat servislerinin bu kişi üzerine arama yapıldığı bilinmekteydi. Bu bilgi eşliğinde site içerisinde son zamanlarda yayınlanan bir yazıda "Bu yazılımın güvenli değil" duyurusu yapıldı. 

## Truecrypt Kurulum Platformu

- En son sürümü yayınlanan [Truecrypt 7.2][1], windows platformunda kurulum yapan arkadaşlar için şifreleme yapmamakta, sadece şifreli alanlara ulaşmanızda yardımcı olmaktadır.
- Bunun için windows platformunda kurulum yapmak için [Truecrypt 7.1][2] dağıtımlarından birisini kurmalısınız. Kendi sitesinde eski dağıtımlara ulaşmak mümkün olmadığı gibi bu dağıtımları [github][2] üzerinden ulaşmanız mümkündür.
- Windows ortamında kurulum sıradan next adımları ile rahatlıkla kurulmaktadır.

## Linux platformunda Truecrypt Kurulumu

> sudo add-apt-repository ppa:stefansundin/truecrypt

> sudo apt-get update

> sudo apt-get install truecrypt

- Yukarıdaki linux kodlarını sırasıyla terminal üzerinde çalıştırıyoruz. 

> /etc/apt/sources.list.d/*********.list.save

- Yukarıdaki gibi bir hata ile karşılaşırsanız aşağıdaki kod satırını çalıştırarak çözüm bulmanız mümkün. Ancak bu kodların ne işe yaradığını araştırarak yapmanızı tavsiye ederim.

>sudo rm -rm /etc/apt/sources.list.d

- İşlem bittikten sonra terminal üzerinden truecrypt yazarak programı çalıştırmanız mümkündür. 

# Truecrypu Usb şifreleme


[1]: http://www.onaymetinkivilcim.com/Dersler/Truecrypt-Kullanimi/65
[2]: https://github.com/DrWhax/truecrypt-archive