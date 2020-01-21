# Proxmox Virtual Environment PVE  Open-source server virtualization software. 40.115.17.145 socialcoin-proxmox.westeurope.cloudapp.azure.com:8006

Proxmox VE is a complete open-source platform for enterprise virtualization. With the built-in web interface you can easily manage VMs and containers, software-defined storage and networking, high-availability clustering, and multiple out-of-the-box tools on a single solution.


# Proxmox experiment  theo theunissen 

Download the proxmox VE ISO-image vanaf https://www.proxmox.com/en/downloads/category/iso-images-pve 
en installeer deze bij Azure. (Mogelijk werkt t niet bij Azure… Discipl_Discipl)

[az create vm docs](https://docs.microsoft.com/en-us/cli/azure/vm?view=azure-cli-latest)
[azure-cli-latest#az-vm-create](https://docs.microsoft.com/en-us/cli/azure/vm?view=azure-cli-latest#az-vm-create)

## create azure debian virtual machine
``` az login ````  bosch.peter@outlook.com 0l

```` az group delete --name SocialcoinProxmoxGroup ````

```` az vm create --resource-group SocialcoinProxmoxGroup --name socialcoinVM ````

```` az group create --name SocialcoinProxmoxGroup --location westeurope````

```` touch cloud-init.txt````

````az vm create   --resource-group SocialcoinProxmoxGroup    --name  DebianBuster   --image Debian   --admin-username boscp08   --admin-password Di_Di   --custom-data cloud-init.txt   --generate-ssh-keys 
````


````
az vm create   --resource-group SocialcoinProxmoxGroup    --name  UbuntuLTS   --image UbuntuLTS   --admin-username boscp08   --admin-password Disicpl_Discipl   --custom-data cloud-init.txt   --generate-ssh-keys 
````


