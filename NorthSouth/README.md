**The Purpose of this template is to allow you to auto launch the architecture needed to test drive the Azure HA offering.**   


# Azure HA North/South Deployment

[<img src="http://azuredeploy.net/deploybutton.png"/>](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FPaloAltoNetworks%2FAzure-HA-AutoLaunch%2Fmaster%2FNorthSouth%2Fazuredeploy.json?token=AZoiWXZHIcxPcJG4iqbfyOUvHN1O8coUks5ahgGXwA%3D%3D)

# Requirements   
- VM-Series Plugin v1.0.4 or greater.
- A working Azure Service Principal.
For information on setting up an Azure Service Princial [CLICK HERE](https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal) 


**VM-Series Config File**   
a sample VM-Series configuration file has been included in this GitHub repository. This is preconfigured with all the necessary settings. You will need to add your service principal information and change the HA settings to your liking.  
***user:*** admin  
***pwd:*** PaloAlto@123 

**ARM Template Password**  
***user:*** pandemo  
***pwd:*** Dem0pa55w0rd

**Demo Video**
- North/South 	***3:21***  [CLICK HERE](
https://raw.githubusercontent.com/PaloAltoNetworks/Azure-HA-AutoLaunch/master/NorthSouth/AzureHANorthSouth.mp4)  

# Manual Approach
If you choose to take a different approach you can do the following

1. Launch a VM-Series firewall using the latest which is 9.1(only needed if you don't have an existing VM-Series launched)
2. Use Azure CLI to launch a second VM-Series running PAN-OS 9.1 into the exact same Resource Group as the first firewall

For more information on how to use the Azure CLI. [CLICK HERE](https://docs.microsoft.com/en-us/cli/azure/?view=azure-cli-latest)  
For an Online Azure CLI shell use the following link and select the Powershell option. [CLICK HERE](https://shell.azure.com/)  
For information on how to setup an Azure Service Principal [CLICK HERE](https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal)  

You will still be responsible for configuring your own Azure HA settings within the Azure Portal and the VM-Series firewall. Please refer to the VM-Series deployment guide for 9.1 for configuration details. [DEPLOYMENT GUIDE](https://docs.paloaltonetworks.com/vm-series/9-1/vm-series-deployment/set-up-the-vm-series-firewall-on-azure/configure-activepassive-ha-for-vm-series-firewall-on-azure.html)


# Support Policy: Community-Supported
The code and templates in this repository are released under an as-is, best effort, support policy. These scripts should viewed as community supported and Palo Alto Networks will contribute our expertise as and when possible. We do not provide technical support or help in using or troubleshooting the components of the project through our normal support options such as Palo Alto Networks support teams, or ASC (Authorized Support Centers) partners and backline support options. The underlying product used (the VM-Series firewall) by the scripts or templates are still supported, but the support is only for the product functionality and not for help in deploying or using the template or script itself. Unless explicitly tagged, all projects or work posted in our GitHub repository (at https://github.com/PaloAltoNetworks) or sites other than our official Downloads page on https://support.paloaltonetworks.com are provided under the best effort policy.
