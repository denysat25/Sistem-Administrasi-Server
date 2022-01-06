# Laporan Praktikum Modul 4

1. Bryan pratma Putra (1202190037)
2. Deny Satria Ardi (1202190026)

------
For each container, make 2 copies

![01_1_lxc](assets/01_1_lxc.PNG)

Start each containers

![01_2_lxc_start](assets/01_2_lxc_start.PNG)

Go to ubuntu_php7.4_2 , then change the IP address to 10.0.3.111

![01_3_netplan_php742](assets/01_3_netplan_php742.PNG)

Go to etc/hosts to register lxc_php7_2.dev

![01_4_php742_etchosts](assets/01_4_php742_etchosts.PNG)

Change the server name

![01_5_php742_sitesavailable](assets/01_5_php742_sitesavailable.PNG)

Restart nginx then curl it. Repeat with same steps on the ubuntu_php7.4_3

![01_6_php742_curl](assets/01_6_php742_curl.PNG)

Same as on ubuntu_php7.4, start all container

![01_7_debian_start](assets/01_7_debian_start.PNG)

Go to 'debian_php5.6_2' and change the IP address to 10.0.3.112

![01_8_debian_etcnetworkinterfaces](assets/01_8_debian_etcnetworkinterfaces.PNG)

Register lxc_php5_2.dev at /etc/hosts

![01_9_debian_etchosts](assets/01_9_debian_etchosts.PNG)

Change the server name, then repeat with same steps on the debian_php5.6_3. After that restart the container

![01_10_debian_sitesavailable](assets/01_10_debian_sitesavailable.PNG)

Register all the contaiers in /etc/hosts

![01_11_vm_etchosts](assets/01_11_vm_etchosts.PNG)

Run the jmeter. Change the number from 50, 100, 150

![02_1_jmeter_50](assets/02_1_jmeter_50.PNG)

![02_2_jmeter_graph_results](assets/02_2_jmeter_graph_results.PNG)

![02_3_jmeter_viewtable_1](assets/02_3_jmeter_viewtable_1.PNG)

![02_4_jmeter_viewtable_2](assets/02_4_jmeter_viewtable_2.PNG)

![02_5_jmeter_sumreport](assets/02_5_jmeter_sumreport.PNG)

![02_6_jmeter_100](assets/02_6_jmeter_100.PNG)

![02_7_jmeter_100_graph_results](assets/02_7_jmeter_100_graph_results.PNG)

![02_8_jmeter_100_viewtable_1](assets/02_8_jmeter_100_viewtable_1.PNG)

![02_9_jmeter_100_viewtable_2](assets/02_9_jmeter_100_viewtable_2.PNG)

![02_10_jmeter_100_sumreport](assets/02_10_jmeter_100_sumreport.PNG)

![02_11_jmeter_150](assets/02_11_jmeter_150.PNG)

![02_12_jmeter_150_graph_results](assets/02_12_jmeter_150_graph_results.PNG)

![02_13_jmeter_150_viewtable_1](assets/02_13_jmeter_150_viewtable_1.PNG)

![02_14_jmeter_150_viewtable_2](assets/02_14_jmeter_150_viewtable_2.PNG)

![02_15_jmeter_150_sumreport](assets/02_15_jmeter_150_sumreport.PNG)

Turn back to VM and go to

```
/etc/nginx/sites-available/vm.local
```

Add upstream landing, php5, and php7

![03_1_sitesavailable_vm](assets/03_1_sitesavailable_vm.PNG)

Change the proxy_pass

![03_2_sitesavailable_vm](assets/03_2_sitesavailable_vm.PNG)

Then, return to the jmeter and redo

![04_1_jmeter_50](assets/04_1_jmeter_50.PNG)

![04_2_jmeter_50_graph_results](assets/04_2_jmeter_50_graph_results.PNG)

![04_3_jmeter_50_viewtable_1](assets/04_3_jmeter_50_viewtable_1.PNG)

![04_4_jmeter_50_viewtable_2](assets/04_4_jmeter_50_viewtable_2.PNG)

![04_5_jmeter_50_sumreport](assets/04_5_jmeter_50_sumreport.PNG)

![04_6_jmeter_100](assets/04_6_jmeter_100.PNG)

![04_7_jmeter_100_graph_results](assets/04_7_jmeter_100_graph_results.PNG)

![04_8_jmeter_100_viewtable_1](assets/04_8_jmeter_100_viewtable_1.PNG)

![04_9_jmeter_100_viewtable_2](assets/04_9_jmeter_100_viewtable_2.PNG)

![04_10_jmeter_100_sumreport](assets/04_10_jmeter_100_sumreport.PNG)

![04_11_jmeter_150](assets/04_11_jmeter_150.PNG)

![04_12_jmeter_150_graph_results](assets/04_12_jmeter_150_graph_results.PNG)

![04_13_jmeter_150_viewtable_1](assets/04_13_jmeter_150_viewtable_1.PNG)

![04_14_jmeter_150_viewtable_2](assets/04_14_jmeter_150_viewtable_2.PNG)

![04_15_jmeter_150_sumreport](assets/04_15_jmeter_150_sumreport.PNG)

Analysis

Below is the results from when we use load balancer and not using the load balancer

 - When there is 50 users that access our web, if we don't use load balancer the average time of user accessing our web is
   - landing : 2444 ms / 2.4 s
   - blog : 2347 ms / 2.3 s
   - app : 19 ms / 0.019 s
- When we use load balancer, then
  - landing : 1841 ms / 1.8 s
   - blog : 1379 ms / 1.3 s
   - app : 12 ms / 0.012 

Here we can know that the average time of user accessing our web is faster then if we don't use load balancer. For the throughput or the amount of user accessing our web is

- When there is 50 users that access our web, if we don't use load balancer the amount of user accessing our web is

  - landing : 16 user / second
  - blog :  12 user / second
  - app : 22 user / second

- When we use load balancer, then

  - landing : 42 user / second
  - blog :  29 user / second
  - app : 30 user / second

  Here we can know that the average time of amount of user accessing our web in 1 second is faster then if we don't use load balancer.

  

  The conclusion is, if we use load balancer, then the time is faster and the amount of users that accessing our web is much more then when we don't use load balancer.

  
