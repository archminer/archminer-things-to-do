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
  <li>By default virtualbox sets a "CD/DVD" in IDE.  Add the iso for archlinux there</li>
  <li>Boot the system -> Boot Arch Linux</li>
  <li>You'll very quickly be at a command prompt with root access.</li>
  <li>"wget archfi.sf.net/archfi"</li>
  <li>"sh archfi"</li>
  <li>Follow through the options (more detail coming)</li>
</ul>

