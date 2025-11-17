# Jarkom Modul 4 2025 K-30

| Nama                          | NRP        |
|-------------------------------|------------|
| Putu Yudi Nandanjaya Wiraguna | 5027241080 |

## CPT VLSM

Pertama-tama buatlah topologi pada platform **Cisco Packet Tracker**. Agar memudahkan pengerjaan, kelompokkan subnet-subnet dan berikan nama seperti, A1, A2, dll. Dalam topologi saya sendiri terdapat 23 subnet. 

<img width="1536" height="687" alt="image" src="https://github.com/user-attachments/assets/233e8fd0-38bd-4f87-bbde-6278df7f64e9" />

**Berikut merupakan rute dari subnet-subnet :**

| Nama Subnet | Rute                                                                                | Jumlah IP          | Netmask |
| ----------- | ----------------------------------------------------------------------------------- | ------------------ | ------- |
| **A1**      | Amonsul > Minastir                                                                  | 2                  | /30     |
| **A2**      | Amonsul > Minastir > Anor                                                           | 2                  | /30     |
| **A3**      | Amonsul > Minastir > Amroth                                                         | 2                  | /30     |
| **A4**      | Amonsul > Minastir > Amroth > Switch0 > Morgoth, Throne                             | 3                  | /29     |
| **A5**      | Amonsul > Minastir > Anor > Switch1 > Beacon, Silmarils                             | 1 + 279 + 381      | /22     |
| **A6**      | Amonsul > Minastir > Amroth > Switch0 > Throne > Erebor                             | 1 + 2              | /29     |
| **A7**      | Amonsul > Minastir > Amroth > Switch0 > Morgoth > Switch2 > Erendis, Elrond         | 1 + 27 + 34        | /26     |
| **A8**      | Amonsul > Fornost                                                                   | 2                  | /30     |
| **A9**      | Amonsul > Fornost > Switch3 > Valinor, Valmar                                       | 3                  | /29     |
| **A10**     | Amonsul > Fornost > Switch3 > Valinor > Switch4 > Shadow, Anarion, Lindon           | 1 + 99 + 67 + 132  | /23     |
| **A11**     | Amonsul > Fornost > Switch3 > Valmar > Switch5 > Doriath, Arnor                     | 1 + 17 + 10        | /27     |
| **A12**     | Amonsul > Fornost > Switch3 > Valmar > Switch6 > Imrahil, Utumno, Gwaith            | 1 + 27 + 2 + 4     | /26     |
| **A13**     | Amonsul > Eregion                                                                   | 2                  | /30     |
| **A14**     | Amonsul > Eregion > Switch12 > Mirkwood, Morgul                                     | 1 + 23 + 102       | /25     |
| **A15**     | Amonsul > Eregion > Numenor                                                         | 2                  | /30     |
| **A16**     | Amonsul > Eregion > Numenor > Guldur                                                | 2                  | /30     |
| **A17**     | Amonsul > Eregion > Numenor > Guldur > Switch11 > Palantir, Edhil                   | 1 + 73 + 46        | /25     |
| **A18**     | Amonsul > Eregion > Numenor > Guldur > Switch10 > Ironcrown, Grond, Hobbiton        | 1 + 5 + 4 + 4      | /28     |
| **A19**     | Amonsul > Eregion > Numenor > Switch7 > Arthedain, Mirdain                          | 1 + 246 + 628      | /22     |
| **A20**     | Amonsul > Eregion > Numenor > Moldor                                                | 2                  | /30     |
| **A21**     | Amonsul > Eregion > Numenor > Moldor > Erain                                        | 2                  | /30     |
| **A22**     | Amonsul > Eregion > Numenor > Moldor > Erain > Switch8 > Balrog, Gothmog, Thranduil | 1 + 256 + 84 + 129 | /23     |
| **A23**     | Amonsul > Eregion > Numenor > Moldor > Erain > Switch9 > Melkor, Khazad             | 1 + 250 + 252      | /23     |

Total Kebutuhan
- Total Host: 3219
- Netmask Agregat: /20

**Berikut merupakan pembagian IP :**

