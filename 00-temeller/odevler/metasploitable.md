# Metasploitable Kurulumu

## Sanal Makinenin Oluşturulması

- İlk olarak yeni bir sanal makine oluşturmak için **Yeni** butonuna tıklıyoruz.

![0](images/Metasploitable/0.jpg)

- Sanal makinenin ismini belirleyip **Türü** ve **Sürüm** kısımlarını aşağıdaki gibi seçiyoruz.

![1](images/Metasploitable/1.jpg)

- **Bellek Boyutu** 512 MB olarak belirliyoruz ve **İleri** diyoruz.

![2](images/Metasploitable/2.jpg)

- **Mevcut sanal sabit disk dosyasi kullan** (Use an existing virtual hard disk file) seceneğini seçiyoruz.

![3](images/Metasploitable/3.jpg)

- Sağ alttaki dizin butonuna tıklayarak aşağıdaki gibi **Metasploitable.vmdk** aç diyoruz.

![4](images/Metasploitable/4.jpg)

- Bu aşamadan sonra **Oluştur** diyoruz.

![5](images/Metasploitable/5.jpg)

- Sanal makinemizi çalıştırdıktan sonra asağıdaki gibi bir ekran karşımıza geliyor.

![6](images/Metasploitable/7.jpg)

## Nat Network Kurulumu

- Nat network kurulumu [burada][1] anlatılmıştır.

- Daha önce Nat network ağını kurduysaniz **pentestlab-network** sanal makinanizin ayarlar->Ağ bölümünden Nat ağını seçebilirsiniz.

![7](images/Metasploitable/8.jpg)

## Snapshot Alınması

- Sanal makineniz seçili iken sağ üst köşedeki **Anlik Görüntüler** (Snapshot) seçmesine tıklayıp aşağıdaki gibi anlık görüntüsünü alabilirsiniz.

![8](images/Metasploitable/9.jpg)

[1]: kali-linux-kurulumu.md
