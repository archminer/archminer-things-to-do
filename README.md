This will be a work in progress.

Why i did this? I have been working with linux since around 1998, and for some reason I've always avoided arch linux.  Over the past 6 months I started mining, anyone that knows me knows that I don't go the easy way ;) This was also an excuse for me to learn the power of arch linux and virtualbox \o/ 

We will end up creating a crypto miner system using virtualbox which will be much easier to work with rather than 100% on console :) 
Since I concentrate my mining with privacy based altcoins, I mine using AMD cards, yes RED TEAM :p So for my instructions as of right now I am only going to go over AMD drivers to start. This is not a complete step by step.  You will need some linux experience, otherwise you might find this alittle confusing. I will try my best to give credit where I can to everyone that I utilizing their code or tutorials.  

If you think this guide is helpful, please show some ❤ with some xmr 
4AMogZXHNd14zymMNT1RZWGsqPFXrEecQ66bkFR7i6CC2dmuAAG8FeMDAeCCfJgd3EE6tGgh74YQJ1HSAyP1HXuxHwZsQtF


What you'll need:
You can do this on a windows system or linux as long as you have a gui

<ul>
  <li>virtualbox https://www.virtualbox.org/wiki/Downloads</li>
  <li>archlinux iso https://www.archlinux.org/download/</li>
  <li>In the end you'll need a "thumb drive" or a hard drive</li>
</ul>

Everything else will be in the steps.

As mentioned before this is a work in progress.  So, I am actually using this for taking notes LOL, If you notice any issues please post as an issue :) Thank you, I'll try my best to keep up.

<b>STEPS:</b>
<ul>
  <li>Install virtualbox</li>
  <li>Download archlinux iso</li>
  <li>Create a new virtual machine.</li>
  <li>Create a virtual drive for the machine as small as possible, I am suggesting with 8gb.  But, as long as you have a drive that is larger or the same size your ok. Do not set it as dynamic. In virtualbox, set the drive as a regular SATA drive.</li>
  <li>By default virtualbox sets a "CD/DVD" in IDE.  Add the iso for archlinux there.  I would strongly suggest changing the network to bridged, this way you can login from your host computer or another computer on your network.</li>
  <li>Boot the system -> Boot Arch Linux</li>
  <li>You'll very quickly be at a command prompt with root access.</li>
  <li>"wget archfi.sf.net/archfi" https://github.com/MatMoul/archfi</li>
  <li>"sh archfi"</li>
  <li>Follow through the options (more detail coming) There is no need to install archdi which helps setup a gui interface</li>
  <li>After your done reboot. And remove the iso image from the virtual machine. Hopefully your system starts nicely.</li>
  <li>You will be have a login waiting for you.  Next login with root and the password you created.</li>
  <li>"pacman -Sy sudo openssh git yajl base-devel</li>
  <li>"useradd miner"</li> 
  <li>"passwd miner"</li>
  <li>"mkhomedir_helper miner"</li>
  <li>"visudo"</li>
  <li>Under the line "root ALL=(ALL) ALL" add </br>"miner ALL=(ALL) ALL"</li>
  <li>save and exit</li>
  <li>"vi /etc/ssh/sshd_config"
  <li>add the line "AllowUsers miner" and a seperate line for "PermitRootLogin no"
  <li>uncomment "Port 22</li>
  <li>Start the socket service.</br>"systemctl start sshd.socket"</br>Enable the socket service to run on boot.</br>"systemctl enable sshd.socket"</li>
 <li>"ip address show"
 <li>connect via ssh client using the ip shown and the added user miner.</li>
  <li>install yaourt, this will make your life much easier! https://archlinux.fr/yaourt-en </br>"git clone https://aur.archlinux.org/package-query.git"</br>"cd package-query"</br>"makepkg -si"</br>"cd .."</br>"git clone https://aur.archlinux.org/yaourt.git"</br>"cd yaourt"</br>"makepkg -si"</br>"cd .."</li>
 <li>
</ul>

