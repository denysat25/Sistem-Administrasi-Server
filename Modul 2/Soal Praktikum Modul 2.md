# Laporan Praktikum Modul 2

1. Bryan pratma Putra (1202190037)
2. Deny Satria Ardi (1202190026)

------

## 1. Rubah LXC landing dengan ubuntu focal (destroy n create, same ip, same name)

cek-lxc
``` 
lxc-ls -f
```

![](Assets/1/cek-lxc.png)

Menganti ubuntu landing, dan buat ubuntu vocal baru
``` 
lxc-destroy ubuntu_landing
```

![](Assets/1/destroy-ubuntu-landing.png)

Create-ubuntu-landing

![](Assets/1/create-ubuntu-landing.png)

Install nano

![](Assets/1/apt-install-nano.png)

Atur IP ubuntu_landing

![](Assets/1/edit-lxc-yaml.png)

melihat perubahan dengan menggunakan ```ip r```

![](Assets/1/ip-r.png)

Buat ubuntu_landing jadi auto start dengan ```lxc.start.auto = 1``` pada config

![](Assets/1/auto-start-ubuntu-landing.png)

install-ssh-server

![](Assets/1/install-ssh-server.png)

masuk ke ```/etc/ssh/sshd_config``` dan tambahkan code dibawah ini :

```
PermitRootLogin yes
RSAAuthentication yes
```

dan lakukan ```service sshd restart```

![](Assets/1/sshd-config.png)

mengatur sandi baru dengan ```passwd``` dan cek ssh 

![](Assets/1/set-new-pass-dan-cek-ssh.png)

![](Assets/1/.png)

![](Assets/1/.png)

## 2. Rubah LXC php7 dengan ubuntu focal (destroy n create, same ip, same name)

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

## 3. vm.local/
## 4. vm.local/blog
