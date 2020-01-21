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

````az vm create   --resource-group SocialcoinCityGroup    --name  DebianBuster   --image Debian   --admin-username boscp08   --admin-password Di_Di   --custom-data cloud-init.txt   --generate-ssh-keys````

# FQDN
When you create a virtual machine (VM) in the Azure portal, a public IP resource for the virtual machine is automatically created. You use this IP address to remotely access the VM. Although the portal does not create a fully qualified domain name, or FQDN, you can add one once the VM is created. This article demonstrates the steps to create a DNS name or FQDN.

[FQDN](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/portal-create-fqdn)
