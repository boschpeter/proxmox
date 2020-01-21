# Proxmox Virtual Environment Open-source server virtualization software.

Proxmox VE is a complete open-source platform for enterprise virtualization. With the built-in web interface you can easily manage VMs and containers, software-defined storage and networking, high-availability clustering, and multiple out-of-the-box tools on a single solution.


Proxmox experiment

Download the proxmox VE ISO-image vanaf https://www.proxmox.com/en/downloads/category/iso-images-pve 
en installeer deze bij Azure. (Mogelijk werkt t niet bij Azure…)



``` az login ````  bosch.peter@outlook.com 0l
```` az group delete --name SocialcoinCityGroup ````
```` az vm create --resource-group SocialcoinCityGroup --name socialcoinVM ````
```` az group create --name SocialcoinCityGroup --location westeurope````
```` touch cloud-init.txt````

````az vm create   --resource-group SocialcoinCityGroup    --name  DebianBuster   --image Debian   --admin-username boscp08   --admin-password Discicpl_Discicpl   --custom-data cloud-init.txt   --generate-ssh-keys````
