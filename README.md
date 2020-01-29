# Install ***Metatron Discovery*** by docker Guide
### <p align="right">***Written by : Minwoo Baek***</p>

![enter image description here](https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/discovery-web-logo.png)

- ***Metatron Discovery*** Link : [https://metatron.app](https://metatron.app/)
- ***Metatron Discovery*** Github : [https://github.com/metatron-app/metatron-discovery](https://github.com/metatron-app/metatron-discovery/)

## Overview
***Metatron discovery*** is an end-to-end data discovery solution that supports quick and easy analysis process even with a tremendous amount of data. This Guide is for who using Windows10 64bit OS. 

----

## 1. Install Dockerhub
![https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/1_dockerhub_main.PNG](https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/1_dockerhub_main.PNG)

- Dockerhub Link : [https://hub.docker.com](https://hub.docker.com/)

1. Enter to Dockerhub main homepage
2. Press button of Get started with Docker Desktop
---

## 2. Follow the process of installing Dockerhub
![https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/2_download_docker_desktop.PNG](https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/2_download_docker_desktop.PNG)

1. Press button of Download Docker Desktop for Windows

![https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/3_install_docker.PNG](https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/3_install_docker.PNG)

2. Install Docker Desktop package
---

## 3. Setting Docker Limit
![https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/4_setting_docker_cpu_memory.PNG](https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/4_setting_docker_cpu_memory.PNG)

- ***Metatron Discovery*** needs enough CPU cores and Memory space.
- Minimum setting
	- CPU : 2
	- Memory : 9000MB
---

## 4. Install ***Metatron Discovery***
![https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/5_open_metatron_discovery_install_guide.PNG](https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/5_open_metatron_discovery_install_guide.PNG)

1. Open ***Metatron Discovery*** install guide : [https://metatron.app/download/installation-guide-docker/](https://metatron.app/download/installation-guide-docker/)

![https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/6_checking_latest_version.PNG](https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/6_checking_latest_version.PNG)

2.  Enter to ***Metatron Discovery*** Docker repository page and checking latest version

![https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/7_download_metatron_image.PNG](https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/7_download_metatron_image.PNG)

3. Download ***Metatron Discovery*** in your Docker

![https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/8_making_container_metatron.PNG](https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/8_making_container_metatron.PNG)
 

    docker run -i -d --rm -m 11G  -p ${HOST_DISCOVERY_PORT:=8180}:8180 --name metatron-discovery metatronapp/discovery:latest

4. Open Command screen and input this code.
	- 11G : Docker memory 
	- ${HOST_DISCOVERY_PORT:=8180} : External Port 
		- If you want to use remote, you need set firewall. 
		- In this example, your ***Metatron Discovery*** will use 8180 port.
		- So, After start ***Metatron Discovery*** container, [http://localhost:8180](http://localhost:8180) is the address of ***Metatron Discovery*** .
---
## 5. Checking container and Start ***Metatron Discovery***
![https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/9_checking_container_status.PNG](https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/9_checking_container_status.PNG)

1. Checking Docker container : If Docker run ***Metatron Discovery***  image well, you will see the result as shown.

![https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/10_metatron_start.png](https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/10_metatron_start.png)

2. Start ***Metatron Discovery*** container 

    docker start metatron-discovery
---

## 6. ***Metatron Discovery*** Login

![https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/11_metatron_login.png](https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/11_metatron_login.png)

1. [http://localhost:8180](http:/localhost:8180) 
2. Initial ID : admin / Initial Password : admin
---

## 7. Sample Image
![https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/12_metatron_sample.png](https://raw.githubusercontent.com/rasnim/Install-metatron-discovery-by-docker/master/img/12_metatron_sample.png)

Link : [https://metatron-app.github.io/metatron-doc-discovery/en/](https://metatron-app.github.io/metatron-doc-discovery/en/)

---
### Now you can use ***Metatron Discovery***

