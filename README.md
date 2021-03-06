# Proxmox Virtual Environment PVE  Open-source server virtualization software. 40.115.17.145 socialcoin-proxmox.westeurope.cloudapp.azure.com:8006

Proxmox VE is a complete open-source platform for enterprise virtualization. With the built-in web interface you can easily manage VMs and containers, software-defined storage and networking, high-availability clustering, and multiple out-of-the-box tools on a single solution.


# Proxmox experiment  theo theunissen Discipl_Discipl

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

````az vm create   --resource-group SocialcoinProxmoxGroup    --name  Socialcoin_proxmox   --image Debian   --admin-username boscp08   --admin-password D_D   --custom-data cloud-init.txt   --generate-ssh-keys 
````


````
az vm create   --resource-group SocialcoinProxmoxGroup    --name  UbuntuLTS   --image UbuntuLTS   --admin-username boscp08   --admin-password D_D   --custom-data cloud-init.txt   --generate-ssh-keys 
````

### pretty  

````
az vm create
--resource-group SocialcoinProxmoxGroup
--name DebianBuser
--image Debian
--admin-username boscp08
--admin-password Di..Di
--custom-data cloud-init.txt
--generate-ssh-keys
````

````
az vm create
--resource-group Discipl_Wigo4it_DockerGroup \
--name waardepapierenVM \
--image UbuntuLTS \
--admin-username ezahr \
--admin-password Di..._Wi...it \
--generate-ssh-keys \
--custom-data cloud-init.txt
````

Discipl_Discpl
### open sesame

````
az vm open-port --port 80 \
   --resource-group SocialcoinProxmoxGroup \
   --name  Socialcoin_proxmox
````

````
az vm open-port --port 443 \
  --resource-group SocialcoinProxmoxGroup \
  --name  Socialcoin_proxmox \
  --priority 1010
````

````
az vm open-port --port 8006 \
   --resource-group SocialcoinProxmoxGroup \
   --name Socialcoin_proxmox \
   --priority 1030
````

````
boscp08@boscp08-dingo:~$ ssh boscp08@40.115.17.145
Password: Di_Di
Linux socialcoinVM 4.19.0-6-cloud-amd64 #1 SMP Debian 4.19.67-2+deb10u2 (2019-11-11) x86_64

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
````

````ssh-copy-id -i ~/.ssh/id_rsa.pub boscp08@40.115.17.145````
   
   

# FQDN
When you create a virtual machine (VM) in the Azure portal, a public IP resource for the virtual machine is automatically created. You use this IP address to remotely access the VM. Although the portal does not create a fully qualified domain name, or FQDN, you can add one once the VM is created. This article demonstrates the steps to create a DNS name or FQDN.

[FQDN](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/portal-create-fqdn)
Now that your VM has a public IP and DNS name, you can deploy common application frameworks or services such as nginx, MongoDB, Docker, proxmox? etc.


[proxmox_works_on_azure](https://www.reddit.com/r/Proxmox/comments/cp2xrp/proxmox_works_on_azure/)

i fired up a D4s_v3 (4vCPU, 16GB RAM, 32GB SSD) + an additional 512GB SSD with a default Debian Buster (non backport) image, configured an SSH key-pair and opened up all ports to my home IP (but probably just 22, 8006 and maybe 443 would suffice).
After connecting via SSH [I followed the instructions at Install_Proxmox_VE_on_Debian_Buster](https://pve.proxmox.com/wiki/Install_Proxmox_VE_on_Debian_Buster)


![ssh_tunnel_socialcoin_Proxmox_Virtual_Environment.](https://github.com/boschpeter/proxmox/blob/master/pictures/ssh_tunnel_socialcoin_Proxmox_Virtual_Environment.png)

[goto_wiki->](https://github.com/boschpeter/proxmox/wiki/Install_Proxmox_VE_on_Debian_Buster)



boscp08@boscp08-dingo:~$ az vm create   --resource-group SocialcoinProxmoxGroup    --name  UbuntuLTS   --image UbuntuLTS   --admin-username boscp08   --admin-password D_D   --custom-data cloud-init.txt   --generate-ssh-keys 
{
  "fqdns": "",
  "id": "/subscriptions/cfcb03ea-255b-42f8-beca-2d4ac30779bb/resourceGroups/SocialcoinProxmoxGroup/providers/Microsoft.Compute/virtualMachines/UbuntuLTS",
  "location": "westeurope",
  "macAddress": "00-0D-3A-AE-66-01",
  "powerState": "VM running",
  "privateIpAddress": "10.0.0.5",
  "publicIpAddress": "23.101.73.20",
  "resourceGroup": "SocialcoinProxmoxGroup",
  "zones": ""
}

socialcoin-proxmox.westeurope.cloudapp.azure.com


Connection to socialcoin-proxmox.westeurope.cloudapp.azure.com closed.
boscp08@boscp08-dingo:~$ az vm create   --resource-group SocialcoinProxmoxGroup    --name  Socialcoin_proxmox   --image Debian   --admin-username boscp08   --admin-password Di_DI   --custom-data cloud-init.txt   --generate-ssh-keys 
{
  "fqdns": "",
  "id": "/subscriptions/cfcb03ea-255b-42f8-beca-2d4ac30779bb/resourceGroups/SocialcoinProxmoxGroup/providers/Microsoft.Compute/virtualMachines/Socialcoin_proxmox",
  "location": "westeurope",
  "macAddress": "00-0D-3A-AC-A5-8C",
  "powerState": "VM running",
  "privateIpAddress": "10.0.0.6",
  "publicIpAddress": "40.114.254.99",
  "resourceGroup": "SocialcoinProxmoxGroup",
  "zones": ""
}


