# router_on_stick
Implementasi topologi jaringan dengan Router on a Stick, di mana satu router digunakan untuk mengelola beberapa VLAN pada jaringan yang tersegmentasi menggunakan switch managed. 

## Komponen yang Digunakan
1. Router2811: Menggunakan port fisik untuk menghubungkan subnet yang berbeda.
2. ISR 4321: Dikonfigurasi dengan sub-interface menggunakan encapsulation dot1Q untuk mengelola VLAN.
3. Switch Managed Cisco 2960: Digunakan untuk mengelola VLAN dan menghubungkan perangkat jaringan.
4. PC dan laptop yang ditempatkan pada berbagai VLAN.
   
## Jaringan VLAN:
Terdiri dari VLAN15, VLAN25, dan VLAN35 dengan subnet masing-masing.

## Konfigurasi yang Digunakan
1. Router ISR 4321:
Sub-interface dibuat untuk setiap VLAN dengan IP yang sesuai untuk masing-masing subnet,
Routing antar VLAN diaktifkan sehingga perangkat dari VLAN berbeda dapat saling berkomunikasi.
2. Switch Cisco 2960:
VLAN didefinisikan dan port-port pada switch dihubungkan ke VLAN tertentu,
Port trunk diatur untuk membawa semua VLAN ke router melalui koneksi tunggal.
3. Router 2811:
Konfigurasi dasar untuk mendukung routing antar subnet tanpa VLAN tagging.

