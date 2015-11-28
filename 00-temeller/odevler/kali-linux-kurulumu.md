# Kali Linux Kurulumu

## NAT Network Kurulumu

- İlk olarak **File** menüsü altından **Preferences** kısmı açılır.

![1](images/Selection_1.png)

- Açılan menüden **Network** alt menüsüne geçilir. Buradan sağ tarafta yer alan **Adds new NAT network** butonuna tıklanır.

![2](images/Selection_2.png)

- Burada **NatNetwork** seçmesine çift tıklanıp **OK** butonuna tıklanır.

![3](images/Selection_3.png)

- Network ismi belirlenip devam edilir.

![4](images/NAT Network Details_008.png)

- Resimdeki gibi seçilerek devam edilir.

![5](images/VirtualBox - Preferences_009.png)

## Sanal Makinenin Oluşturulması

- Sanal makineyi açıp, sol üstteki  **New** butonuna tıklıyoruz. 

![6](images/Selection_010.png))

- Sanal makinenin ismini belirleyip  **Type** ve **Version** kısımları aşağıdaki gibi seçiyoruz.

![7](images/Create Virtual Machine_011.png)

- **Memory Size** 1024 MB olarak belirliyoruz ve **next** diyoruz.

![8](images/Create Virtual Machine_012.png)

- **Create a virtual hard disk now** seçeneğini seçip devam ediyoruz.
 
![9](images/Create Virtual Machine_013.png)

- **VDI** seçeneğini seçip devam ediyoruz.

![10](images/Create Virtual Hard Disk_014.png)

- **Dynamically allocated** seçeneğini seçip devam ediyoruz.

![11](images/Create Virtual Hard Disk_015.png)

- File boyutunu 20 GB yapıp **Create** diyoruz.

![12](images/Create Virtual Hard Disk_016.png)

- **pentest** isimli sanal makinemiz  aşağıdaki gibi oluşmuş oluyor.

![13](images/Selection_017.png)

- Burada **Setting** butonuna tıklıyoruz.

![14](images/Selection_018.png)

- Sağ kısımdan **Network** butonuna tıklayıp resimdeki seçenekleri seçiyoruz.

![15](images/pentest - Settings_019.png)

- Daha sonra sol kısımdan **Storage** butonuna tıklayıp, **Empty** seçmesine geçiyoruz.

![16](images/pentest - Settings_020.png)

- Burada aşağıdaki gibi **Choose Virtual Optical Disk File** diyoruz.

![17](images/Selection_022.png)

- Ve iso dosyasını seçiyoruz.

![18](images/Selection_023.png)

- **OK** deyip devam ediyoruz.

![19](images/pentest - Settings_024.png)

## Kali Linux Kurulumu

- Sanal makineyi açıp pentest makinesini seçip **Start** butonuna tıklıyoruz.

![19](images/Selection_025.png)

- Aşağıdaki gibi **Install** seçmesini seçip devam ediyoruz.

![20](images/Selection_026.png)

- Buradan dil olarak **English** seçiyoruz. Siz Türkçe de seçebilirsiniz.

![21](images/Selection_027.png)

- Ülke seçiminde önce **Other** seçmesini seçip,

![22](images/Selection_028.png)

- **Asia** deyip,

![23](images/Selection_029.png)

- **Turkey** seçiyoruz.

![24](images/Selection_030.png)

- Daha sonra aşağıdaki gibi seçip devam ediyoruz.

![25](images/Selection_031.png)

- Aşağıdaki gibi Türkçe klavye seçip devam ediyoruz.

![26](images/Selection_032.png)

- Burada kurulumu bekliyoruz.

![27](images/Selection_033.png)

- Burada **Hostname** belirleyip devam ediyoruz.

![28](images/Selection_034.png)

- **Domain** kısmına boşluk koyup devam ediyoruz.

![29](images/Selection_035.png)

- Parolamızı giriyoruz.

![30](images/Selection_036.png)

- Bekliyoruz.

![31](images/Selection_037.png)

- Aşağıdaki gibi seçip devam ediyoruz.

![32](images/Selection_038.png)

- Aşağıdaki gibi seçip devam ediyoruz.

![33](images/Selection_039.png)

- Aşağıdaki gibi seçip devam ediyoruz.

![34](images/Selection_040.png)

- Aşağıdaki gibi seçip devam ediyoruz.

![35](images/Selection_041.png)

- **Yes** deyip devam ediyoruz.

![36](images/Selection_042.png)

- Verilerin diske kopyalanmasını bekliyoruz.

![37](images/Selection_043.png)

- Burada **Yes** diyip devam ediyoruz.

![38](images/Selection_044.png)

- Direk **continue** diyip devam ediyoruz.

![39](images/Selection_045.png)

![40](images/Selection_046.png)

- **Yes** diyip devam ediyoruz.

![41](images/Selection_047.png)

- Aşağıdaki gibi seçip devam ediyoruz.

![42](images/Selection_048.png)

- Bekliyoruz.

![43](images/Selection_049.png)

- **Continue** deyip devam ediyoruz.

![44](images/Selection_050.png)

- Burada sağ alttaki kısımda hiçbirşeyin seçili olmadığından emin oluyoruz.

![45](images/Selection_053.png)

- **Username** giriyoruz.

![46](images/Selection_054.png)

- **Password** giriyoruz. Kali'yi açmış bulunmaktayız.

![47](images/Selection_055.png)

## Guest Eklentilerinin Kurulumu

- Terminal'i açıyoruz.

![48](images/Selection_058.png)

```
cp /media/cdrom0 vbox -r
cd vbox/
./VBoxLinuxAdditions.run
```
- Komutlarını aşağıdaki gibi sırayla çalıştırıyoruz.

![49](images/Selection_059.png)

![50](images/Selection_060.png)

- **Machine -> Reset Host** deyip sistemi baştan başlatıyoruz ve kurulumu tamamlamış oluyoruz.

![51](images/Workspace 1_061.png)

## Sistemin Güncellenmesi

- Aşağıdaki komutu çalıştırarak sistemi güncelleyebilirsiniz.

```sudo apt-get update && apt-get upgrade && apt-get disk-upgrade && apt-get -f install && apt-get autoremove```

![52](images/Selection_062.png)

