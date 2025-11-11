# Tugas-1-Jarkom_Clarissa-Aydin_014

# Topologi

### Merancang topologinya menggunakan Cisco Packet Tracer

<img width="1611" height="790" alt="image" src="https://github.com/user-attachments/assets/bd432ec2-f5a8-4338-88a8-de9f11482242" />

# Base Network dan Subnetting

### Base Network Unik

```
NRP 5027241014 mod 256 = 54
Base = 10.54.0.0
```

### Subnetting
```
IP Prefix: 10.54.0.0/22
Total Host: 778 host
```

| **Nama Subnet**                    | **Host** | **Host + Gateway** | **Netmask** |
|-----------------------------------|---------:|--------------------:|:-----------:|
| Sekretariat                       |     380 |                381  | /23         |
| Bidang Kurikulum                  |     220 |                221  | /24         |
| Bidang Guru & Tendik              |      95 |                 96  | /25         |
| Bidang Sarana Prasarana           |      45 |                 46  | /26         |
| Bidang Pengawas Sekolah           |      18 |                 19  | /27         |
| Server & Admin                    |       6 |                  7  | /28         |
| Jaringan Gabungan                 |       6 |                  6  | /29         |
| Tunnel (Link Pusat dan Cabang)    |       2 |                  2  | /30         |
| TOTAL                             |         |              **778**| **/22**     |




# VLSM


## Topologi VLSM

<img width="1425" height="742" alt="image" src="https://github.com/user-attachments/assets/1eb36bc5-dd37-4356-a7bc-cebc9f93d6f7" />

## Pohon VLSM

<img width="795" height="923" alt="image" src="https://github.com/user-attachments/assets/bf331d9c-2b45-4919-a310-c7c7a1e947a1" />


## Perhitungan Subnetting VLSM 

| **Nama Subnet**                    | **Kebutuhan Host** | **Network Address** | **Prefix** | **Subnet Mask**     | **Host Range**                 | **Broadcast Address** | **Gateway Address** |
|-----------------------------------|--------------------|----------------------|------------|----------------------|-------------------------------|------------------------|----------------------|
| Sekretariat                       | 381                | 10.54.2.0            | /23        | 255.255.254.0        | 10.54.2.1 - 10.54.3.254       | 10.54.3.255            | 10.54.2.1            |
| Bidang Kurikulum                  | 221                | 10.54.1.0            | /24        | 255.255.255.0        | 10.54.1.1 - 10.54.1.254       | 10.54.1.255            | 10.54.1.1            |
| Bidang Guru & Tendik              | 96                 | 10.54.0.128          | /25        | 255.255.255.128      | 10.54.0.129 - 10.54.0.254     | 10.54.0.255            | 10.54.0.129          |
| Bidang Sarana Prasarana           | 46                 | 10.54.0.64           | /26        | 255.255.255.192      | 10.54.0.65 - 10.54.0.126      | 10.54.0.127            | 10.54.0.65           |
| Bidang Pengawas Sekolah (Caba)    | 19                 | 10.54.0.32           | /27        | 255.255.255.224      | 10.54.0.33 - 10.54.0.62       | 10.54.0.63             | 10.54.0.33           |
| Server & Admin                    | 7                  | 10.54.0.16           | /28        | 255.255.255.240      | 10.54.0.17 - 10.54.0.30       | 10.54.0.31             | 10.54.0.17           |
| Jaringan Gabungan                 | 6                  | 10.54.0.8            | /29        | 255.255.255.248      | 10.54.0.9 - 10.54.0.14        | 10.54.0.15             | 10.54.0.9            |
| Tunnel (Link Pusat dan Cabang)                          | 2                  | 10.54.0.0            | /30        | 255.255.255.252      | 10.54.0.1 - 10.54.0.2         | 10.54.0.3              | 10.54.0.1            |

---

# CIDR


## Topologi CIDR

<img width="1290" height="700" alt="image" src="https://github.com/user-attachments/assets/a758e509-75a7-456f-8ace-3b1b100fe460" />

## Pohon CIDR

<img width="954" height="529" alt="image" src="https://github.com/user-attachments/assets/381f5398-5d5e-4b72-a5dc-12c0c1627103" />

## Perhitungan Subnetting CIDR

| **Subnet** | **Prefix (CIDR)** | **Description**                       | **Network Address** | **Subnet Mask**     | **Usable Host Range**         | **Broadcast Address** | **Suggested Gateway** |
|------------|-------------------|----------------------------------------|----------------------|---------------------|-------------------------------|------------------------|------------------------|
| A1         | /25               | Bidang Guru dan Tendik                | 10.54.3.0            | 255.255.255.128     | 10.54.3.1 - 10.54.3.126       | 10.54.3.127            | 10.54.3.1              |
| A2         | /24               | Bidang Kurikulum                      | 10.54.2.0            | 255.255.255.0       | 10.54.2.1 - 10.54.2.254       | 10.54.2.255            | 10.54.2.1              |
| A3         | /26               | Bidang Sarana Prasarana               | 10.54.3.128          | 255.255.255.192     | 10.54.3.129 - 10.54.3.190     | 10.54.3.191            | 10.54.3.129            |
| A4         | /28               | Server dan Admin                      | 10.54.3.192          | 255.255.255.240     | 10.54.3.193 - 10.54.3.206     | 10.54.3.207            | 10.54.3.193            |
| A5         | /23               | Sekretariat                           | 10.54.0.0            | 255.255.254.0       | 10.54.0.1 - 10.54.1.254       | 10.54.1.255            | 10.54.0.1              |
| A6         | /29               | Jaringan Gabungan / Backbone          | 10.54.3.208          | 255.255.255.248     | 10.54.3.209 - 10.54.3.214     | 10.54.3.215            | 10.54.3.209            |
| A7         | /27               | Bidang Pengawas Sekolah (Cabang)      | 10.54.4.0            | 255.255.255.224     | 10.54.4.1 - 10.54.4.30        | 10.54.4.31             | 10.54.4.1              |
| A8         | /30               | Tunnel (Link Pusat dan Cabang)        | 10.54.4.32           | 255.255.255.252     | 10.54.4.33 - 10.54.4.34       | 10.54.4.35             | 10.54.4.33             |