| Subnet  | Network ID    | Netmask         | Broadcast      | Range IP                      |
| ------- | ------------- | --------------- | -------------- | ----------------------------- |
| **A1**  | 192.226.0.0   | 255.255.255.252 | 192.226.0.3    | 192.226.0.1 – 192.226.0.2     |
| **A2**  | 192.226.0.4   | 255.255.255.252 | 192.226.0.7    | 192.226.0.5 – 192.226.0.6     |
| **A3**  | 192.226.0.8   | 255.255.255.252 | 192.226.0.11   | 192.226.0.9 – 192.226.0.10    |
| **A4**  | 192.226.0.40  | 255.255.255.248 | 192.226.0.47   | 192.226.0.41 – 192.226.0.46   |
| **A5**  | 192.226.8.0   | 255.255.252.0   | 192.226.11.255 | 192.226.8.1 – 192.226.11.254  |
| **A6**  | 192.226.0.48  | 255.255.255.248 | 192.226.0.55   | 192.226.0.49 – 192.226.0.54   |
| **A7**  | 192.226.0.128 | 255.255.255.192 | 192.226.0.191  | 192.226.0.129 – 192.226.0.190 |
| **A8**  | 192.226.0.12  | 255.255.255.252 | 192.226.0.15   | 192.226.0.13 – 192.226.0.14   |
| **A9**  | 192.226.0.56  | 255.255.255.248 | 192.226.0.63   | 192.226.0.57 – 192.226.0.62   |
| **A10** | 192.226.2.0   | 255.255.254.0   | 192.226.3.255  | 192.226.2.1 – 192.226.3.254   |
| **A11** | 192.226.0.96  | 255.255.255.224 | 192.226.0.127  | 192.226.0.97 – 192.226.0.126  |
| **A12** | 192.226.0.192 | 255.255.255.192 | 192.226.0.255  | 192.226.0.193 – 192.226.0.254 |
| **A13** | 192.226.0.16  | 255.255.255.252 | 192.226.0.19   | 192.226.0.17 – 192.226.0.18   |
| **A14** | 192.226.1.0   | 255.255.255.128 | 192.226.1.127  | 192.226.1.1 – 192.226.1.126   |
| **A15** | 192.226.0.20  | 255.255.255.252 | 192.226.0.23   | 192.226.0.21 – 192.226.0.22   |
| **A16** | 192.226.0.32  | 255.255.255.252 | 192.226.0.35   | 192.226.0.33 – 192.226.0.34   |
| **A17** | 192.226.1.128 | 255.255.255.128 | 192.226.1.255  | 192.226.1.129 – 192.226.1.254 |
| **A18** | 192.226.0.64  | 255.255.255.240 | 192.226.0.79   | 192.226.0.65 – 192.226.0.78   |
| **A19** | 192.226.12.0  | 255.255.252.0   | 192.226.15.255 | 192.226.12.1 – 192.226.15.254 |
| **A20** | 192.226.0.24  | 255.255.255.252 | 192.226.0.27   | 192.226.0.25 – 192.226.0.26   |
| **A21** | 192.226.0.28  | 255.255.255.252 | 192.226.0.31   | 192.226.0.29 – 192.226.0.30   |
| **A22** | 192.226.4.0   | 255.255.254.0   | 192.226.5.255  | 192.226.4.1 – 192.226.5.254   |
| **A23** | 192.226.6.0   | 255.255.254.0   | 192.226.7.255  | 192.226.6.1 – 192.226.7.254   |

**Tree penyebaran IP :**

<img width="1181" height="743" alt="image" src="https://github.com/user-attachments/assets/f480dad8-4aa2-4673-96f9-a6319e430bfd" />

### Metodologi Alokasi IP (Subnetting)

**Tujuan Utama**: Tujuan dari metodologi ini adalah efisiensi alokasi IP. Dengan jaringan yang memiliki kebutuhan sangat beragam—dari 2 host hingga lebih dari 800 host—metode ini memastikan bahwa setiap subnet mendapatkan alamat yang "pas" tanpa membuang-buang IP.

**Metode yang Digunakan**: Saya menggunakan VLSM (Variable Length Subnet Masking). Metode ini memungkinkan penggunaan prefix (netmask) yang berbeda-beda untuk setiap subnet, disesuaikan dengan kebutuhan host-nya.

**Proses Alokasi**: Proses ini mengikuti strategi "Largest First" (Terbesar Dulu) untuk mencegah fragmentasi blok alamat:

- **Analisis Kebutuhan Host**: Pertama, saya menghitung total host yang dibutuhkan untuk setiap subnet (termasuk PC, server, dan 1 IP untuk gateway router).

- **Pengurutan Subnet**: Subnet diurutkan, bukan berdasarkan nama (A1, A2...), tetapi berdasarkan jumlah host terbanyak hingga yang paling sedikit.

- **Alokasi Blok**: Saya mengalokasikan blok IP mulai dari subnet terbesar. Subnet seperti A19 (875 host) dan A5 (661 host) mendapatkan blok besar /22 (1022 IP) terlebih dahulu. Setelah semua blok besar ditempatkan, sisa ruang IP dipecah-pecah untuk subnet yang lebih kecil, seperti /26 (62 IP) dan /30 (2 IP) untuk link antar router.

**Hasil (Kesimpulan)**: Network ID terlihat "melompat" (misalnya, A1 ada di 192.226.0.0 sementara A5 ada di 192.226.8.0) karena alokasi ini didasarkan pada ukuran kebutuhan, bukan urutan nama. Ini adalah hasil yang disengaja dari proses VLSM yang efisien.
