# Parallel_Execution_With_Docker
## What is Docker?
Answer :<br>
	Docker is tool designed to make It easier to create, deploy, and run applications by using containers.<br>
	Docker is a set of platforms as a service which use OS level virtualization to deliver application in pkgs called container.<br>
	All Container are run by an OS kernel and share the system resources that is the reason containers are lightweight then VM.<br>

**Download Docker for Window**: https://docs.docker.com/docker-for-windows/install/

**Docker Commands:**
->docker –version or docker -v <br>

	Docker run -it -d node  	=> to start container <br>
	Docker ps  	 =>it list all running container <br>
	Docker ps -a	=> it will list all running and non-running containers <br>
	Docker restart	id/name	=> it will restart the container <br>
	Docker stop id/name	=> it stop the container <br>
	Docker exec -it id(container id) bash	=>get into particular container <br>
	@root/containerId> Exit	=> to get out of container, simple type exit <br>
	Docker rm <containerid>	=> to remove image <br>
	Docker images	=> list all pulled images in the docker <br>
	Docker rm <imageid> 	=> romove image from docker <br>
	Docker pull <image name>	=> to pull image into docker <br>
	Docker start <containerId>	=> will start the container <br>
	Docker kill <container id>	=> forcefully kill the container <br>
	Docker inpect <contianer id> 	=> to inpect container <br>
	Docker image ls		=> list all images <br>

**Selenium grid setup:**
  
	Docker pull selenium/hub	=> Image for running a Grid Hub <br>
	Docker pull selenium/node-chrome-debug	=>Grid Node with Chrome installed and runs a VNC server, needs to be connected to a Grid Hub <br>
	Docker pull selenium/node-firefox-debug 		=> Grid Node with Firefox installed and runs a VNC server, needs to be connected to a Grid Hub <br>
  
**Image Command** <br>
Selenium hub	=> docker pull selenium/hub <br>
Selenium firefox node	=> docker pull selenium/node-firefox <br>
Selenium chrome node	=> docker pull selenium/node-chrome <br>
Selenium firefox debug	=> docker pull selenium/node-firefox-debug <br>
Selenium chrome debug	=> docker pull selenium/node-chrome-debug <br>

**How to Check running containers: type below command on CMD**<br>
  	docker ps -a
  
  
**To Run hub:**<br>
  
  docker run -d -p 4546:4444 --name selenium-hub selenium/hub<br>
  ![image](https://user-images.githubusercontent.com/45819133/133747093-ce054e62-6ace-4b73-9bd6-8915ad09dea4.png) <br>
Where 4546 -> customize port  <br>
	4444-> selenium default port  <br>
*Open into browser (chrome, Firefox or any browser): localhost:4546  <br>
*If localhost does not work use your system IP and port for example 172.81.24.5:4546  <br>


**Link Chrome Browser with hub:** <br>
docker run -d -P --link selenium-hub:hub selenium/node-chrome-debug
 ![image](https://user-images.githubusercontent.com/45819133/133747604-e00254cb-03b5-4a61-b08f-1487304cd26e.png) <br>

**Link Firefox browser with hub:** <br>
docker run -d -P --link selenium-hub:hub selenium/node-firefox-debug <br>
![image](https://user-images.githubusercontent.com/45819133/133747704-d6ca6d3a-a90c-4614-90ea-ff23acbcca07.png) <br>

**URL to download TighVNC **: https://www.tightvnc.com/ <br>
How to View browser running virtually <br>
Step 1: Install TightVNC  <br>
Step 2: get running Chrome or Firefox port number. <br>
Note: How to get port number <br>
 Type “docker ps -a”  in cmd – you will all running port in the container <br>
 ![image](https://user-images.githubusercontent.com/45819133/133747816-9feccd6a-7f3b-4a04-8090-938c2fdaaff8.png) <br>

Step 3: TightVNC UI and which IP and port need to use here.<br>
 ![image](https://user-images.githubusercontent.com/45819133/133747862-39330faa-0541-450a-8bc0-02679286ce8b.png) <br>

Ip should be current system IP address. So, to get IP for the system <br>
	Type ipconfig in the CMD and pick IP address. <br>
 ![image](https://user-images.githubusercontent.com/45819133/133747934-ddf9519c-ea81-4274-b7f7-d2ca4a18ec2d.png) <br>

Step 4: So, combine system IP and chrome or Firefox port from step 2 and put into TightVNC
 ![image](https://user-images.githubusercontent.com/45819133/133747977-14bbf601-ccdf-4c7b-b66e-ef71132cd2ca.png) <br>

Step 5: after click on Connect, you will get below UI, so in the password section please use default password.
Default password: secret
	![image](https://user-images.githubusercontent.com/45819133/133748006-55ed3758-52fe-438b-a3f8-7ee6577bba86.png) <br>

 

