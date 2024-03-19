# Docker Crach Course 
Docker is a container management tool, that makes it easy to run applications on any computer in an isolated container, that includes everything it needs to run predictably.

![Arquitetura Docker](https://github.com/omar-gamel/docker-crash-course/blob/master/ArquiteturaDocker.png)

<h3>Containers vs VMs</h3>
<ul>
   <li>Virtual Machines :</li>
   Has ite's own full operating system & typically slower
   <li>Containers :</li>
   Share the host's operating system & typically quicker
</ul> 

#

<h3>Intalling Docker</h3>
<ul>
   <li>Install WSL : https://docs.microsoft.com/en-us/windows/wsl/install-win10</li> 
   <li>Manual installation steps for older versions of WSL: https://learn.microsoft.com/en-us/windows/wsl/install-manual</li> 
       1- Enable the Windows Subsystem for Linux :<br>
	<pre> $ dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart</pre>
       2- Check requirements for running WSL 2 : To update to WSL 2, you must be running Windows 10...<br>
       3- Enable Virtual Machine feature :
	  <pre>$ dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart</pre>
       4- Download the Linux kernel update package :
	  <pre>$ https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi</pre> 
       5- Download the Linux kernel update package :
          <pre>$ wsl --set-default-version 2</pre>
       6- Install your Linux distribution of choice : Open the Microsoft Store and select your favorite Linux distribution.
  
</ul> 

#

<h3>Docker Images</h3>
<ul>
   <li>Like blueprints for containers</li>
       Runtime environment -  Application code -  Any dependencies - Extra configuration (Ex: env variables) - Commands
   <li>Run Container</li>
       Running instance of an image - Runs out application
	<li>Image is Read only</li>
	<li>Image are made up from several "layers"</li>
       run commands - dependencies - source code 
	<li>Parent image: includes the OS & sometime the runtime environment</li>
	<li>Docker Images : https://hub.docker.com/search?q=&type=image</li> 
	<li>Download Node Image</li> 
	   <pre>$ docker pull node</pre>
	<li>Delete all images, containers and volumes</li> 
	   <pre>$ docker system prune</pre>
	<li>Build new image</li> 
	   <pre>$ docker build -t myapp .</pre>	
	<li>Create and run new container with port</li> 
	   <pre>$ docker run --name myapp_c -p 4000:4000  -d myapp</pre>
		<pre>$ docker build -t myapp:nodemon .</pre>	
		<pre>$ docker run --name myapp_c_nodemon -p 4000:4000 --rm myapp:nodemon</pre>	
		 note: --rm to remove container when stoped 
	<li>Run container</li> 
	   <pre>$ docker start myapp_c</pre>	
	<li>Get all container</li> 
	   <pre>$ docker ps -a</pre>	
	<li>Get running container</li> 
	   <pre>$ dcoker ps</pre>	
	<li>Get all imagese</li> 
	   <pre>$ docker images</pre>		
	<li>Stop running container</li> 
	   <pre>$ docker stop myapp_c</pre>	
	<li>Create and run new container</li> 
	   <pre>$ docker run --name myapp_c1 myapp</pre>	
	<li>To run docker compose</li> 
	   <pre>$ docker-compose up</pre>	
	<li>Stop and remove containers, images and volumes in docker compose </li> 
	   <pre>$ docker-compose down --rmi all -v</pre>	
	<li>To push image to Repository in docker hub</li> 
	   <pre>$ docker push omargamel/myapi</pre>	
	<li>Remove image</li> 
	   <pre>$ docker image rm omargamel/myapi</pre>	
	<li>Pull image from docker hub</li> 
	   <pre>$ docker pull omargamel/myapi</pre>		
</ul> 

