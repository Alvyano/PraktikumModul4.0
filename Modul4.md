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

 Below is the results from when we use load balancer and not using the load balancer

 * When there is 50 users that access our web, if we don't use load balancer the average time of user accessing our web is
   - landing : 1115 ms / 1.1 s
   - blog : 1555 ms / 1.5 s
   - app : 4 ms / 0.004 s
- When we use load balancer, then
   - landing : 37 ms / 0.037 s
   - blog : 27 ms / 0.027 s
   - app : 21 ms / 0.021 s

Here we can know that the average time of user accessing our web is faster then if we don't use load balancer. For the throughput or the amount of user accessing our web is
- When there is 50 users that access our web, if we don't use load balancer the amount of user accessing our web is

  - landing : 36 user / second
  - blog :  20 user / second
  - app : 41 user / second

- When we use load balancer, then

  - landing : 427 user / second
  - blog :  439 user / second
  - app : 446 user / second

The conclusion is, if we use load balancer, then the time is faster and the amount of users that accessing our web is much more then when we don't use load balancer.

*SUWUN* 
