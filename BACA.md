[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/cakraawijaya/Whatsapp-Bot-based-Weather-monitoring-using-SPI-communication?logo=Codeforces&logoColor=white&color=%23F7DF1E)
![Type](https://img.shields.io/badge/Type-Personal%20Experiment-light.svg?style=flat&logo=gitbook&logoColor=white&color=%23F7DF1E)

# Whatsapp-Bot-based-Weather-monitoring-using-SPI-communication
Segera Hadir...

<br><br>

## Kebutuhan Proyek
| Bagian | Deskripsi |
| --- | --- |
| Papan Pengembangan | • STM32F103C8T6<br>• Wemos D1 Mini |
| Editor Kode | Arduino IDE |
| Alat Pemrogram | ST-Link/V2 |
| Alat Komunikasi Serial | USB FTDI |
| Driver | • ST-Link USB Driver<br>• CDM FTDI USB Driver<br>• CH340 USB Driver |
| Dukungan Aplikasi | Bot Whatsapp |
| Platform IoT | • Twilio<br>• ThingESP |
| Protokol Komunikasi | • Serial Peripheral Interface (SPI)<br>• Hypertext Transfer Protocol (HTTP) |
| Arsitektur IoT | 4 Lapisan |
| Bahasa Pemrograman | C/C++ |
| Pustaka Arduino | • SPI (default)<br>• ThingESP |
| Sensor | • MH-RD: Sensor Tetesan Air Hujan (x1)<br>• LDR: Sensor Intensitas Cahaya (x1)<br>• LM35: Sensor Suhu Udara (x1) |
| Komponen Lainnya | • Kabel USB Mikro - USB tipe A (x1)<br>• Kabel jumper (1 set)<br>• Breadboard (x1) |

<br><br>

## Unduh & Instal
1. Arduino IDE

   <table><tr><td width="810">
         
   ```
   https://bit.ly/ArduinoIDE_Installer
   ```

   </td></tr></table><br>

2. CDM FTDI USB Driver

   <table><tr><td width="810">

   ```
   https://bit.ly/CDM_FTDI_USB_Driver
   ```

   </td></tr></table><br>

3. ST-Link USB Driver

   <table><tr><td width="810">

   ```
   https://bit.ly/STLink_USB_Driver
   ```

   </td></tr></table><br>
   
4. STM32CubeProgrammer

   <table><tr><td width="810">
   
   ```
   https://bit.ly/STM32_Cube_Programmer_Installer
   ```

   </td></tr></table><br>
   
5. CH340 USB Driver

   <table><tr><td width="810">
   
   ```
   https://bit.ly/CH340_USB_Driver
   ```
   
   </td></tr></table>
   
<br><br>

## Rancangan Proyek
<table>
<tr>
<th width="420">Diagram Blok</th>
<th width="420">Infrastruktur</th>
</tr>
<tr>
<td><img src="Assets/Documentation/Diagram/Block Diagram.jpg" alt="block-diagram"></td>
<td><img src="Assets/Documentation/Diagram/Infrastructure.jpg" alt="infrastructure"></td>
</tr>
</table>
<table>
<tr>
<th width="420">Diagram Ilustrasi</th>
<th width="420">Pengkabelan</th>
</tr>
<tr>
<td><img src="Assets/Documentation/Diagram/Pictorial Diagram.jpg" alt="pictorial-diagram"></td>
<td><img src="Assets/Documentation/Table/Device Wiring.jpg" alt="wiring"></td>
</tr>
</table>

<br><br>

## Pengetahuan Dasar
Pada dasarnya, suatu perangkat itu dapat dikomunikasikan dengan perangkat lain baik secara nirkabel maupun dengan kabel. Komunikasi antar perangkat keras yang umum digunakan salah satunya adalah ``` Komunikasi Serial ```. Dapat diketahui bersama bahwa ``` Komunikasi Serial ``` ini ada tiga jenis, yaitu meliputi: ``` UART (Universal Asynchronous Receiver-Transmitter) ```, ``` SPI (Serial Peripheral Interface) ```, dan ``` I2C (Inter Integrated Circuit) ```. ``` Serial Peripheral Interface (SPI) ``` merupakan ``` komunikasi serial sinkron ``` yang digunakan oleh mikrokontroler untuk dapat berkomunikasi dengan satu atau lebih perangkat periferal dalam jarak yang dekat. Hal ini juga dapat digunakan untuk komunikasi antara dua mikrokontroler. ``` Komunikasi Serial SPI ``` memungkinkan suatu perangkat dapat bertindak sebagai ``` master ``` atau ``` slave ```. ``` Master ``` adalah perangkat utama yang memiliki otoritas penuh atas kontrol Slave, sedangkan ``` Slave ``` adalah perangkat sekunder yang berada di bawah otoritas perangkat Master. ``` Komunikasi SPI ``` membutuhkan 3 jalur yaitu ``` MOSI ```, ``` MISO ```, dan ``` SCK ```. ``` MOSI (Master Output Slave Input) ``` artinya jika dikonfigurasi sebagai ``` master ``` maka ``` pin MOSI berlaku sebagai output ```, tetapi jika dikonfigurasi sebagai ``` slave ``` maka ``` pin MOSI berlaku sebagai input ```. ``` MISO (Master Input Slave Output) ``` artinya jika dikonfigurasi sebagai ``` master ``` maka ``` pin MISO berlaku sebagai input ```, tetapi jika dikonfigurasi sebagai ``` slave ``` maka ``` pin MISO berlaku sebagai output ```. ``` CLK (Clock) ``` artinya jika dikonfigurasi sebagai ``` master ``` maka ``` pin CLK berlaku sebagai output ```, tetapi jika dikonfigurasi sebagai ``` slave ``` maka ``` pin CLK berlaku sebagai input ```.

<br><br>

## Pengaturan Arduino IDE
1. Buka ``` Arduino IDE ``` terlebih dahulu, kemudian buka proyek dengan cara klik ``` File ``` -> ``` Open ``` :

   <table><tr><td width="810">
   
      • ``` Master.ino ```
      
      • ``` Slave.ino ```

   </td></tr></table><br>
   
2. Isi ``` Url Pengelola Papan Tambahan ``` di Arduino IDE

   <table><tr><td width="810">
      
      Klik ``` File ``` -> ``` Preferences ``` -> masukkan ``` Boards Manager Url ``` dengan menyalin tautan berikut :
   
      ```
      https://github.com/stm32duino/BoardManagerFiles/raw/main/package_stmicroelectronics_index.json
      http://arduino.esp8266.com/stable/package_esp8266com_index.json
      ```

   </td></tr></table><br>
   
3. ``` Pengaturan Board ``` di Arduino IDE

   <table>
      <tr><th>
         
      i
         
      </th><th width="780">
            
      Cara mengatur board ``` STM32F103C8T6 ```
   
      </th></tr>
      <tr><td colspan="2">

      • Klik ``` Tools ``` -> ``` Board ``` -> ``` Boards Manager ``` -> Instal ``` STM32 MCU based boards ```.

      • Kemudian klik ``` Tools ``` -> ``` Board ``` -> ``` STM32 boards groups ``` -> ``` Generic STM32F1 series ```.
              
      </td></tr>
   </table><br><table>
      <tr><th>
         
      ii
         
      </th><th width="775">

      Cara mengatur board ``` Wemos D1 Mini ```
            
      </th></tr>
      <tr><td colspan="2">

      • Klik bagian ``` Tools ``` -> ``` Board ``` -> ``` Boards Manager ``` -> Instal ``` esp8266 ```.

      • Kemudian klik ``` Tools ``` -> ``` Board ``` -> ``` ESP8266 Boards ``` -> ``` Wemos D1 Mini ```.
            
      </td></tr>
   </table><br>
   
4. ``` Ubah Kecepatan Papan ``` di Arduino IDE

   <table>
      <tr><th>
         
      i
         
      </th><th width="780">
            
      Cara mengubah kecepatan board ``` STM32F103C8T6 ```
   
      </th></tr>
      <tr><td colspan="2">

      Klik ``` Tools ``` -> ``` Upload Speed ``` -> ``` 9600 ```
              
      </td></tr>
   </table><br><table>
      <tr><th>
         
      ii
         
      </th><th width="775">

      Cara mengubah kecepatan board ``` Wemos D1 Mini ```
            
      </th></tr>
      <tr><td colspan="2">

      Klik ``` Tools ``` -> ``` Upload Speed ``` -> ``` 115200 ```
            
      </td></tr>
   </table><br>
   
5. ``` Ubah Nomor Bagian Papan ``` di Arduino IDE

   <table>
     <tr><th>
         
      Cara mengubah nomor bagian board ``` STM32F103C8T6 ```

     </th></tr>
     <tr><td width="810">
         
      Klik ``` Tools ``` -> ``` Board part number ``` -> ``` BluePill F103C8 ```

     </td></tr>
   </table><br>
   
6. ``` Ubah Dukungan U(S)ART ``` di Arduino IDE

   <table>
     <tr><th>
         
      Cara mengubah dukungan U(S)ART board ``` STM32F103C8T6 ```

     </th></tr>
     <tr><td width="810">
         
      Klik ``` Tools ``` -> ``` U(S)ART Support ``` -> ``` Enabled (generic 'Serial') ```

     </td></tr>
   </table><br>

7. ``` Ubah Metode Pengunggahan ``` di Arduino IDE
  
   <table>
     <tr><th>
         
      Cara mengubah metode pengunggahan board ``` STM32F103C8T6 ```

     </th></tr>
     <tr><td width="810">
         
      Klik ``` Tools ``` -> ``` Upload method ``` -> ``` STM32CubeProgrammer (SWD) ```

     </td></tr>
   </table><br>
   
8. ``` Instal Pustaka ``` di Arduino IDE

   <table><tr><td width="810">
     
      Unduh semua file zip pustaka. Lalu tempelkan di: ``` C:\Users\Computer_Username\Documents\Arduino\libraries ```

   </td></tr></table><br>

9. ``` Pengaturan Port ``` di Arduino IDE

   <table><tr><td width="810">

      Klik ``` Port ``` -> pilih sesuai dengan port perangkat anda ``` (anda dapat melihatnya di Device Manager) ```
         
   </td></tr></table><br>

10. Ubah ``` Nama WiFi ```, ``` Kata Sandi WiFi ```, dan sebagainya sesuai dengan apa yang anda gunakan saat ini.<br><br>

11. Sebelum mengunggah program, silakan klik: ``` Verify ```.<br><br>

12. Jika tidak ada kesalahan dalam kode program, langkah selanjutnya yaitu menggunakan alat pemrograman ``` STM32 ``` sesuai dengan prosedur. Kemudian klik: ``` Upload ```. Sedangkan ``` Wemos D1 Mini ``` dapat dilakukan secara langsung tanpa menggunakan alat pemrograman.<br><br>

13. Jika masih ada masalah saat unggah program, maka coba periksa pada bagian ``` driver ``` / ``` port ``` / ``` alat pemrogram ``` / ``` yang lainnya ```.

<br><br>

## Pengaturan ST-Link/V2
<img width="840" src="Assets/Documentation/Experiment/ST-Link Configuration.jpg" alt="stlink-configuration"><br><br>

<strong>Catatan :</strong>

<table><tr><td width="840">

   • Modul antarmuka JTAG atau ``` Debugging Kabel Serial (SWD) ``` pada dasarnya digunakan untuk berkomunikasi dengan board ``` STM32 ```.
   
   • Pemasangan kabel antara ``` ST-Link/V2 ``` dengan board ``` STM32 ``` dapat anda lihat selengkapnya pada gambar di atas.

   • Untuk mengunggah program, selain menggunakan ``` ST-Link/V2 ```, anda juga dapat menggunakan alat pemrogram lainnya seperti: ``` USB CP2102 ```, ``` USB CH340 ```, ``` USB PL2303 ``` , atau dengan ``` USB FTDI ```.
   
   • Berdasarkan pengalaman, saya akui bahwa menggunakan ``` ST-Link/V2 ``` jauh lebih baik daripada alat pemrogram lainnya karena prosesnya lebih mudah, lebih cepat, dan lebih stabil.

</td></tr></table>

<br><br>

## Pengaturan USB FTDI
<img width="840" src="Assets/Documentation/Experiment/FTDI Configuration.jpg" alt="ftdi-configuration"><br><br>

<strong>Catatan :</strong>

   <table><tr><td width="840">

   • Komunikasi serial pada board ``` STM32 ``` ini sangat dimungkinkan terjadi, terutama untuk keperluan ``` Serial Monitor ``` dan ``` Serial Plotter ```. Alat yang dapat dipakai untuk komunikasi serial antara lain: ``` USB CP2102 ```, ``` USB CH340 ```, ``` USB FTDI ```, atau dengan ``` USB PL2303 ```.
   
   • Pemasangan kabel antara ``` USB FTDI ``` dengan board ``` STM32 ``` dapat anda lihat detailnya pada gambar di atas.

   • Berdasarkan pengalaman, saya akui bahwa penggunaan ``` USB FTDI ``` atau ``` USB CP2102 ``` itu jauh lebih baik daripada ``` USB PL2303 ``` maupun ``` USB CH340 ``` karena diketahui kinerjanya lebih stabil.

   </td></tr></table><br>

<br><br>

## Pengaturan Twilio
1. Memulai Twilio :
   
   <table><tr><td width="810">
      
   • Buka url berikut ini: <a href="https://www.twilio.com/">Klik Disini</a>.

   • Klik ``` Log in ``` untuk mengakses layanan.

   • Jika anda belum memiliki akun, klik ``` Sign up ```.

   </td></tr></table><br>

2. Isi semua kolom yang diperlukan.<br><br>

3. Verifikasi ``` nomor telepon ``` dan ``` email ``` anda.<br><br>

4. Akses ``` WhatsApp sandbox ``` di menu ``` Settings ``` dan ``` kirimkan kode ``` ke ``` nomor WhatsApp yang disediakan ```.
   
<br><br>

## Pengaturan ThingESP
1. Memulai ThingESP :
   
   <table><tr><td width="810">

   • Buka url berikut ini: <a href="https://thingesp.siddhesh.me/#/">Klik Disini</a>.

   • Klik ``` Login ``` untuk mengakses layanan.

   • Jika anda belum memiliki akun, klik ``` Create Account ```.

   </td></tr></table><br>

2. Isi semua kolom yang diperlukan.<br><br>

3. Klik ``` Project ``` di bagian sidebar -> lalu pilih ``` Add New Project ```.<br><br>

4. Setelah proyek dibuat, masukkan ``` URL Twilio WhatsApp Endpoint ``` ke dalam ``` ThingESP ``` agar dapat terhubung.
   
<br><br>

## Memulai
1. Unduh dan ekstrak repositori ini.<br><br>

2. Pastikan anda memiliki komponen elektronik yang diperlukan.<br><br>
   
3. Pastikan komponen anda telah dirancang sesuai dengan diagram.<br><br>
   
4. Konfigurasikan perangkat anda menurut pengaturan di atas.<br><br>
    
5. Selamat menikmati [Selesai].

<br><br>

## Demonstrasi Aplikasi
Via Whatsapp: <a href="https://github.com/devancakra/Whatsapp-Bot-based-Weather-monitoring-using-SPI-communication/">Weathersia Bot</a>

<br><br>

## Sorotan
<table>
<tr>
<th width="840">Perangkat</th>
</tr>
<tr>
<td><img src="Assets/Documentation/Experiment/Device.jpg" alt="device"></td>
</tr>
</table>
<table>
<tr>
<th width="840" colspan="2">Bot Whatsapp</th>
</tr>
<tr>
<td width="420"><img src="Assets/Documentation/Experiment/Device.jpg" alt="wa-bot1"></td>
<td width="420"><img src="Assets/Documentation/Experiment/Device.jpg" alt="wa-bot2"></td>
</tr>
</table>

<br><br>

## Pengujian Komponen
Anda dapat mengunduh berkas uji komponen melalui tautan berikut: <a href="Assets/Component Testing/Testing.txt">Klik Disini</a>

<br><br>

## Apresiasi
Jika karya ini bermanfaat bagi anda, maka dukunglah karya ini sebagai bentuk apresiasi kepada penulis dengan mengklik tombol ``` ⭐Bintang ``` di bagian atas repositori.

<br><br>

## Penafian
Aplikasi ini merupakan hasil karya saya sendiri dan bukan merupakan hasil plagiat dari penelitian atau karya orang lain, kecuali yang berkaitan dengan layanan pihak ketiga yang meliputi: pustaka, kerangka kerja, dan lain sebagainya.

<br><br>

## LISENSI
LISENSI MIT - Hak Cipta © 2024 - Devan C. M. Wijaya, S.Kom

Dengan ini diberikan izin tanpa biaya kepada siapa pun yang mendapatkan salinan perangkat lunak ini dan file dokumentasi terkait perangkat lunak untuk menggunakannya tanpa batasan, termasuk namun tidak terbatas pada hak untuk menggunakan, menyalin, memodifikasi, menggabungkan, mempublikasikan, mendistribusikan, mensublisensikan, dan/atau menjual salinan Perangkat Lunak ini, dan mengizinkan orang yang menerima Perangkat Lunak ini untuk dilengkapi dengan persyaratan berikut:

Pemberitahuan hak cipta di atas dan pemberitahuan izin ini harus menyertai semua salinan atau bagian penting dari Perangkat Lunak.

DALAM HAL APAPUN, PENULIS ATAU PEMEGANG HAK CIPTA DI SINI TETAP MEMILIKI HAK KEPEMILIKAN PENUH. PERANGKAT LUNAK INI DISEDIAKAN SEBAGAIMANA ADANYA, TANPA JAMINAN APAPUN, BAIK TERSURAT MAUPUN TERSIRAT, OLEH KARENA ITU JIKA TERJADI KERUSAKAN, KEHILANGAN, ATAU LAINNYA YANG TIMBUL DARI PENGGUNAAN ATAU URUSAN LAIN DALAM PERANGKAT LUNAK INI, PENULIS ATAU PEMEGANG HAK CIPTA TIDAK BERTANGGUNG JAWAB, KARENA PENGGUNAAN PERANGKAT LUNAK INI TIDAK DIPAKSAKAN SAMA SEKALI, SEHINGGA RISIKO ADALAH MILIK ANDA SENDIRI.
