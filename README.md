# Azure RouteServer with NVA and VPN
This creates a hub vnet and an NVA vnet with a c8000v bgp peered to the route server, it creates a spoke vnet peered only to the nva vnet. An onprem vnet is created with an asav to with an ipsec tunnel the hub vnet vpngw. You'll be prompted for the resource group name, location where you want the resources created, your public ip and username and password to use for the VM's as well as the subsciption IDto use. NSG's are placed on the default subnets of each vnet allowing RDP access from your public ip. This also creates a logic app that will delete the resource group in 24hrs.

The topology will look like this:
<img width="1709" height="1398" alt="topology" src="https://github.com/user-attachments/assets/7cb5451f-3d1a-42fd-ac4d-5d9d5de6130f" />


You can run Terraform right from the Azure cloud shell by cloning this git repository with "git clone https://github.com/quiveringbacon/AzureRSwithNVAandVPN.git ./terraform".

Then, "cd terraform" then, "terraform init" and finally "terraform apply -auto-approve" to deploy.
