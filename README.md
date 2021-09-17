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

