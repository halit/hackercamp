# Forensic

## Dosya Türü

- Her binary dosyanın başında türünü belirten magic number bulunmaktadır.
- Bu özel sayı her zaman gerçek formatını belirtmemektedir.
- Çeşitli uygulamaları aldatmak için kullanılabilir.

```
file a.jpg
file a.zip
file a.txt
hexeditor a.jpg
hexdump -C a.jpg | head
```

## Sıkıştırma Araçları

- Verinin sıkıştırılması ile tamamen farklı bir forma dönüş yapılmaktadır.
- Bu yüzden sıkıştırma yöntemlerinin ve araçlarının da iyi bilinmesi gerekmektedir.

```
zip a.zip a.txt
tar cvf a.tar a.txt
tar czvf a.tar.gz a.txt
gzip a.txt
gzip -d a.txt.gz
```

## Bilgi Toplama

- Elimizdeki binary dosyanın türünü belirledikten sonra üzerinde bilgi toplama aşaması başlar.
- Bu noktada dosya türüne göre farklı araçlar kullanılmaktadır.

```
readelf -h 
strings uygulama
exiftool resim.jpg
binwalk uygulama_diger
dd if=uygulama_diger of=ilginc.jpg skip=8 count=20
volatility -f win7.dmp imageinfo
volatility --profile=Win7SP0x86 -f win7.dmp pstree
```

## Network

- Network forensic aşamasında en iyi yardımcı şüphesiz ki Wireshark aracıdır.
- Desteklediği protokol sayısından, kullanım kolaylığına kadar pek de rakibi yoktur.

## Örnekler

- [evidence01.pcap][0] dosyasından, Ann'in konuştuğu kişinin adını ve gönderdiği dosyanın adını bulma.

## Örnek Kod

```
#include<stdio.h>

const char* secret = "cok gizli";
const int super_secret[] = {0x73,0x75,0x70,0x65,0x72,0x20,0x67,0x69,0x7a,0x6c,0x69};

int main(){
    printf("Hello World\n");
}
```

```
",".join(map(lambda x: hex(ord(x)), "super gizli"))
```

## Ödevler

- UPX kullanarak çalıştırılabilir bir dosyayı sıkıştırınız.
- Forensic yarışmasındaki geri [kalan][2] soruları çözmeye çalışınız.
- **volatility** aracını kullanarak diğer bellek [örneklerini][1] analiz ediniz.
- **foremost** kullanarak silinmiş dosyaların nasıl geri döndürüldüğünü inceleyiniz.
- Metadata silen araçları araştırınız.
- Büyük pcap dosyalarını Wireshark ile nasıl açabileceğinizi araştırınız.
- Windows işletim sistemi içerisinde bellek dumpı alınız ve bu dumpı analiz ediniz.
- MFT'nin ne olduğunu araştırınız.
- Honeynet'in hazırladığı [soruları][3] çözmeye çalışınız.

[0]: http://forensicscontest.com/contest01/evidence01.pcap
[1]: https://code.google.com/p/volatility/wiki/FAQ#Are_there_any_public_memory_samples_available_that_I_can_use_for
[2]: http://forensicscontest.com/puzzles
[3]: https://honeynet.org/challenges
