# LAB-16-DHCP-Server-dan-Static-Leases
tanggal 14 agustus 2025

# konfigurasi DHCP dan static leases

![m](pppp.png)

Static Lease merupakan sebuah cara yang dapat digunakan pada DHCP Server untuk memberikan sebuah Fixed IP kepada Client.

**Langkah-langkahnya:**

1. masuk ke mikrotik via winbox pilih  
   menu: IP > DHCP CLIENT  
   klik tanda +  
   Setting DHCP Client agar Mikrotik terhubung ke intrnet melalui ether1 yang terhubung ke ISP.  

![I](kull1.PNG)

2. buat ip static buat ether2 di  
   menu: IP > Address  
   klik +  
   seting address untuk interface ether2  

![I](kull2.PNG)

3. membagikan IP ke client secara otomatis.  
   menu: IP > DHCP server > DHCP setup  
   lalu klik next hingga selesai  
   
![I](kull3.PNG)

4. Setting DNS, masukan DNS google.  
   menu: IP > DNS  

![I](kull4.PNG)

5. Setting IP Firewall NAT agar client bisa mengakses ke internet.  
   menu: IP > Firewall > NAT  
   pilih menu sesui gambar di bawah   

![I](kull5.PNG)

6. Pindah ke PC Client untuk setting  obtain auto di IPv4.    

![I](kull8.PNG)

7. pengujian dengan cara cek detail di laptop client.
         
Laptop 1  

![I](kulpc1.PNG)

Laptop 2  

![I](fshuehsiuby-,.045.PNG)

8. Jika PC Client sudah mendapat IP, buka kembali Winboxnya
   Buka IP > DHCP SERVER > Lease
9. pilih MAC Client yang akan di static kan.
10. Klik Make static agar perangkat itu punya IP yang tetap tanpa perlu setting IP manual.
Sekarang client yang sudah di config menjadi static lease akan mendapatkan IP yang sama terus walau mengunakan auto obtain.
# kesimpulan 
Dengan menerapkan Static Lease, teman-teman bisa mendapatkan IP 'pseudo-Static' meski menggunakan DHCP Server.
