# Laporan Resmi Praktikum Modul 4 Jarkom Kelompok D06
Dokumen laporan resmi praktikum modul 4 Jarkom Kelompok D06 Jaringan Komputer D Tahun 2022/2023

### Anggota Kelompok:
Nama Lengkap                | NRP
--------------------------- | -------------
Fian Awamiry Maulana        | 5025201035 
Rere Arga Dewanata          | 5025201078 
Muhamad Ridho Pratama       | 5025201186  

Kami menggunakan dua tools pada praktikum ini, yaitu:   
1. CPT untuk konfigurasi Variable Length Subnet Mask (VLSM)   
2. GNS3 untuk konfigurasi Classless Inter Domain Routing (CIDR)

## Konfigurasi Variable Length Subnet Mask (VLSM) di Cisco Packet Tracer
Berikut adalah pengelompokkan subnet pada topologi.  
![Modul4_Subnet-NID drawio](https://user-images.githubusercontent.com/82325182/203382599-b3edc2b0-c594-434a-81d8-e12b87d77e8d.png)  
Dibawah ini merupakan Tree Variable Length Subnet Mask (VLSM):  
![TREE_VLSM](https://user-images.githubusercontent.com/55425460/204121898-5bf81a4b-95a1-4430-a9fe-717febb620a4.png)
Berdasarkan pengelompokkan subnet tersebut, kami membuat tabel untuk penjelasan pembagian subnet dan network ID yang telah dibuat:
![Pembagian Network ID](https://user-images.githubusercontent.com/55425460/204121988-f76a920b-d4f8-4820-ac10-bdfd0d74e49c.png)

Di bawah ini merupakan konfigurasi pada setiap PC:  
### PC Guideau (1000 Host)
![image](https://user-images.githubusercontent.com/82325182/203384335-b51fd07b-4a32-4612-b2fe-0ac2e31e102e.png)
### PC Johan (100 Host)
![image](https://user-images.githubusercontent.com/82325182/203384870-30a958e3-8e2d-4d15-92ab-c9792221a65a.png)
### PC Phanora (150 Host)
![image](https://user-images.githubusercontent.com/82325182/203385022-b5ea1979-821d-4156-ad7a-7b8f87fb1be8.png)
### PC Keith (210 Host)
![PC Keith](https://user-images.githubusercontent.com/55425460/204121617-73c0d182-c685-42d2-8de6-81038ad92c20.png)
### PC Oakleave (500 Host)
![image](https://user-images.githubusercontent.com/82325182/203385194-453b3723-4f59-4683-8b06-f9dc16fa6b0f.png)
### PC Matt Cugaff (120 Host)
![image](https://user-images.githubusercontent.com/82325182/203385429-ef836cc5-8aab-46c1-9201-793cdb856a48.png)
### PC Ashaf (50 Host)
![PC Ashaf](https://user-images.githubusercontent.com/55425460/204121603-0f4b04d4-77ea-44b0-b28d-0c08c0260489.png)
### PC Haines (70 Host)
![image](https://user-images.githubusercontent.com/82325182/203385694-b555d75f-85d8-4027-9680-062495802d9a.png)
### PC Spendrow (120 Host)
![image](https://user-images.githubusercontent.com/82325182/203385761-a7c70cd4-6855-4bb9-9d0b-49386365eaa7.png)
### PC Heiga (70 Host)
![image](https://user-images.githubusercontent.com/82325182/203385852-fc1e5665-1293-4d0d-bab5-54a33913bc46.png)
### PC Corvekt (200 Host)
![image](https://user-images.githubusercontent.com/82325182/203386091-eccd9310-0195-4fcf-a8a9-b2dd2fa5fa34.png)

### Server The Beast
![Server The Beast](https://user-images.githubusercontent.com/55425460/204121630-e29e4bfd-bf7e-4adb-bf3e-473e8cdbf5a8.png)

### Server The Witch
![Server The Witch](https://user-images.githubusercontent.com/55425460/204121636-4f3837a0-c056-4abd-94a4-f5c569b400b0.png)


## Pengaturan Routing VLSM di Cisco Packet Tracer

Cara menambahkan ke routing table:
   1.  Klik pada router yang diinginkan
   2.  Masuk ke tab `Config`
   3.  Masuk ke bagian `Static`
   4.  Masukkan Network ID yang dituju, subnet mask-nya, dan next hop-nya, lalu klik `Add`

### The Resonance

   1. 10.18.11.128/26 via 10.18.11.202
   2. 10.18.11.196/30 via 10.18.11.202
   3. 10.18.11.192/30 via 10.18.11.202
   4. 10.18.0.0/22 via 10.18.11.202
   5. 10.18.8.0/24 via 10.18.11.202
   6. 10.18.6.0/23 via 10.18.11.206
   7. 10.18.11.220/30 via 10.18.11.214
   8. 10.18.10.0/25 via 10.18.11.214
   9. 10.18.11.216/30 via 10.18.11.214
   10. 10.18.9.0/24 via 10.18.11.214
   11. 10.18.4.0/23 via 10.18.11.214
   12. 10.18.11.224/30 via 10.18.11.214
   13. 10.18.11.0/25 via 10.18.11.214
   14. 10.18.10.128/25 via 10.18.11.214

   ![The Resonance Routing](https://user-images.githubusercontent.com/55425460/204121645-26b88201-d5d4-4549-a4da-1dd584036b0e.png)

### The Order

   1. 0.0.0.0/0 via 10.18.11.201
   2. 10.18.11.192/30 via 10.18.11.198
   3. 10.18.0.0/22 via 10.18.11.198
   4. 10.18.8.0/24 via 10.18.11.198

   ![The Order Routing](https://user-images.githubusercontent.com/55425460/204121650-858c9247-6b4c-469a-bde3-e2330a71726c.png)

### The Minister

   1.  0.0.0.0/0 via 10.18.11.197
   2.  10.18.8.0/24 via 10.18.11.194
   
   ![The Minister Routing](https://user-images.githubusercontent.com/55425460/204121659-d119641b-720a-43c4-9375-9a0944790225.png)

### The Dauntless

   1.  0.0.0.0/0 via 10.18.11.193

   ![The Dauntless Routing](https://user-images.githubusercontent.com/55425460/204121676-ab74fec3-9616-48e4-a60c-09cf963ac179.png)

### The Instrument

   1. 0.0.0.0/0 via 10.18.11.213
   2. 10.18.9.0/24 via 10.18.11.222
   3. 10.18.11.224/30 via 10.18.11.222
   4. 10.18.4.0/24 via 10.18.11.222
   5. 10.18.11.0/25 via 10.18.11.218
   6. 10.18.10.128/25 via 10.18.11.218

   ![The Instrument Routing](https://user-images.githubusercontent.com/55425460/204121682-880e9227-5398-4fd2-8628-55b58e321184.png)

### The Firefist

   1.  0.0.0.0/0 via 10.18.11.221
   2.  10.18.11.224/30 via 10.18.9.3

   ![The Firefist Routing](https://user-images.githubusercontent.com/55425460/204121694-62c73f6d-e04e-40d6-b7a3-cbe47571901e.png)

### The Queen

   1.  0.0.0.0/0 via 10.18.9.1

   ![The Queen Routing](https://user-images.githubusercontent.com/55425460/204121702-dfbaeae9-4592-47e8-aaae-9f8c18ae27f7.png)

### The Riofound

   1.  0.0.0.0/0 via 10.18.11.217

   ![The Riofound Routing](https://user-images.githubusercontent.com/55425460/204121706-aa0f1e4d-a30e-43f1-b73c-5a9aeaf6f687.png)

### The Magical

   1.  0.0.0.0/0 via 10.18.11.205

   ![The Magical Routing](https://user-images.githubusercontent.com/55425460/204121709-8b8196b9-05dd-4486-b082-d6c27db0ff9b.png)
    

## Pengetesan Routing di Cisco Packet Tracer (VLSM)

Berikut adalah tampilan percobaan melakukan `ping` dari device satu ke device lainnya
![test_ping](https://user-images.githubusercontent.com/55425460/204121756-a4ec24f1-3e38-43f3-9ecf-953ec73f4bc3.gif)


## Konfigurasi Classless Inter Domain Routing (CIDR) di GNS3

1. Membuat pembagian subnet sebagai berikut
    ![Pengelompokkan Subnet CIDR](https://user-images.githubusercontent.com/70679432/204067436-2d576e2e-00f1-44fa-b377-ea8a171ba705.jpeg)

    ![Grafik  Pengelompokkan Subnet CIDR](https://user-images.githubusercontent.com/70679432/204067458-e1e67056-b6de-4c6c-960a-84a9648bda8e.jpg)

2. Melakukan pembagian IP berdasarkan penggabungan subnet yang telah dibuat dengan membuat tree  
    ![IP_Tree_CIDR](https://user-images.githubusercontent.com/70679432/204067484-1ddcd70b-49a1-4901-8b11-424cae5bc94e.png)

3. Didapatkan hasil sebagai berikut  

    ![Hasil Akhir IP dan Netmask tiap Subnet CIDR](https://user-images.githubusercontent.com/70679432/204067523-5b55f7a6-113e-44e5-969d-bb1ff93a6b0f.jpg)

4. Melakukan konfigurasi Router di GNS 3 sebagai berikut  
    a. The Resonance

        ```  
        # NAT
        auto eth0
        iface eth0 inet dhcp

        # A17
        auto eth1
        iface eth1 inet static
                address 10.18.64.1
                netmask 255.255.255.252

        # A1
        auto eth2
        iface eth2 inet static
                address 10.18.0.1
                netmask 255.255.255.252

        # A3
        auto eth3
        iface eth3 inet static
                address 10.18.160.1
                netmask 255.255.255.252

        #A16
        auto eth4
        iface eth4 inet static
                address 10.18.224.1
                netmask 255.255.255.252
        ```
    b. The Magical 

        ```
        # A1
        auto eth0
        iface eth0 inet static
                address 10.18.0.2
                netmask 255.255.255.252
                gateway 10.18.0.1

        # A2
        auto eth1
        iface eth1 inet static
                address 10.18.32.1
                netmask 255.255.254.0

        ```
    c. The Order
        
        ```
        # A16
        auto eth0
        iface eth0 inet static
            address 10.18.224.2
            netmask 255.255.255.252
            gateway 10.18.224.1

        # A14
        auto eth1
        iface eth1 inet static
            address 10.18.208.1
            netmask 255.255.255.192

        # A15
        auto eth2
        iface eth2 inet static
            address 10.18.200.1
            netmask 255.255.255.252
        ```
    d. The Minister

        ```
        # A15
        auto eth0
        iface eth0 inet static
            address 10.18.200.2
            netmask 255.255.255.252
            gateway 10.18.200.1

        # A13
        auto eth1
        iface eth1 inet static
            address 10.18.194.1
            netmask 255.255.252.0

        # A11
        auto eth2
        iface eth2 inet static
            address 10.18.192.1
            netmask 255.255.255.252

        ```
    e. The Dauntless

        ```
        # A11
        auto eth0
        iface eth0 inet static
            address 10.18.192.2
            netmask 255.255.255.252
            gateway 10.18.192.1

        # A10
        auto eth1
        iface eth1 inet static
            address 10.18.196.1
            netmask 255.255.255.0
        ```
    f. The Instrument

        ```
        # A3
        auto eth0
        iface eth0 inet static
            address 10.18.160.2
            netmask 255.255.255.252
            gateway 10.18.160.1

        # A12
        auto eth1
        iface eth1 inet static
            address 10.18.136.1
            netmask 255.255.255.128

        # A4
        auto eth2
        iface eth2 inet static
            address 10.18.132.1
            netmask 255.255.255.252

        # A6
        auto eth3
        iface eth3 inet static
            address 10.18.152.1
            netmask 255.255.255.252
        ```
    g. The Profound

        ```
        # A4
        auto eth0
        iface eth0 inet static
            address 10.18.132.2
            netmask 255.255.255.252
            gateway 10.18.132.1

        # A5
        auto eth1
        iface eth1 inet static
            address 10.18.130.1
            netmask 255.255.255.128

        # A7
        auto eth2
        iface eth2 inet static
            address 10.18.128.1
            netmask 255.255.255.128

        ```
    h. The Firefist

        ```
        # A6
        auto eth0
        iface eth0 inet static
            address 10.18.152.2
            netmask 255.255.255.252
            gateway 10.18.152.1

        # A8
        auto eth1
        iface eth1 inet static
            address 10.18.144.1
            netmask 255.255.254.0

        # A9
        auto eth2
        iface eth2 inet static
            address 10.18.146.1
            netmask 255.255.255.0

        ```
    I. The Queen

        ```
        # A9
        auto eth0
        iface eth0 inet static
            address 10.18.146.3
            netmask 255.255.255.0
            gateway 10.18.146.1

        # A18
        auto eth1
        iface eth1 inet static
            address 10.18.148.1
            netmask 255.255.255.252
        ```
5. Melakukan konfigurasi PC di GNS 3 sebagai berikut  
    a. The Beast

        ```
        # A17
        auto eth0
        iface eth0 inet static
            address 10.18.64.2
            netmask 255.255.255.252
            gateway 10.18.64.1
        ```
    b. Corvekt (200 Host)

        ```
        auto eth0
        iface eth0 inet static
                address 10.18.32.2
                netmask 255.255.254.0
                gateway 10.18.32.1

        ```
    c. Haines (70 Host)

        ```
        auto eth0
        iface eth0 inet static
                address 10.18.32.3
                netmask 255.255.254.0
                gateway 10.18.32.1

        ```
    d. Ashaf (50 Host)
        
        ```
        # A14
        auto eth0
        iface eth0 inet static
            address 10.18.208.2
            netmask 255.255.255.192
            gateway 10.18.208.1
        ```
    e. Guideau (1000 Host)

        ```
        # A13
        auto eth0
        iface eth0 inet static
            address 10.18.194.2
            netmask 255.255.252.0
            gateway 10.18.194.1
        ```
    f. Johan (100 Host)

        ```
        # A10
        auto eth0
        iface eth0 inet static
            address 10.18.196.2
            netmask 255.255.255.0
            gateway 10.18.196.1
        ```
    g. Phanora (150 Host)

        ```
        # A10
        auto eth0
        iface eth0 inet static
            address 10.18.196.3
            netmask 255.255.255.0
            gateway 10.18.196.1
        ```
    h. Matt Cugat (120 Host)

        ```
        # A12
        auto eth0
        iface eth0 inet static
            address 10.18.136.2
            netmask 255.255.255.128
            gateway 10.18.136.1
        ```
    i.  Spendrow (120 Host)
        
        ```
        # A5
        auto eth0
        iface eth0 inet static
            address 10.18.130.2
            netmask 255.255.255.128
            gateway 10.18.130.1
        ```
    j.  Helga (70 Host)

        ```
        # A7
        auto eth0
        iface eth0 inet static
            address 10.18.128.2
            netmask 255.255.255.128
            gateway 10.18.128.1
        ```
    k. Oakleave (500 Host)

        ```
        # A7
        auto eth0
        iface eth0 inet static
            address 10.18.128.2
            netmask 255.255.255.128
            gateway 10.18.128.1
        ```
    l.  Keith (210 Host)

        ```
        # A9
        auto eth0
        iface eth0 inet static
            address 10.18.146.2
            netmask 255.255.255.0
            gateway 10.18.146.1
        ```
    m.  The Witch

        ```
        # A18
        auto eth0
        iface eth0 inet static
            address 10.18.148.2
            netmask 255.255.255.252
            gateway 10.18.148.1
        ```
6. Lakukan uncomment ```net.ipv4.ip_forward=1 pada file /etc/sysctl.conf``` di semua router  

7. Tambahkan routing pada router 
    a. The Resonance

        ```
        # A1 - A2
        route add -net 10.18.32.0 netmask 255.255.254.0 gw 10.18.0.2

        # A16 - A14
        route add -net 10.18.208.0 netmask 255.255.255.192 gw 10.18.224.2

        # A16 - A15
        route add -net 10.18.200.0 netmask 255.255.255.252 gw 10.18.224.2

        # A16 - A15 - A13
        route add -net 10.18.194.0 netmask 255.255.255.192 gw 10.18.224.2 

        # A16 - A15 - A11
        route add -net 10.18.192.0 netmask 255.255.255.252 gw 10.18.224.2

        # A16 - A15 - A11 - A10
        route add -net 10.18.196.0 netmask 255.255.255.0 gw 10.18.224.2

        # A3 - A12
        route add -net 10.18.136.0 netmask 255.255.255.128 gw 10.18.160.2

        # A3 - A4
        route add -net 10.18.132.0 netmask 255.255.255.252 gw 10.18.160.2

        # A3 - A4 - A7
        route add -net 10.18.128.0 netmask 255.255.255.252 gw 10.18.160.2

        # A3 - A4 - A5
        route add -net 10.18.130.0 netmask 255.255.255.252 gw 10.18.160.2

        # A3 - A6
        route add -net 10.18.152.0 netmask 255.255.255.252 gw 10.18.160.2

        # A3 - A6 - A8
        route add -net 10.18.144.0 netmask 255.255.254.0 gw 10.18.160.2

        # A3 - A6 - A9
        route add -net 10.18.146.0 netmask 255.255.255.0 gw 10.18.160.2

        # A3 - A6 - A18
        route add -net 10.18.148.0 netmask 255.255.255.252 gw 10.18.160.2
        ```
    b. The Order

        ```
        # A15 - A13
        route add -net 10.18.194.0 netmask 255.255.255.252 gw 10.18.200.2

        # A15 - A11
        route add -net 10.18.192.0 netmask 255.255.255.252 gw 10.18.200.2

        # A15 - A11 - A10
        route add -net 10.18.196.0 netmask 255.255.255.0 gw 10.18.200.2
        ```
    c. The Minister 
        
        ```
        # A11 - A10
        route add -net 10.18.196.0 netmask 255.255.255.0 gw 10.18.192.2

        # A15 - A16 - A1 - A2
        route add -net 10.18.32.0 netmask 255.255.254.0 gw 10.18.200.1
        ```
    d. The Instrument
        
        ```
        # A4 - A5
        route add -net 10.18.130.0 netmask 255.255.255.128 gw 10.18.132.2

        # A4 - A7
        route add -net 10.18.128.0 netmask 255.255.255.128 gw 10.18.132.2

        # A6 - A8
        route add -net 10.18.144.0 netmask 255.255.254.0 gw 10.18.152.2

        # A6 - A9
        route add -net 10.18.146.0 netmask 255.255.255.0 gw 10.18.152.2

        # A6 - A18
        route add -net 10.18.148.0 netmask 255.255.255.252 gw 10.18.152.2
        ```
    e.  The Profound

        ```
        # A4 - A3
        route add -net 10.18.160.0 netmask 255.255.255.252 gw 10.18.132.1
        ```
    f.  The Firefist
        
        ```
        # A18
        route add -net 10.18.148.0 netmask 255.255.255.252 gw 10.18.146.3
        ```
    g. The Dauntless
        ```
        # A11 - A15
        route add -net 10.18.200.0 netmask 255.255.255.252 gw 10.18.192.1
        ```
8.  Pengetesan dengan cara melakukan ping  
    a. Dari The Witch ke The Beast  
        ![Ping The Witch to The Beast](https://user-images.githubusercontent.com/70679432/204068870-2b99a146-0b4f-43d4-ae46-35842f918a7f.jpg)
    b. Dari The Dauntles ke The Profound
        ![Ping The Duntles to The Profound](https://user-images.githubusercontent.com/70679432/204096239-f410b721-75b2-4e52-a780-e9c8a20b48b4.jpg)
    c. Dari Guideau ke The Firefist
        ![Ping Guideau to The Firefist](https://user-images.githubusercontent.com/70679432/204096265-857aba59-3782-448e-a705-658b50d9708e.jpg)
    d.  Dari Corvekt ke The Minister
        ![Ping Corvekt to The Minister](https://user-images.githubusercontent.com/70679432/204096300-41b838aa-65c0-494f-866a-442fdf8a5e69.jpg)

## Kendala

1. Di Cisco Packet Tracer, saat ingin melakukan pengetesan routing dengan tombol `Simple PDU`, percobaan pertama selalu `Failed`, harus dicoba berkali-kali atau dipancing dengan command `ping` melalui command prompt
2. Kesulitan dalam melakukan konfigurasi routing pada router
3. Kesulitan dalam menentukan subnet yang terjauh dari NAT
