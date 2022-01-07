# Laporan Praktikum Modul 4

1. Bryan pratma Putra (1202190037)
2. Deny Satria Ardi (1202190026)

------
For each container, make 2 copies

![](bahan/001.png)

Start each containers

![](bahan/002.png)

Go to ubuntu_php7.4_2 , then change the IP address to 10.0.3.111

![](bahan/003.png)

Go to etc/hosts to register lxc_php7_2.dev

![](bahan/004.png)

Change the server name

![](bahan/005.png)

Restart nginx then curl it. Repeat with same steps on the ubuntu_php7.4_3

![](bahan/006.png)


Same as on ubuntu_php7.4, start all container

![](bahan/007.png)
![](bahan/008.png)

Go to 'debian_php5.6_2' and change the IP address to 10.0.3.112

![](bahan/009.png)

Register lxc_php5_2.dev at /etc/hosts

![](bahan/010.png)

Change the server name, then repeat with same steps on the debian_php5.6_3. After that restart the container

![](bahan/011.png)

![](bahan/012.png)

Register all the contaiers in /etc/hosts

![](bahan/013.png)

Run the jmeter. Change the number from 50, 100, 150 :

50

![](bahan/014.png)

![](bahan/015.png)

![](bahan/016.png)

![](bahan/017.png)

100

![](bahan/017a.png)

![](bahan/018.png)

![](bahan/019.png)

![](bahan/020.png)

150

![](bahan/021.png)

![](bahan/022.png)

![](bahan/023.png)

![](bahan/024.png)

Turn back to VM and go to

```
/etc/nginx/sites-available/vm.local
```

Add upstream landing, php5, and php7

![](bahan/025.png)

Change the proxy_pass

![](bahan/026.png)

Then, return to the jmeter and redo

50

![](bahan/026a.png)

![](bahan/027.png)

![](bahan/028.png)

![](bahan/029.png)

100

![](bahan/030.png)

![](bahan/031.png)

![](bahan/032.png)

![](bahan/033.png)

150

![](bahan/034.png)

![](bahan/035.png)

![](bahan/036.png)

![](bahan/037.png)


### Analysis

Overall, it may be said if we use load balancer, then the time is faster and the amount of users that accessing our web is much more then when we don't use load balancer
