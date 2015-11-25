# Lab

## Sanallaştırma

Herhangi bir sanallaştırma çözümü kullanılabilir. Ancak eğitim içerisinde [virtualbox][1] yazılımı kullanılacaktır.

## Network

Sanal makineler için **PentestNetwork** ve **MalwrNetwork** isimli iki adet nat networku oluşturulacaktır. İlgili networkler içerisinde 10.0.3.0/24 ve 10.0.4.0/24 ip blokları kullanılabilir.

## Sanal Makineler

- pentest: Debian 64 bit, 20gb disk, 1gb ram, [Kali Linux][2] dağıtımı, PentestNetwork ağı.
- pentestlab-network: Debian 64 bit, 8gb disk, 512mb ram, [Metasploitable][3] dağıtımı, PentestNetwork ağı.
- pentestlab-web: Debian 64 bit, 8gb disk, 512mb ram, [Web for pentester][4] dağıtımı, PentestNetwork ağı.
- pentestlab-win: Windows xp 32 bit, 20gb disk, 256mb ram, [Windows XP SP3][5] işletim sistemi, PentestNetwork ağı.
- malwarelab-32: Windows xp 32 bit, 20gb disk, 256mb ram, [Windows XP SP3][5] işletim sistemi, MalwrNetwork ağı.
- malwarelab-64: Windows 7 64 bit, 20gb disk, 512mb ram, [Windows 7 Professional SP1][6] işletim sistemi. MalwrNetwork ağı.

[1]: https://www.virtualbox.org/wiki/Downloads
[2]: https://www.kali.org
[3]: http://sourceforge.net/projects/metasploitable/files/Metasploitable2/
[4]: https://pentesterlab.com/exercises/web_for_pentester
[5]: https://e5.onthehub.com/WebStore/Welcome.aspx?ws=d0ada7dc-6b9b-e011-969d-0030487d8897&vsro=8
[6]: https://e5.onthehub.com/WebStore/Welcome.aspx?ws=d0ada7dc-6b9b-e011-969d-0030487d8897&vsro=8
