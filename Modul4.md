# **Modul 4 Practicum Report**

### By : Alvyano Rizqilla & Difa Taufiqurahman

----

- First, make 2 copies of containers, and then start

![](Modul4/1.PNG)

![](Modul4/2.PNG)

- Next, open ubuntu_php7.4_2 and change the IP address to 10.0.3.111/24. Do the same thing on ubuntu_php7.4_3, change the IP address to 10.0.3.121

![](Modul4/3.PNG)

* Go to lxc_php7_2.dev and change the server name

![](Modul4/4.PNG)

![](Modul4/5.PNG)

* Restart nginx and curl it. 

![](Modul4/6.PNG)


* Next step is ubuntu_php7.4_3 (IP 10.0.3.121), debian_php5.6_2 (IP 10.0.3.112), debian_php5.6_3 (IP 10.0.3.122) the same as ubuntu_php7.4_2. (And  add name server /etc/hosts (on VM))

![](Modul4/7.PNG)

* Run the jmeter, and change the number of threads

![](Modul4/8.PNG)

![](Modul4/9.jpeg)

![](Modul4/10.jpeg)

![](Modul4/11.jpeg)

![](Modul4/12.PNG)

![](Modul4/13.PNG)

![](Modul4/14.PNG)

![](Modul4/15.PNG)

![](Modul4/16.PNG)

![](Modul4/17.PNG)

![](Modul4/18.PNG)

![](Modul4/19.PNG)


* Go back to the VM and write the script as below to add upstream landing, php5,and php7


```markdown
/etc/nginx/sites-available/vm.local
```
![](Modul4/20.PNG)

* Change the proxy_pass

![](Modul4/21.PNG)

* Then we go back to the jmeter

```
50
```
![](Modul4/22.PNG)

![](Modul4/23.PNG)

![](Modul4/24.PNG)

![](Modul4/25.PNG)

```
100
```

![](Modul4/26.PNG)

![](Modul4/27.PNG)

![](Modul4/28.PNG)

![](Modul4/29.PNG)

```
150
```

![](Modul4/30.PNG)

![](Modul4/31.PNG)

![](Modul4/32.PNG)

![](Modul4/33.PNG)

----
### Analysis

Below are the results when using a load balancer and not using a load balancer

* when there are 150 users accessing our web, if we don't use a load balancer then the average time users access our web is

landing: 1273 ms = 1.27 s

blog : 15740 ms = 15.74 s

application : 2 ms = 0.002 sec

* when we use load balancer, then

landing : 1261 ms = 1.26 s

blog : 7489 ms = 7.49 s

application : 2 ms = 0.002 sec

Here we can find out that the average time users access our web is faster using a load balancer than when using a load balancer. For throughput or the number of users accessing our web, namely:

* When there are 150 users accessing our web, if we don't use a load balancer, the number of users accessing our web is

landing: 58 users/sec

blog : 8 users / sec

app: 16 users/sec

* when using a load balancer, then

landing: 66 users/sec

blog : 14 users/sec

app: 34 users/sec

Here we can see that by not using a web load balancer can access more users in 1 second

In conclusion, if we use a load balancer, the time required is faster and the number of users accessing our web is more than if we don't use a load balancer.

*SUWUN* 
