# Docker Crach Course 
Docker is a container management tool, that makes it easy to run applications on any computer in an isolated container, that includes everything it needs to run predictably.
#
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
       1- Enable the Windows Subsystem for Linux<br>
           dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart<br> 
           <pre style="background-color:#F5F5F5;">
           $ git clone https://github.com/username/repository.git
           </pre>
       2- Check requirements for running WSL 2 : To update to WSL 2, you must be running Windows 10...<br>
       3- Enable Virtual Machine feature<br>
          dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
  
</ul> 
