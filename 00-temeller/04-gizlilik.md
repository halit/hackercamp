# Gizlilik

## Gizlilik İhtiyacı

- Siber güvenlik alanıyla uğraşan herkes gizlilik ihtiyacı duymaktadır. 
- Her ne kadar bir saldırgan olmasanız da bu gereklilik geçerlidir. 
- Örneğin bir saldırgan büyük bir firmadan çaldığı özel bilgileri kimsenin eline geçmemesi ve yakalandığı takdirde güvenlik birimlerinden saklama amaçlı olarak gizlilik ihtiyacı duymaktadır. Ancak beyaz şapkalı bir güvenlik uzmanı ise güvenlik testi sonucunda elde ettiği çok benzer önemli verileri saklama ihtiyacı duyacaktır. 
- Çünkü bu tarz verilerin bir şekilde başka kişilerin eline geçmesi hem çalıştığı firmaya itibar kaybı yaşatacak iken, hem de güvenlik testi yapılan firma ile işbirliklerinin bozulmasına yol açacaktır. 
- Bu yüzden siber güvenlik alanında çalışma yapan herkesin veri güvenliğine, gizliliğine ihtiyacı vardır.

## İnternette Gizlenme

- Hackerlar internette gizlenmek için çok farklı teknikler kullanmaktadır. 
- Bunların en ünlüsü şüphesiz ki VPN kullanımıdır. 
- Ancak tek başına VPN kullanımı her zaman yeterli olmamaktadır. 
- İşte bu yüzden saldırganlar, hedeflerine göre gizlilik derecelerini değiştirmektedir. 
- Bunun için aşağıdaki benzer kombinasyonlar kurulabilmektedir. 
- Burada HACKED kelimesi hackerlar tarafından daha önceden ele geçirilmiş sunucuları veya kişisel bilgisayarları belirtmektedir.

### Bazı Kombinasyonlar

- ATTACKER -> VPN -> TARGET
- ATTACKER -> VPN -> VPN -> TARGET
- ATTACKER -> VPN -> HACKED -> HACKED -> ... -> TARGET
- ATTACKER -> VPN -> HACKED -> HACKED -> ... -> VPN -> TARGET
- ATTACKER -> VPN -> DARKNET -> VPN -> TARGET
- ATTACKER -> VPN -> DARKNET -> TARGET
- ATTACKER -> DARKNET -> TARGET
- ATTACKER -> HACKED -> HACKED -> .. -> TARGET

## Siber Güvenlik Açısından

- Siber güvenlik uzmanları da bazı zamanlar içerisinde gizlilik ihtiyacı duymaktadır. 
- Örneğin X ülkesinde savunma sanayi firmasında çalışan bir siber güvenlik uzmanı, gün içerisinde çeşitli hacker forumlarını vs takip etmesi gerekmektedir. 
- Eğer doğrudan çalıştığı firmanın IP adresi ile bu tarz forumlara bağlanırsa, bu hem kimliklerini ortaya çıkaracaktır hem de hackerların ilgili firmaya yönelmesine sebep olacaktır. 
- Bu yüzden siber güvenlik uzmanları da kendi VPN'lerine sahip olmalıdır.

## Anonim Para

- Hackerlar gizlilik için VPN veya benzeri şekilde çeşitli sunuculara ihtiyaç duymaktadır. 
- Bu ihtiyaçlarını yasa dışı yollar ile elde edebilecekleri gibi anonim para kullanarak da gerçekleştirmektedirler.
- En ünlü anonim para birimi ise [Bitcoin][1]'dir. 
- Temelinde kriptografik sonuçların olduğu Bitcoin hackerların vazgeçilmezidir. 
- Her bir ticaret için ayrı oluşturulan cüzdanlar sayesinde sahiplik olayı ortadan kalkmaktadır. 
- Ayrıca ilk başta legal yollardan döndürülen paranın da anonimleştirilmesi için **Para Yıkama** denilen teknikler kullanılmaktadır.
- Yukarıda bahsedildiği gibi siber güvenlik uzmanlarının da internet üzerinden çeşitli ticaret yapmaları gerekebilmektedir.
- Örneğin alacakları VPN servislerinin ödemelerini kendi hesapları yerine bitcoin üzerinden yapmayı tercih etmektedir. 
- Aynı şekilde bitcoin cüzdanlarına aktarılacak paraları da gene yasal olan prepaid kartlar aracılığı ile kendi cebinden sağlayabilmektedir.

## Veri Güvenliği

- Hackerlar ele geçirdikleri verileri, siber güvenlik uzmanları da işleri sırasında elde ettikleri verileri saklama ihtiyacı duymaktadır. 
- Bunun için en çok kullanılan araç şüphesiz ki [Truecrypt][9] aracıdır. 
- Her ne kadar geliştirilmesinin durdurulması konusunda çeşitli şüpheler bulunsa da aktif olarak hem siber güvenlik uzmanları hem de hackerlar tarafında sıkça kullanılmaktadır.
- Veri güvenliği kısmında diğer bir önemli nokta da [PGP][6]'dir. 
- Ağırlıklı olarak mail iletişimi sırasında kullanılsa da verilerin saklanması konusunda da sıkça kullanılmaktadır. 
- Gmail veya benzer bir mail sağlayıcısını kullanan hem saldırgan hem de uzmanlar, mail göndermek istedikleri kişinin public keyi ile veriyi şifreleyip karşı tarafa göndermektedir. 
- Maili şifreli bir şekilde alan karşı karaf ise elinde bulunan private key ile orjinal maile ulaşmaktadır. 
- Bu noktada [PGP][6] sadece şifreleme yazılımı olarak düşünülmemelidir. 
- Şifreleme ve imzalama kullanım alanlarının başında gelmektedir.

## Ödev

- [Digitalocean][2], [linode][3] gibi sağlayıcılardan alınacak ucuz linux sunucular içerisine kişisel vpn kurulması ve bağlantı gerçekleştirilmesi
- Bitcoin cüzdanı oluşturulması ve saklanması
- [Tails][4], [whonix][5] gibi işletim sistemlerinin kullanılması ve amaçlarının kavranması
- Harici bir diski veya USB diski truecrypt containeri haline getirme, aynı container içerisinde hidden container oluşturma
- Kişisel public-private key ikililerinin oluşturulması, [PGP][6] kullanılması, [Enigmail][7] ile imzalı mail gönderilmesi
- [PGP][6] ile simetrik şifreli dosya oluşturulması, [PGP][6] ile asimetrik şifreli dosya oluşturulması
- Jabber clienti kurulması, [OTR][8] kullanılması
- Prepaid kart sahibi olma

[1]: https://bitcoin.org/tr/
[2]: https://www.digitalocean.com/
[3]: https://www.linode.com/
[4]: https://tails.boum.org/
[5]: https://www.whonix.org/
[6]: https://en.wikipedia.org/wiki/Pretty_Good_Privacy
[7]: https://www.enigmail.net/
[8]: http://wiki.xmpp.org/web/OTR
[9]: http://truecrypt.sourceforge.net/


