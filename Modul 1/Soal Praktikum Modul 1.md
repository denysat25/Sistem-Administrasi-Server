# Laporan Soal Praktikum Modul 1

1. Bryan pratma Putra (1202190037)
2. Deny Satria Ardi (1202190026)


### Objectives

### Daftar Isi
[1. Rename Ubuntu_php5.6 Menjadi Ubuntu_landing](https://github.com/bryanpratama/Sistem-Administrasi-Server/new/main/Modul%201#1-rename-ubuntu_php56-menjadi-ubuntu_landing)<br>
[2. Install LXC debian 9 dengan nama debian_php5.6](https://github.com/bryanpratama/Sistem-Administrasi-Server/new/main/Modul%201#2-install-lxc-debian-9-dengan-nama-debian_php56)<br>
[3. Setup nginx pada dabian_php5.6](https://github.com/bryanpratama/Sistem-Administrasi-Server/new/main/Modul%201#3-setup-nginx-pada-dabian_php56)<br>
[4. Setup nginx pada ubuntu_landing](https://github.com/bryanpratama/Sistem-Administrasi-Server/new/main/Modul%201#4-setup-nginx-pada-ubuntu_landing)<br>
[5. Auto start pada LXC ubuntu_landing](https://github.com/bryanpratama/Sistem-Administrasi-Server/new/main/Modul%201#5-auto-start-pada-lxc-ubuntu_landing)<br>
[6. Setup nginx pada vm.local mengatur proxy_pass](https://github.com/bryanpratama/Sistem-Administrasi-Server/new/main/Modul%201#6-setup-nginx-pada-vmlocal-mengatur-proxy_pass)<br>
[7. Tampilan pada browser](https://github.com/bryanpratama/Sistem-Administrasi-Server/new/main/Modul%201#7-tampilan-pada-browser)<br>
[8. Analisa](https://github.com/bryanpratama/Sistem-Administrasi-Server/new/main/Modul%201#8-analisa)<br>

#### 1. Rename Ubuntu_php5.6 menjadi Ubuntu_landing
ubah nama

![rename](Assets/rename.png)

ubah ip ke 103

![ubah ip](Assets/ip-address-sesudah.png)

jika mengalami double ip bisa melakukan reboot

![eror double ip](Assets/error-double-ip.png)

ubah ip ubuntu_php7.4 ke 101

![ubah ip php_7.4](Assets/ubah-ip-php7.4%20ke-101.png)

sudo netplan apply

![confirm ip php_7.4](Assets/periksa-ip-sudah-berubah-ke-101.png)

#### 2. Install LXC debian 9 dengan nama debian_php5.6

membuat debian_php5.6

![add debian_php5.6](Assets/membuat-debian-5.6.png)

mengecek debian_php5.6

![create debian_php5.6 done](Assets/debian5.6-berhasil-dibuat.png)

#### 3. Setup nginx pada dabian_php5.6

start debian_php5.6 dan install nginx

![start debian + install nginx](Assets/run-debian5.6-dan-install-nginx.png)

install nano, net-tools, dan curl

![install nano net tools dan curl](Assets/install-net-tools-curl-di-debian.png)

setting ip jadi 102

![change ip to 102](Assets/ubah-isi-dari-network-interface-debian.png)

melakukan restart 

![restart network service](Assets/mengecek-perubahan-ip-debian-dengan-menggunakan-ifconfig.png)

jika ip tidak berubah silakam melakukan reboot

![reboot to change ip to 102](Assets/ip-debian-berhasil-di-ubah-menjadi-10.0.3.102%20.png)

setting nginx

![setting nginx](Assets/add-lxc_php5.6-ke-debian.png)

mengiisi lxc_php5.6

![add server name + index](Assets/mengisi-lxc_php5.6.png)

butuh pembaruan

![](Assets/copy-lxc5.6-ke-enabled.png)

![add lxc_php5.6 to hosts](Assets/menambahkan-lxc_php5.6-ke-hosts.png)

![copy index to lxc_php5_6 index](Assets/mebuat-direktori-lxc_php5.6.png)

![test curl ](Assets/menampilkan-isi-debian-lxc_php5.6-dengan-curl.png)

#### 4. Setup nginx pada ubuntu_landing

butuh pembaruan ke index lxc_landing

![change server name to lxc_landing](Assets/mengubah-server-name-yang-sebelumnya-lxc_php5.6-ke-lxc_landing.png)

![add lxc_ladning to sites enabled](Assets/mebuat-lxc_landing-di-sites-enable-ubuntu-landing.png)

![add lxc_landing to hosts](Assets/menambahkan-ip-lxc_landing.png)

![masuk ke lxc_lading index](Assets/masuk-ke-index-pada-lxc-landing.png)

![melihat isi lxc_landing index](Assets/melihat-isi-dari-lxc-landing-index.png)

melakukan test dengan curl ke lxc_landing.dev

![](Assets/)

#### 5. Auto start pada LXC ubuntu_landing

sebelum melakukan auto start stop terlebih dahulu ubuntu landing

![stop ubuntu landing](Assets/stop-ubuntu-landing.png)

masuk ke ubuntu landing config

![masuk ke ubuntu landing config](Assets/masuk-ke-ubuntul-landing-config.png)

![nano config](Assets/masuk-e-config-ubuntul-landing2.png)

menambahkan config dengan lxc.start.auto = 1

![add auto start](Assets/menambahkan-auto-start-pada-ubuntu-landing.png)

maka auto start = 1

![reboot for check auto start = 1](Assets/ubuntu-landing-auto.png)

#### 6. Setup nginx pada vm.local mengatur proxy_pass

masuk ke hosts vm.local

![change to 101 102 103](Assets/merubah-hosts-ke-101-102-103.png)

masuk ke vm.local

![nano vm local](Assets/masuk-ke-vm.local.png)

butuh perbaikan

![merubah isi vm local](Assets/merubah-isi-vm.local.png)

#### 7. Tampilan pada browser

curl didalam

![ip 101](Assets/curl-in-7.4.png)

![ip 102](Assets/curl-in-debian5.6.png)

![ip 103](Assets/curl-in-landing.png)

curl dari home

![home curl 101](Assets/curl-home-in-7.4.png)

![home curl 102](Assets/curl-home-in-debian5.6.png)

![home curl 103](Assets/curl-home-in-landing.png)

dari browser

![browser 101](Assets/tampilan-lxc_7.4-browser.png)

![browser 102](Assets/tampilan-debian_5.6-browser.png)

![browser 103](Assets/tampilan-lxc_landing-browser.png)

#### 8. Analisa
   - Mengapa untuk kebutuhan php5.6 tidak bisa menggunakan ubuntu 16.04, sehingga perlu diganti os ke debian 9?
   - Kenapa harus menggunakan virtualisasi LXC pada skema website yang akan didevelop?
   - Apa yang dimaksud dengan proxy server? kenapa vm.local bisa kita anggap sebagai proxy server?
