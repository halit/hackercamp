# Kriptoloji

## Tanımlar

- **Kriptoloji:** Şifre bilimidir. Kriptografi ve kriptoanaliz birleşiminden oluşur.
- **Steganografi:** Veriyi saklama veya gizleme bilimidir.
- **Encoding:** Verinin başka bir forma dönüştürülmesidir.

## Encoding

- Çoğu zaman veriyi farklı formlara dönüştürmek gerekmektedir. 
- Örneğin elimizdeki binary bir resmi, ascii karakterlerden oluşan bir diziye dönüştürme düşünülebilir. 
- Burada dikkat edilmesi gereken nokta, şifreleme yapılmadığıdır. 
- Sadece aynı veri farklı bir forma dönüştürülmektedir.
- Orjinal haline herkes geri dönüştürebilir.
- En ünlü encode yöntemlerinden birisi base64'tür. 

```
echo -n "deneme" | base64
echo -n "ZGVuZW1l" | base64 -d
cat resim.jpg | base64 > resim.encoded
```

## Hash

- Hash fonksiyonları genellikle tek gidişli fonksiyonlar olarak tanımlanmaktadır. 
- Giriş kısmından verilen veriyi her zaman aynı boyuttaki unique bir değere dönüştürmektedir. 
- Verilen veri 10K, 1M, 100M, 1GB de olsa çıkıştaki uzunluk hep aynı olmaktadır. 
- Fonksiyonların gücü, güvenilirliği genellikle çakışma oranı ile ölçülmektedir. 
- Eğer girişten verilen iki farklı veri aynı özet çıktısına giderse ilgili hash fonksiyonu zayıftır denilebilir. 
- En çok kullanılan hash algoritmalarına örnek md5, sha1, sha256, sha512, LM, NTLM verilebilir.

```
echo -n "123456" | md5sum
echo -n "123456" | sha1sum
echo -n "123456" | sha256sum
md5sum dosya.jpg
```

## Hash Kırma Saldırıları

- Yapılan büyük yanlışlardan birisi de şifrelerin hash halini almanın, bir şifreleme yöntemi olduğunu düşünmektir.
- Tek yönlü bir fonksiyon olduğu için geriye dönüş teorik olarak imkansızdır. (en azından imkansız olması beklenmektedir)
- Bu yüzden hash algoritmalarına kriptografik saldırılar yerine wordlist veya kaba kuvvet saldırıları yapılmaktadır.
- John The Ripper aracının hash formatlarına [buradan][0] bakabilirsiniz.
- Hash kırma saldırılarının vazgeçilmesi olan [hashcat][1] aracı GPU gücünden de faydalanabilmektedir.
- Saldırılar arasında en hızlı sonuç getiren şüphesiz rainbow table denilen yöntemdir. Bu sayede yerden kaybedilmesine rağmen hızdan kazanılmaktadır.
- Popüler algoritmalar için tablolara [buradan][2] ulaşabilirsiniz.

```
echo "halit:e10adc3949ba59abbe56e057f20f883e" > a.txt
john a.txt --format=Raw-MD5
echo "diger:b24ed7db06817c48245a939dd97e72573a81c881" > b.txt
john b.txt --wordlist /usr/share/wordlists/rockyou.txt --format=Raw-SHA1
echo "e10adc3949ba59abbe56e057f20f883e" > c.txt
hashcat -m 0 -a 0 c.txt  /usr/share/wordlists/rockyou.txt
```

## Simetrik Şifreleme

- Veriler bloklar halinde işleme alınır. 
- Haliyle blok boyutları sabittir ve isimlendirmelerde belirtilir.
- Verinin boyu yetersiz ise gereksiz veriler ilgili boyuta tamamlandır.
- Kullanılan şifreleme modu çok önemlidir. Doğru mod seçimi yapılmazsa saldırılara maruz kalınabilir.
- İlgili modların kullanımı ve sonuçlarına [buradan][3] ulaşabilirsiniz.
- En ünlüleri AES, DES, Blowfish, Serpent ve Twofish'tir. Ancak AES standart olarak kabul edilmektedir.

## Simetrik Şifre Saldırıları

- Kullanılan mod kaynaklı saldırı yöntemleri değişebilmektedir.
- Örneğin ECB modundaki bir şifreleme de, anahtara sahip olunamasa da istenilen sonuca erişilebilir.
- 2DES'de olduğu gibi kullanım kaynaklı da saldırılar yapılabilmektedir. [Meet in the Middle][4] saldırısı buna örnektir.

