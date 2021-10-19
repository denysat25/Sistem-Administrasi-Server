# Laporan Soal Latihan Praktikum Modul 1

1. Bryan pratma Putra (1202190037)
2. Deny Satria Ardi (1202190026)

## SAS Modul 1

### Objectives

### Daftar Isi

### 1. Konfigurasi VM

1.1 Memastikan network VM sudah diset ke Bridged Adapter

1.2 Start VM

1.3 Check network ubuntu server
```
ip a

system-resolve --status | grep Current

ip r
```
1.4 Setup static IP ubuntu server
```
sudo nano /etc/netplan/00-installer-config.yaml
```
```
sudo netplan apply
ifconfig
```
```
ping 1.1.1.1
ping google.com
```

### 2. Membuat LXC
2.1 Membuat 2 LXC dengan nama ubuntu_php5.6 (dengan ubuntu 16.04 ```xenia```) dan ubuntu_7.4 (dengan ubuntu 18.04```bionic```) 
```
sudo lxc-create -n ubuntu_php5.6 -t download -- --dist ubuntu --release xenial --arch amd64 --force-cache --no-validate --server images.linuxcontainers.org

sudo lxc-create -n ubuntu_php7.4 -t download -- --dist ubuntu --release bionic --arch amd64 --force-cache --no-validate --server images.linuxcontainers.org
```
2.2 Install nginx dan nginx-extras
- pada LXC ubuntu_php5.6
```
sudo lxc-start -n ubuntu_php5.6
sudo lxc-attach -n ubuntu_php5.6
sudo apt install nginx nginx-extras
exit
```

### 3. Ubuntu_php5.6

### 4. Ubuntu_php7.4

### 5. VM

### 6. Konfigurasi laptop/pc
