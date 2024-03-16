[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/Telegram-Bot-based-Weather-monitoring-using-SPI-communication)
![Project](https://img.shields.io/badge/Project-SPI-light.svg?style=flat&logo=arduino&logoColor=white&color=%23F7DF1E)

# Whatsapp-Bot-based-Weather-monitoring-using-SPI-communication
<strong>Proyek Tunggal: Pemantauan cuaca berbasis Bot Whatsapp menggunakan komunikasi SPI</strong><br><br>
Segera Hadir...

<br><br>

## Kebutuhan Proyek
| Bagian | Deskripsi |
| --- | --- |
| Papan Pengembangan | • STM32F103C8T6<br>• Wemos D1 Mini |
| Editor Kode | Arduino IDE |
| Alat Pemrogram | ST-Link/V2 |
| Alat Komunikasi Serial | USB FTDI |
| Driver | • ST-Link<br>• USB-Serial CH340 |
| Dukungan Aplikasi | Bot Whatsapp |
| Platform IoT | • Twilio<br>• ThingESP |
| Protokol Komunikasi | • Serial Peripheral Interface (SPI)<br>• Hypertext Transfer Protocol (HTTP) |
| Arsitektur IoT | 3 Lapisan |
| Bahasa Pemrograman | C/C++ |
| Pustaka Arduino | • SPI (default)<br>• ThingESP |
| Sensor | • MH-RD: Modul Sensor Tetesan Air Hujan (x1)<br>• Modul Sensor LDR (x1)<br>• LM35: Suhu Udara (x1) |
| Komponen Lainnya | • Kabel Mikro USB - USB tipe A (x1)<br>• Kabel jumper (1 set)<br>• Breadboard (x1) |

<br><br>

## Unduh & Instal
1. Arduino IDE

   <table><tr><td width="810">
         
   ```
   https://www.arduino.cc/en/software
   ```

   </td></tr></table><br>

2. ST-Link Driver

   <table><tr><td width="810">

   ```
   https://bit.ly/STLink_Driver
   ```

   </td></tr></table><br>

3. STM32CubeProgrammer

   <table><tr><td width="810">
   
   ```
   https://bit.ly/STM32_Cube_Programmer
   ```

   </td></tr></table><br>
   
4. USB-Serial CH340

   <table><tr><td width="810">
   
   ```
   https://bit.ly/CH340_Driver
   ```
   
   </td></tr></table>
   
<br><br>

## Rancangan Proyek
<table>
<tr>
<th width="420">Diagram Blok</th>
<th width="420">Diagram Ilustrasi</th>
</tr>
<tr>
<td><img src="" alt="Block-Diagram"></td>
<td><img src="" alt="Pictorial-Diagram"></td>
</tr>
</table>
<table>
<tr>
<th width="840">Pengkabelan</th>
</tr>
<tr>
<td><img src="" alt="Wiring"></td>
</tr>
</table>

<br><br>

## Pengetahuan Dasar
Pada dasarnya, suatu perangkat itu dapat dikomunikasikan dengan perangkat lain baik secara nirkabel maupun dengan kabel. Komunikasi antar perangkat keras yang umum digunakan salah satunya adalah ``` Komunikasi Serial ```. Dapat diketahui bersama bahwa ``` Komunikasi Serial ``` ini ada tiga jenis, yaitu meliputi: ``` UART (Universal Asynchronous Receiver-Transmitter) ```, ``` SPI (Serial Peripheral Interface) ```, dan ``` I2C (Inter Integrated Circuit) ```.

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
<img width="840" src="https://github.com/devancakra/Whatsapp-Bot-based-Weather-monitoring-using-SPI-communication/assets/54527592/54bf34f8-62c0-482e-8e91-0ab1fe603b76"><br><br>

<strong>Catatan :</strong>

<table><tr><td width="840">

   • Modul antarmuka JTAG atau ``` Debugging Kabel Serial (SWD) ``` pada dasarnya digunakan untuk berkomunikasi dengan board ``` STM32 ```.
   
   • Pemasangan kabel antara ``` ST-Link/V2 ``` dengan board ``` STM32 ``` dapat anda lihat selengkapnya pada gambar di atas.

   • Untuk mengunggah program, selain menggunakan ``` ST-Link/V2 ```, anda juga dapat menggunakan alat pemrogram lainnya seperti: ``` USB CP2102 ```, ``` USB CH340 ```, ``` USB PL2303 ``` , atau dengan ``` USB FTDI ```.
   
   • Berdasarkan pengalaman, saya akui bahwa menggunakan ``` ST-Link/V2 ``` jauh lebih baik daripada alat pemrogram lainnya karena prosesnya lebih mudah, lebih cepat, dan lebih stabil.

</td></tr></table>

<br><br>

## Pengaturan USB FTDI
<img width="840" src=""><br><br>

<strong>Catatan :</strong>

   <table><tr><td width="840">

   • Komunikasi serial pada board ``` STM32 ``` ini sangat dimungkinkan terjadi, terutama untuk keperluan ``` Serial Monitor ``` dan ``` Serial Plotter ```. Alat yang dapat dipakai untuk komunikasi serial antara lain: ``` USB CP2102 ```, ``` USB CH340 ```, ``` USB FTDI ```, atau dengan ``` USB PL2303 ```.
   
   • Pemasangan kabel antara ``` USB FTDI ``` dengan board ``` STM32 ``` dapat anda lihat detailnya pada gambar di atas.

   • Berdasarkan pengalaman, saya akui bahwa penggunaan ``` USB FTDI ``` atau ``` USB CP2102 ``` itu jauh lebih baik daripada ``` USB PL2303 ``` maupun ``` USB CH340 ``` karena diketahui kinerjanya lebih stabil.

   </td></tr></table><br>

<br><br>

## Pengaturan Bot Whatsapp
Segera Hadir...

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
<th width="840">Perangkat Keras</th>
</tr>
<tr>
<td><img src="" alt="hardware"></td>
</tr>
</table>
<table>
<tr>
<th width="840" colspan="2">Bot Whatsapp</th>
</tr>
<tr>
<td width="420"><img src="" alt="wa_bot1"></td>
<td width="420"><img src="" alt="wa_bot2"></td>
</tr>
</table>

<br><br>

## Pengujian Komponen
Anda dapat mengunduh berkas uji komponen melalui tautan berikut: <a href="https://github.com/devancakra/Whatsapp-Bot-based-Weather-monitoring-using-SPI-communication/">Klik Disini</a>

<br><br>

## Apresiasi
Jika anda merasa karya ini bermanfaat, dukunglah karya ini sebagai bentuk apresiasi kepada penulis dengan cara mengeklik tombol ``` ⭐Bintang ```.

<br><br>

## Penafian
Aplikasi ini dibuat dengan menyertakan sumber-sumber dari pihak ketiga. Pihak ketiga di sini adalah penyedia layanan, yang layanannya berupa pustaka, kerangka kerja, dan lain-lain. Saya ucapkan terima kasih banyak atas layanannya. Telah terbukti sangat membantu dan dapat diimplementasikan.

<br><br>

## LISENSI
LISENSI MIT - Hak Cipta © 2024 - Devan C. M. Wijaya, S.Kom

Dengan ini diberikan izin tanpa biaya kepada siapa pun yang mendapatkan salinan perangkat lunak ini dan file dokumentasi terkait perangkat lunak untuk menggunakannya tanpa batasan, termasuk namun tidak terbatas pada hak untuk menggunakan, menyalin, memodifikasi, menggabungkan, mempublikasikan, mendistribusikan, mensublisensikan, dan/atau menjual salinan Perangkat Lunak ini, dan mengizinkan orang yang menerima Perangkat Lunak ini untuk dilengkapi dengan persyaratan berikut:

Pemberitahuan hak cipta di atas dan pemberitahuan izin ini harus menyertai semua salinan atau bagian penting dari Perangkat Lunak.

DALAM HAL APAPUN, PENULIS ATAU PEMEGANG HAK CIPTA DI SINI TETAP MEMILIKI HAK KEPEMILIKAN PENUH. PERANGKAT LUNAK INI DISEDIAKAN SEBAGAIMANA ADANYA, TANPA JAMINAN APAPUN, BAIK TERSURAT MAUPUN TERSIRAT, OLEH KARENA ITU JIKA TERJADI KERUSAKAN, KEHILANGAN, ATAU LAINNYA YANG TIMBUL DARI PENGGUNAAN ATAU URUSAN LAIN DALAM PERANGKAT LUNAK INI, PENULIS ATAU PEMEGANG HAK CIPTA TIDAK BERTANGGUNG JAWAB, KARENA PENGGUNAAN PERANGKAT LUNAK INI TIDAK DIPAKSAKAN SAMA SEKALI, SEHINGGA RISIKO ADALAH MILIK ANDA SENDIRI.