```
echo "deneme metin" > d.txt
gpg -c --cipher-algo AES256 d.txt
gpg -o original.txt -d d.txt.gpg
```

## Asimetrik Şifreleme

- Simetrik şifrelemede güvenlik algoritmanın gizliliğine değil, anahtarın korunmasına bağlıdır. Haliyle tek anahtar olmaktadır.
- Ancak birden fazla kişiyle aynı verinin güvenli paylaşımı için herkese anahtarın paylaştırılması gerekmektedir.
- Anahtar paylaşım problemini ortadan kaldırmak için asimetrik şifreleme önerilmiştir.
- Buna göre artık tek bir anahtar yerine, public ve private anahtar ikilileri oluşturulmaktadır.
- Karşı tarafa gönderilmek istenen veri, ilgili kişinin public anahtarı ile şifrelenerek gönderilir.
- Veriyi alan kişi de kendi private anahtarı ile eski haline dönüştürür.
- Burada public anahtarın paylaşılması güvenlik olarak herhangi bir risk teşkil etmemektedir.
- Sistemin güvenliği private anahtarın korunmasına bağlıdır.
- Asimetrik şifreleme sadece verileri şifrelemek için kullanılmamaktadır.
- Imzalama sistemlerinde de asimetrik şifrelemeden faydalanılmaktadır.
- En popüler algoritma RSA'dir. 

## OTP

- Doğru kullanımlarda en güvenli algoritma olarak nitelendirilmektedir.
- Ancak aynı anahtarın tekrar tekrar kullanılması ile crib-drag saldırı tekniği ile kolay bir şekilde kırılabilmektedir.

## Dizi Şifreleme

- Yüksek hız gerektiren yerlerde tercih edilirler.
- Örneğin A5 algoritması GSM protokolünde verinin şifrelenmesi için kullanılır.
- Aynı şekilde WEP protokolü de RC4 şifreleme algoritmasını kullanmaktadır.
- Uygulanmasından kaynaklı olarak saldırılara maruz kalmaktadır.
- RC4 algoritmasına karşı gerçekleştirilebilen çok kolay ve güçlü yöntemler bulunmaktadır.

## Örnekler

- Truecrypt ile AES bloğu oluşturma ve truecrack ile kırılması.
- Enigmail ile public-private anahtar oluşturma ve mail gönderilmesi.
- Browser üzerinde sertifika incelenmesi.

## Ödev

- **HMAC** tekniğine karşı yapılan **length extension** saldırısını araştırınız. **hashpump** aracının kullanımını inceleyiniz.
- **MD5** algoritmasına karşı yapılabilecek saldırıları analiz ediniz. İki adet aynı hash değerine sahip farklı çıktı üreten dosya oluşturunuz.
- Doğumgünü paradoxunu inceleyiniz. Hash algoritmaları için önemini kavrayınız.
- **WEP** algoritmasına yönelik saldırıların nasıl gerçekleştiğini öğrenininiz. Altında yatan kriptografik zayıflığı kavrayınız.
- Amazon tarzı bulut sistemlerde şifre kırma saldırılarının nasıl gerçekleştirildiğini araştırınız.
- **ophcrack** ve **rainbowcrack** araçlarının ne tarz bir saldırı yaptığını araştırınız.
- **ECB** moduna yönelik yapılan saldırıları inceleyiniz.
- **zip2john** ve **rar2john** kullanarak **zip** ve **rar** dosyalarını kırınız. Aynı yöntemi **pdf** için de gerçekleştiriniz.
- **crunch** aracı ile nasıl wordlist oluşturulduğunu araştırınız.
- **crib-drag** yönteminin ne olduğunu kavrayınız. Bu işi yapan örnek bir araç bulunuz.
- **SSL** ve **TLS** arasındaki farkları inceleyiniz.
- **A5** şifreleme yöntemine yönelik saldırıların neden **PlayStation** üzerinde başarılı olduğunu kavrayınız.
- **gpa** benzeri bir araç ile public-private anahtar yönetimi yapınız.
- **AES** ve **RSA** için güvenli en düşük bit miktarlarını araştırınız.
- Asal çarpanlarına ayırma algoritmalarının iyileşmesinin **RSA** algoritmasına zararını araştırınız.

[0]: http://pentestmonkey.net/cheat-sheet/john-the-ripper-hash-formats
[1]: https://hashcat.net/oclhashcat/
[2]: http://project-rainbowcrack.com/table.htm
[3]: https://en.wikipedia.org/wiki/Block_cipher_mode_of_operation
[4]: https://en.wikipedia.org/wiki/Meet-in-the-middle_attack
