# Kişisel Güvenlik

## Gereksinim

- Bir önceki başlıklarda bahsedildiği üzere internet çok da güvenli bir ortam değil. 
- Bu yüzden siber güvenlik uzmanlarının kendisini ve verilerini güvende tutması gerekmektedir. 
- %100 güvenlikten bahsedilemeyecek olmasına rağmen önlemlerini alması çok önemlidir. 
- Yakın zamanda yaşanan [Hackingteam][1] vakası bunu doğrular niteliktedir.

## İşletim Sistemi Güvenliği

- Kullanılan işletim sisteminin güvenlik içerisinde ciddi derecede önemi vardır. 
- Burada güvenlikten bahsedilen hem sistem içerisine sızabilme hem de verilerin başka kimseler tarafından paylaşılması olabilmektedir. 
- Örneğin Windows 10 işletim sisteminin gizliliğinizi tehdit edecek bir çok [özelliği][2] ortaya çıkmıştır. 
- Bu yüzden özgür ve açık kaynaklı işletim sistemlerine yönelmek doğru olacaktır. 
- Burada yapılan büyük bir hata da [Kali][3] veya [Blackarch][4] gibi güvenlik alanında çalışanlara özel geliştirilmiş GNU/Linux dağıtımlarını host sistem olarak kullanmaktır. Bu kişisel güvenliği riske atacak bir durumdur. 
- Host olarak [Arch Linux][5] veya [Gentoo][6] gibi işletim sistemlerini kullanmak daha doğru olacaktır. 
- Tabi host işletim sistemlerinin [full disk encryption][7] olarak kurulması büyük önem taşımaktadır. 
- Aynı şekilde işletim sistemi güvenliğinin sağlanmasından sonra BIOS güvenliği de ayrı bir önem taşımaktadır.

## Veri Güvenliği

- [Gizlilik][18] kısmında da bahsedildiği üzere günlük hayatta [Truecrypt][8] ve [PGP][9] ile veri güvenliği sağlanabilmektedir.

## Mobil Güvenlik

- Mobil cihazların kullanım oranında yer alan ciddi yükseliş, hackerlar açısından bu alanı cezbeder hale gelmiştir. 
- O yüzden siber güvenlik alanında uğraşan kişilerin mobil cihazlarının güvenliklerini de sağlamaları gerekmektedir. 
- Örneğin Android işletim sistemine sahip cihazlarda tüm cihazın şifrelenmesi özelliği aktif olarak tutulmalıdır. 
- Bunun yanında çeşitli uygulamaların da kullanılması tavsiye edilmektedir. 
- Örnek olarak [Redphone][10], [K9 Mail][11], [Swift Wifi][12], [AIMSICD][13] verilebilir.

## Sosyal Medya Güvenliği

- Facebook, twitter gibi sosyal medya kullanımlarına ayrıca dikkat edilmesi gerekmektedir. 
- Otomatize araçlar ile rahatlıkla bilgi toplanması ve sınıflandırma yapma şansı tanımaktadır. 
- Ayrıca büyük saldırılarda büyük veri kaçaklarına sebep olmaktadır. 
- Günümüzde çokça meşhur olan anlık mesajlaşma yazılımlarına da ayrıca dikkat edilmelidir. 
- Örneğin [whatsapp][16] gibi şifresiz iletişim yapan uygulamalar yerine [telegram][17] gibi çözümler tercih edilmelidir.

## Sunucu Güvenliği

- Kişisel sunucuların güvenliği de büyük önem arz etmektedir. 
- Buna göre örneğin VPN olarak kullandığınız veya kişisel blog sitelerinin tutulduğu sunuculara ayrıca önem verilmelidir.
- Böyle sunucuların saldırganlar tarafından ele geçirilmesi ileride gelecek olan büyük saldırılara hazırlık olarak kullanılabilir.

## Paylaşımlı Ağ Güvenliği

- Paylaşımlı ağlar kişisel güvenlik için en büyük tehditlerin başında gelmektedir. 
- Buna göre örneğin gidilen bir kafe'de bağlanılan ağ içerisinde bir saldırgan tarafından saldırıya uğrama olasılığı çok yüksektir. 
- Bu yüzden çok gerekmediği sürece bu tarz ağlara giriş yapılmaması gerekmektedir. 
- Eğer zorunlu ise ortadaki adam saldırıları için önlem alınması ve VPN kullanılarak internete çıkılması gerekmektedir. 
- Tabi tüm bunlar %100 derecede önlem sağlamamaktadır.

## Örnekler

- Windows işletim sistemine sahip, full disk encryption olmayan, admin parolası bilinmeyen bir sisteme live cd kullanarak erişim.
- En çok kullanılan 4 kablosuz ağın güvenliklerine göre analizi.

## Ödev

- BIOS ve GPU kaynaklı zararlı yazılımların araştırılması ve önlemlerin alınması.
- Full disk encryption ile birlikte [Blackarch][4] işletim sisteminin kurulması.
- Örnek olarak gösterilen saldırının başka formatlarda benzer şekilde uygulanması.
- [Zanti][14] uygulamasının kurulması ve incelenmesi.
- [Nethunter][15] uygulamasının kurulması ve incelenmesi.
- [Telegram][17] uygulamasının kurulması ve secret chat özelliğinin incelenmesi.
- Vlan hopping kavramının araştırılması.
- Sanallaştırma çözümlerinin getirdiği avantajları kavrama.
- DNS Crypt kullanılması, getirdiği önlemleri detaylıca inceleme.

[1]: https://wikileaks.org/hackingteam/emails/
[2]: https://bgr.com/2015/07/31/windows-10-upgrade-spying-how-to-opt-out/
[3]: https://www.kali.org/
[4]: http://blackarch.org/
[5]: https://www.archlinux.org/
[6]: https://www.gentoo.org/
[7]: https://en.wikipedia.org/wiki/Linux_Unified_Key_Setup
[8]: http://truecrypt.sourceforge.net/
[9]: https://en.wikipedia.org/wiki/Pretty_Good_Privacy
[10]: https://play.google.com/store/apps/details?id=org.thoughtcrime.redphone&hl=tr
[11]: https://play.google.com/store/apps/details?id=com.fsck.k9&hl=tr
[12]: https://play.google.com/store/apps/details?id=mobi.wifi.toolbox&hl=tr
[13]: https://secupwn.github.io/Android-IMSI-Catcher-Detector/
[14]: https://www.zimperium.com/zanti-mobile-penetration-testing
[15]: https://www.kali.org/kali-linux-nethunter/
[16]: https://www.whatsapp.com/?l=tr
[17]: https://telegram.org/
[18]: 04-gizlilik.md
