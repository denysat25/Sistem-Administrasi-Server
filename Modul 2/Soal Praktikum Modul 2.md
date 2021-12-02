# Laporan Soal Praktikum Modul 2

1. Bryan pratma Putra (1202190037)
2. Deny Satria Ardi (1202190026)

------

cek-lxc

![](Assets/1/cek-lxc.png)

destroy-ubuntu-landing

![](Assets/1/destroy-ubuntu-landing.png)

create-ubuntu-landing

![](Assets/1/create-ubuntu-landing.png)

apt-install-nano

![](Assets/1/apt-install-nano.png)

edit-lxc-yaml

![](Assets/1/edit-lxc-yaml.png)

ip-r

![](Assets/1/ip-r.png)

auto-start-ubuntu-landing

![](Assets/1/auto-start-ubuntu-landing.png)

install-ssh-server

![](Assets/1/install-ssh-server.png)

sshd-config

![](Assets/1/sshd-config.png)

set-new-pass-dan-cek-ssh

![](Assets/1/set-new-pass-dan-cek-ssh.png)

![](Assets/1/.png)

![](Assets/1/.png)

2. 

Cek lxc dengan menggunakan 

```markdown
    lxc-ls -f
```
Hapus ubuntu_php7.4 dan buat ubuntu_php7.4 baru seperti pada gambar dibawah ini.

![](Assets/No%202/002.png)

Setelah itu start dan jalankan ubuntu_7.4, lalu install tools curl.

![](Assets/No%202/003.png)

Atur IP ubuntu_php7.4, dengan menggunakan

```markdown
    nano /etc/netplan/10-lxc.yaml
    netplan apply
```
![](Assets/No%202/004.png)

![](Assets/No%202/005.png)

Atur autostart pada ubuntu_php7.4

![](Assets/No%202/005a%20set%20autostaart.png)

Install ssh

![](Assets/No%202/006.png)

Atur sshd-config

![](Assets/No%202/008.png)

Atur password baru

![](Assets/No%202/009.png)

Cek ssh apakah sudah berjalan atau belum

![](Assets/No%202/010.png)

coming soon...
